---
title: httpRpcProxy
date: 2017-12-03 09:44:08
tags: rpc
---

# httpRpcProxy
> use http to achive RPC(romote process call)

## 适用场景

> 方便调用一些远端的rest接口

## 技术原理

> 借助Java动态代理，将带有特定注解的service方法调用改为http远程通信。

## 如何使用

1. 可以实际需求自定义http header

2. 略加修改可以支持json和protobuf序列化方式

3. 根据业务需求添加service，通过spring注入bean调用。

## 源码
[httpRpcProxy](https://github.com/newjunwei/httpRpcProxy)