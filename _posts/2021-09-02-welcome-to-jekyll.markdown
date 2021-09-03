---
layout: post
title:  "Welcome to Jekyll!"
date:   2021-09-02 17:23:10 +0800
categories: jekyll update
---

配置与流程

描述定义    
* **未登录** 指号码未通过校验
* **TSG订购** 通过外部网站的页面完成订购
* **破解** 指不在外部网站页面上 但验证码下发与回填最终会提交给外部网站的订购方式

### 配置一: 移动常规流程
$isLogin=\begin{cases}\text{if true} [] \\ \text{if false} [A1] \end{cases}$
$isCrbt=\begin{cases}\text{if true} [] \\ \text{if false} [B2, V2] \end{cases}$
$isOrder=\begin{cases}\text{if true} [] \\ \text{if false} [BCM] \end{cases}$

* 未登录+非彩+非会    
$\Large{号码短验 \to 开通功能资费确认 \to 订购会员资费确认 \to 移动TSG订购}$

* 未登录+非彩+是会    
$\Large{号码短验 \to 开通功能资费确认 \to 订购会员资费确认}$

* 未登录+是彩+非会    
$\Large{号码短验 \to 订购会员资费确认 \to 移动TSG订购}$

* 已登录+非彩+非会    
$\Large{开通功能资费确认 \to 订购会员资费确认 \to 移动TSG订购}$

* 已登录+非彩+是会    
$\Large{开通功能资费确认}$

* 已登录+是彩+非会    
$\Large{移动TSG订购}$


### 配置二：移动破解流程

$isLogin=\begin{cases}\text{if true} [] \\ \text{if false} [A1] \end{cases}$
$isCrbt=\begin{cases}\text{if true} [B3, V3] \\ \text{if false} [B4, V4] \end{cases}$
$isOrder=\begin{cases}\text{if true} [] \\ \text{if false} [B3, V3] \end{cases}$

非彩、非会，破解

* [A1,B4,V4,C6]：号码短验→开通彩铃+会员资费确认
* [A4,[B4,]V4,C6]：开通功能+会员短验

是彩，非会，破解

* [A1,B3,V3,C6]：号码短验→订购会员资费确认
* [A3,[B3,]V3,C6]：订购会员短验
* [A3,V3,C6]：订购会员短验
