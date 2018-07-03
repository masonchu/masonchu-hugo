---
title: "在本機安裝 Minikube"
date: 2018-07-03T09:56:18+08:00
draft: false
weight: 20
pre: "<b>1. </b>"
---
minikube 是 kubernetes 社群推出的的一個輕量型工具，用於在本地端建置模擬 kubernetes 功能。minikube 支援以下幾種 vm driver。

1. virtualbox(預設值)
2. vmwarefusion
3. kvm2
4. kvm
5. hyperkit

> 後續內容預設使用 macOS + virtualbox。

## 安裝 VM
## 安裝 kubectl

```
brew install kubernetes-cli
```
確定安裝版本
```
kubectl version
```
> 如果還沒有啟動 Minikube 這時候會出現 The connection to the server localhost:8080 was refused 的訊息。

## 安裝 Minikube

```
curl -Lo minikube https://storage.googleapis.com/minikube/releases/v0.28.0/minikube-darwin-amd64 && chmod +x minikube && sudo mv minikube /usr/local/bin/
```
也可以使用 homebrew 安裝
```
brew cask install minikube
```
### 啟動 Minikube
```
minikube start
```
> 如果是第一次啟動，這時候會自動下載 Minikube ISO & kubelet & kubeadm

### 啟動 Minikube 儀表板
```
minikube dashboard
```
![minikube dashboard](/images/kubernetes/minikube-dashboard.png)
## reference
<https://kubernetes.io/docs/setup/minikube/#minikube-features>