---
title: "開始 microservices 架構"
date: 2017-07-05T15:52:11+08:00
tags:        [ "microservice", "golang" ]
topics:      [ "microservice", "golang" ]
draft: true
---
## 為什麼 microservices
以往在建構大型系統的時候，本來也就是會區分成多個部分來進行。像是常見的金流物流系統，就是將部分系統功能區分出去。microservices 則是將這種概念又更延伸到極致。
一開始這個架構被稱為 monolithic ，是從 java 開始流行起來。

## 前置作業
要開始進行 microservices 之前我認為至少要具備一些基本的系統服務處理，如果這幾個項目沒有先處理或是設想好，在實際開發上帶來的缺點可能比優點更多。  
1. 服務發現 service discovery  
2. 事件訊息 event sourcing  
3. 系統監控 monitor  
4. 訊息傳遞 RPC
## 造成延伸問題
microservices solve organizational problems  
microservices cause technical problems
## Reference
`Go + Microservices = Go Kit [I] - Peter Bourgon, Go Kit`<https://www.youtube.com/watch?v=NX0sHF8ZZgw>  
