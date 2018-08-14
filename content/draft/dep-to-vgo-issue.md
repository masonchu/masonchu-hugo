---
title: "從 dep 轉換到 vgo"
date: 2018-08-01T15:48:37+08:00
draft: true
---
在 go1.11 之後，vgo 會直接加入 go 官方套件管理工具，在正式釋出之前遇到一些小問題。

## vscode gopkgs 支援

如果是使用 Microsoft/vscode-go 套件在 vscode 下開發的話，使用 vgo 之後移除 vendor 套件，會發現專案內 go import 出現找不到路徑的錯誤，這是由於 vscode-go 使用的 toolchain 還沒有更新的問題。立即的解法就是直接將 vscode 設定 `go.alternateTools` 直接改成 vgo 就可以了。
```
"go.alternateTools": {
	"go": "vgo"
},
```

## exec: "clang": executable file not found in $PATH

使用 vgo 啟動出現這個錯誤的話，目前暫時使用
```
CGO_ENABLED=0 vgo build
CC=gcc vgo build
```

## ref
<http://www.evanlin.com/til-practical-in-vgo/>  
<https://github.com/Microsoft/vscode-go/issues/1532>  
<https://github.com/golang/go/issues/23965>  