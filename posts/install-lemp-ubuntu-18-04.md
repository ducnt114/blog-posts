---
title: "Cài đặt Nginx, PHP, MySQL (LEMP stack) trên Ubuntu 18.04"
date: 2020-01-04T23:49:47+07:00
draft: true
---

## Giới thiệu

LEMP stack là bộ các phần mềm để xây dựng và triển khai các trang web động, bao gồm:

* L: Linux
* E: Nginx (Engine-X)
* M: MySQL
* P: PHP

## Yêu cầu 

Bài viết này giả định rằng bạn đã có sẵn 1 máy chủ cài đặt Ubuntu 18.04 (Linux), sau đây sẽ là các bước cài đặt các phần còn lại EMP.

## Bước 1: Cài đặt Nginx web server

Đầu tiên cần update các repository mới nhất:

```bash
sudo apt-get update
```

Sau đó là cài đặt nginx bằng apt:

```bash 
sudo apt-get install nginx
```

Ở ubuntu 18.04, Nginx sẽ tự động start ngay sau khi cài đặt.

Tiếp theo cần kiểm tra firewall có đang bật hay không:

```bash
sudo ufw status
```

nếu firewall đang tắt thì output sẽ như sau:

```bash
Status: inactive
```

Trong trường hợp firewall đang bật, cần phải đăng kí nginx với firewall để các request vào được port 80 của nginx:

```bash 
sudo ufw allow 'Nginx HTTP'
```

Kiểm tra lại firewall:

```bash
sudo ufw status
```

Nếu đăng kí thành công, output sẽ như sau:

```bash
Status: active

To                         Action      From
--                         ------      ----
OpenSSH                    ALLOW       Anywhere
Nginx HTTP                 ALLOW       Anywhere
OpenSSH (v6)               ALLOW       Anywhere (v6)
Nginx HTTP (v6)            ALLOW       Anywhere (v6)
```

Tiếp theo hãy truy cập vào IP hoặc domain của bạn để kiểm tra cài đặt nginx đã thành công hay chưa:

```
http://server_domain_or_IP
```

Nếu hiện ra trang web như sau là thành công:

