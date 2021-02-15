---
title: "Xây dựng restful API service bằng Golang"
date: 2020-02-06T22:47:12+07:00
categories: [tutorial]
tags: [golang,microservices,restful,api]
draft: true
---

## Giới thiệu

Việc xây dựng hệ thống bằng mô hình microservices đang rất phổ biến hiện nay, trong đó Go đang là 1 sự lựa chọn rất phù hợp để viết code của các service backend.

Trong bài viết này tôi sẽ giới thiệu với các bạn cách xây dựng 1 restful service đơn giản bằng Go.

## Framework và các thư viện 

* [mux](https://github.com/gorilla/mux) 
* [gorm](https://github.com/jinzhu/gorm)
* [godotenv](https://github.com/joho/godotenv)

## Dựng khung project

Cấu trúc tổ chức thư mục của project sẽ như sau:

```
▾ config/                                        
    conf.go                                      
▾ controllers/                                   
▾ repositories/                                  
▾ router/                                        
▾ services/                                      
  go.mod
```

## Tổng kết

Bài viết này tôi đã giới thiệu với các bạn cách xây dựng 1 api service đơn giản bằng Go, cách tổ chức code trong project theo MVC pattern cho rõ ràng, dễ phát triển và maintain cũng như unit test.

Trong bài viết tiếp theo tôi sẽ trình bày cách đóng gói và deploy service bằng Docker, cùng chờ đợi và theo dõi nhé.