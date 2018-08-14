---
title: "設定 mysql 帳號權限"
date: 2018-08-13T12:52:27+08:00
draft: true
---

To list users:
```
select user,host from mysql.user;
```
To show privileges:
```
show grants for 'user'@'host';
```
To change privileges, first revoke. Such as:
```
revoke all privileges on *.* from 'user'@'host';
```
Then grant the appropriate privileges as desired:
```
grant SELECT,INSERT,UPDATE,DELETE ON `db`.* TO 'user'@'host';
```
Finally, flush:
```
flush privileges;
```

## Ref
https://serverfault.com/questions/115950/how-do-i-change-the-privileges-for-mysql-user-that-is-already-created  
https://blog.toright.com/posts/1214/mysql-%E6%96%B0%E5%A2%9E%E4%BD%BF%E7%94%A8%E8%80%85%E8%88%87%E6%AC%8A%E9%99%90%E8%A8%AD%E5%AE%9A-%E7%AD%86%E8%A8%98.html