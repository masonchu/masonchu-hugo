---
menuTitle: "microservices"
title: "開始 microservices"
date: 2018-06-29T11:03:34+08:00
weight: 15
draft: false
---
## monolithic vs microservices
以往在建構大型系統的時候，本來也就是會區分成多個部分來進行。像是常見的金流物流系統，就是將部分系統功能區分出去。microservices 則是將這種概念又更延伸到極致。

## 前置作業
開始進行 microservices 至少要具備的基本建設。
### 開發相關配置 
1. 服務發現 service discovery  
	1. k8s etcd
	2. consul
	3. zookeeper
	4. Netflix/eureka
2. 事件訊息 event sourcing messaging
	1. kafka
3. 系統監控 monitor  
	1. metrics
	2. Prometheus
	3. Grafana
4. 訊息傳遞 transport
	1. grpc
	2. thrift
	3. http
5. 斷路器 Circuit Breaker
6. 紀錄追蹤 Log Tracking
	1. opentracing
	2. zipkin
7. Auth

### Devops
1. CI / CD
2. Docker
3. k8s

## golang 相關套件
1. go-kit <https://github.com/go-kit/kit>
2. go-micro <https://github.com/micro/go-micro>
3. gizmo <https://github.com/nytimes/gizmo>
4. rpcx <https://github.com/smallnest/rpcx>

## 造成延伸問題
microservices solve organizational problems  
microservices cause technical problems

## Reference
Go + Microservices = Go Kit [I] - Peter Bourgon, Go Kit <https://www.youtube.com/watch?v=NX0sHF8ZZgw>  
微服務基礎建設 - Service Discovery <http://columns.chicken-house.net/2017/12/31/microservice9-servicediscovery/>
