---
title: "DevOps Cheat Sheet"
date: 2021-03-08T11:04:00+07:00
categories: [devops]
tags: [devops]
---

## Linux

### Increase max open file

File: `/etc/security/limits.conf`

```
* hard nofile 1024000
* soft nofile 1024000
* hard nproc 65535
* soft nproc 65535

<os-user> soft memlock unlimited
<os-user> hard memlock unlimited
```

### Rsync parallel

```
rsync -aHAXxv --numeric-ids --delete --progress -e "ssh -T -c arcfour -o Compression=no -x" user@<source>:<source_dir> <dest_dir>
```

## MySQL

- Create user
```bash
CREATE USER 'finley'@'localhost' IDENTIFIED BY 'password';
GRANT ALL PRIVILEGES ON *.* TO 'finley'@'localhost';
GRANT SELECT ON *.* TO 'u'@'%' IDENTIFIED BY 'password';

FLUSH PRIVILEGES;
```

- Change password
```bash
ALTER USER 'root'@'localhost' IDENTIFIED BY 'MyNewPass';
or
SET PASSWORD FOR 'root'@'localhost' = PASSWORD('MyNewPass');
```

- Dump
```bash
mysqldump [options] db_name [tbl_name ...]
```

- Import
```bash
mysql -u <username> -p <databasename> < <filename.sql>
```

## Redis 

### Delete key by pattern

```bash
redis-cli --raw keys "$PATTERN" | xargs redis-cli del
redis-cli KEYS "prefix:*" | xargs redis-cli DEL
```