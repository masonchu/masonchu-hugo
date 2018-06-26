---
title: "Gvm Go Version"
date: 2018-06-25T14:54:21+08:00
draft: true
---

使用 GVM 安裝 Go 1.6、Go1.4 與各種版本的做法(首次安裝)
```
gvm install go1.4 --binary # 直接安裝 binary
gvm use go1.4 # 使用 go1.4 的環境
export GOROOTBOOTSTRAP=$GOROOT # 設定 $GOROOTBOOTSTRAP
gvm install go1.6 # 安裝 Go 1.6
Installing go1.6...
```