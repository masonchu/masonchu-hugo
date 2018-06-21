---
title: "安裝和啟用 NSQ 服務"
date: 2018-06-21T15:53:16+08:00
tags:        [ "microservice" ]
topics:      [ "microservice" ]
draft: false
---
<!-- # 使用 NSQ -->
## 安裝 NSQ
NSQ 本身有提供 brew / docker 版本。在這邊我是直接使用 github 原始碼下載編譯，注意 golang 1.7+ 並且已經有 dep 套件管理。在 test.sh 會執行 golang test & 編譯出所有的可執行檔。
### 下載 source code & 安裝相依性套件
```
git clone https://github.com/nsqio/nsq $GOPATH/src/github.com/nsqio/nsq
cd $GOPATH/src/github.com/nsqio/nsq
dep ensure
```
### 測試 & 編譯
```
./test.sh
```
### 安裝到 $GOPATH/bin
```
go install ./apps/nsqlookupd
go install ./apps/nsqd
go install ./apps/nsqadmin
```
### 依序啟動服務
nsqlookupd 預設監聽 http:4161 / tcp:4160，而 nsqd 啟動時自動到 nsqlookupd 註冊。
```
nsqlookupd
nsqd --lookupd-tcp-address=127.0.0.1:4160
nsqadmin --lookupd-http-address=127.0.0.1:4161
```