![nginx default page](https://assets.digitalocean.com/articles/lemp_ubuntu_1604/nginx_default.png)


## Bước 2: Cài đặt MySQL

Cài đặt MySQL bằng lệnh:

```bash
sudo apt install mysql-server
```

Sau khi chạy xong command trên, mysql đã được cài đặt nhưng chưa được cấu hình hoàn chỉnh. Ta cần thiết lập một số tuỳ chọn bằng công cụ đi kèm của mysql server:

```bash
sudo mysql_secure_installation
```

chương trình sẽ hỏi bạn có muốn cài đặt `VALIDATE PASSWORD PLUGIN` hay không, đây là công cụ dùng để cấu hình và kiểm tra độ phức tạp của mật khẩu.

Nếu muốn cài đặt, hãy nhấn `Y`.

```
VALIDATE PASSWORD PLUGIN can be used to test passwords
and improve security. It checks the strength of password
and allows the users to set only those passwords which are
secure enough. Would you like to setup VALIDATE PASSWORD plugin?

Press y|Y for Yes, any other key for No:
```

Tiếp theo bạn cần chọn độ phức tạp của mật khẩu tương ứng:

```
There are three levels of password validation policy:

LOW    Length >= 8
MEDIUM Length >= 8, numeric, mixed case, and special characters
STRONG Length >= 8, numeric, mixed case, special characters and dictionary                  file

Please enter 0 = LOW, 1 = MEDIUM and 2 = STRONG: 1
```

Sau khi chọn độ phức tạp 0/1/2 tương ứng, bạn sẽ cần thiết lập mật khẩu cho tài khoản `root`:

```
Please set the password for root here.

New password:

Re-enter new password:
```

Ở bản MySQL 5.7 trở về sau, tài khoản root của MySQL sẽ được đăng nhập trực tiếp bằng tài khoản root của Linux host, thông qua plugin `auth_socket`. Điều này là an toàn hơn trong một số trường hợp nhưng lại hạn chế về tính tiện lợi khi ta muốn đăng nhập tài khoản root từ các nguồn khác, chẳng hạn từ phpMyAdmin.
Để thiết lập đăng nhập tài khoản root của MySQL bằng mật khẩu, thực hiện câu lệnh:

```bash
sudo mysql
```

Kiểm tra chế độ xác thực tài khoản bằng câu lệnh:

```bash
mysql> SELECT user,authentication_string,plugin,host FROM mysql.user;
```

Output:

```
+------------------+-------------------------------------------+-----------------------+-----------+
| user             | authentication_string                     | plugin                | host      |
+------------------+-------------------------------------------+-----------------------+-----------+
| root             |                                           | auth_socket           | localhost |
| mysql.session    | *THISISNOTAVALIDPASSWORDTHATCANBEUSEDHERE | mysql_native_password | localhost |
| mysql.sys        | *THISISNOTAVALIDPASSWORDTHATCANBEUSEDHERE | mysql_native_password | localhost |
| debian-sys-maint | *CC744277A401A7D25BE1CA89AFF17BF607F876FF | mysql_native_password | localhost |
+------------------+-------------------------------------------+-----------------------+-----------+
4 rows in set (0.00 sec)
```

Như ví dụ trên, bạn có thể thấy user `root` đang xác thực bằng plugin `auth_socket`. Để đăng nhập tài khoản `root` bằng mật khẩu, chạy câu lệnh:

```
mysql> ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
```

Tiếp theo cần `FLUSH PRIVILEGES` để các thay đổi được thực hiện:

```
mysql> FLUSH PRIVILEGES;
```

Kiểm tra lại thiết lập vừa thay đổi:

```
mysql> SELECT user,authentication_string,plugin,host FROM mysql.user;
```

output:

```
+------------------+-------------------------------------------+-----------------------+-----------+
| user             | authentication_string                     | plugin                | host      |
+------------------+-------------------------------------------+-----------------------+-----------+
| root             | *3636DACC8616D997782ADD0839F92C1571D6D78F | mysql_native_password | localhost |
| mysql.session    | *THISISNOTAVALIDPASSWORDTHATCANBEUSEDHERE | mysql_native_password | localhost |
| mysql.sys        | *THISISNOTAVALIDPASSWORDTHATCANBEUSEDHERE | mysql_native_password | localhost |
| debian-sys-maint | *CC744277A401A7D25BE1CA89AFF17BF607F876FF | mysql_native_password | localhost |
+------------------+-------------------------------------------+-----------------------+-----------+
4 rows in set (0.00 sec)
```

Như bạn thấy, tài khoản root lúc này đã được xác thực bằng `mysql_native_password` thay cho `auth_socket`.

> **Note**: Lưu ý là từ lúc này, để đăng nhập vào tài khoản root, 
> bạn cần dùng câu lệnh: `mysql -u root -p` và nhập mật khẩu 

Đến đây thì database đã sẵn sàng, chuyển qua bước cuối cùng là cài đặt PHP.

## Bước 3: Cài đặt PHP

Do Nginx không có trình xử lý PHP đi kèm nên chúng ta cần cài thêm `php-fpm` (viết tắt của `fastCGI processing manager`). Khi có gói phần mềm này, các request vào trang php sẽ được Nginx forward sang cho php-fpm xử lý.

Tuỳ thuộc vào việc máy chủ linux mà bạn cài như thế nào, có thể bạn sẽ phải cập nhật repository của apt bằng lệnh:

```bash
sudo add-apt-repository universe
```

Tiếp theo ta sẽ cài đặt 2 gói `php-fpm` và `php-mysql` bằng lệnh:

```bash
sudo apt install php-fpm php-mysql
```

Đến đây thì ta đã có đủ bộ các thành phần của LEMP stack, tuy nhiên để có thể chạy hoàn chỉnh 1 trang web PHP thì ta cần thực hiện thêm một số cấu hình của Nginx. Đầu tiên bạn cần thêm 1 file config cho trang web, giả sử là `example.com`, ta sẽ tạo 1 file như sau:

```
sudo vim /etc/nginx/sites-available/example.com
```

Nội dung của file như sau:

```
server {
        listen 80;
        root /var/www/html;
        index index.php index.html index.htm index.nginx-debian.html;
        server_name example.com;

        location / {
                try_files $uri $uri/ =404;
        }

        location ~ \.php$ {
                include snippets/fastcgi-php.conf;
                fastcgi_pass unix:/var/run/php/php7.2-fpm.sock;
        }

        location ~ /\.ht {
                deny all;
        }
}
```

Mặc định thì Nginx sẽ chỉ đọc các file config ở thư mục `/etc/nginx/sites-enabled/` nên ta sẽ tạo 1 symlink bằng lệnh sau:

```
sudo ln -s /etc/nginx/sites-available/example.com /etc/nginx/sites-enabled/
```

Tiếp theo ta sẽ bỏ file config mặc định của Nginx trong thư mục `/sites-enabled/`:

```
sudo unlink /etc/nginx/sites-enabled/default
```

Kiểm tra file config có lỗi gì hay không bằng lệnh:

```
sudo nginx -t
```

Nếu có thông báo lỗi nào hiện ra, cần kiểm tra và sửa lại file config.

Sau khi hoàn tất, reload lại Nginx để cập nhật file config mới:

```
sudo systemctl reload nginx
```

## Bước 4: Tạo file PHP để kiểm tra quá trình cài đặt

Tạo 1 file php trong thư mục web như sau:

```
sudo vim /var/www/html/info.php
```

nội dung của file:

```php
<?php
phpinfo();
```

Lưu lại file, sau đó kiểm tra bằng trình duyệt:

```
http://your_server_domain_or_IP/info.php
```

nếu thấy nội dung như sau là quá trình cài đặt thành công:

![php info page](https://assets.digitalocean.com/lemp_ubuntu_1804/php_info_1804.png)

Khi kiểm tra xong, đừng quên xoá file `info.php` đi để đảm bảo an toàn cho máy chủ của bạn:

```
sudo rm /var/www/html/info.php
```

Đến đây ta hoàn tất quá trình cài đặt LEMP stack trên Ubuntu 18.04

## Tổng kết

Ngày nay, có nhiều công cụ và framework khác nhau để phát triển các trang web, tuy nhiên đa số vẫn sử dụng PHP do ưu điểm thời gian phát triển nhanh và tiện dụng. Hi vọng bài viết này giúp đỡ mọi người trong quá trình cài đặt LEMP stack trên Ubuntu 18.04.

