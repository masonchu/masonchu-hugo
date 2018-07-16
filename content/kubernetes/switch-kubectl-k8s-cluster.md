---
title: "切換 kubectl 對應的 k8s 叢集"
date: 2018-07-12T09:50:57+08:00
draft: true
---
在本地端安裝 minikube 之後，就可以使用 kubectl 對 k8s 進行相關的操作，但是 kubectl 怎麼知道他對硬的是哪個環境，或著說之後建立了其他測試環境或是雲端 AWS, GCP。那怎麼使用 kubectl 操作。

## 什麼是 Context

取得可以對應的 contect
```
kubectl config get-contexts
```
切換 kubectl 對應
```
kubectl config use-context CONTEXT_NAME
```

## ref

<https://kubernetes.io/docs/tasks/access-application-cluster/web-ui-dashboard/>

kubectx
<https://github.com/ahmetb/kubectx>