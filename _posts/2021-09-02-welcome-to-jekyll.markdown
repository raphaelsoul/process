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

### 移动

#### 两步确认+TSG

$\large{号码短验 \to 开通功能资费确认 \to 订购会员资费确认 \to 移动TSG订购}$    
$isLogin=\begin{cases}\text{if true} [] \\ \text{if false} [A1] \end{cases}$
$isCrbt=\begin{cases}\text{if true} [] \\ \text{if false} [B2, B3, V2] \end{cases}$
$isOrder=\begin{cases}\text{if true} [] \\ \text{if false} [BCM] \end{cases}$

#### 会员确认+TSG
$\large{号码短验 \to 订购会员资费确认 \to 移动TSG订购}$    
$isLogin=\begin{cases}\text{if true} [] \\ \text{if false} [A1] \end{cases}$
$isCrbt=\begin{cases}\text{if true} [] \\ \text{if false} [V2] \end{cases}$
$isOrder=\begin{cases}\text{if true} [] \\ \text{if false} [B3, BCM] \end{cases}$

#### 单步双确认+TSG
$\large{号码短验 \to 开通功能+会员资费确认 \to 移动TSG订购}$    
$isLogin=\begin{cases}\text{if true} [] \\ \text{if false} [A1] \end{cases}$
$isCrbt=\begin{cases}\text{if true} [] \\ \text{if false} [B4, V2] \end{cases}$
$isOrder=\begin{cases}\text{if true} [] \\ \text{if false} [BCM] \end{cases}$

#### 仅TSG
$\large{号码短验 \to 移动TSG订购}$    
$isLogin=\begin{cases}\text{if true} [] \\ \text{if false} [A1] \end{cases}$
$isCrbt=\begin{cases}\text{if true} [] \\ \text{if false} [V2] \end{cases}$
$isOrder=\begin{cases}\text{if true} [] \\ \text{if false} [BCM] \end{cases}$

#### 两步确认
$\large{号码短验 \to 开通功能资费确认 \to 订购会员资费确认}$    
$isLogin=\begin{cases}\text{if true} [] \\ \text{if false} [A1] \end{cases}$
$isCrbt=\begin{cases}\text{if true} [] \\ \text{if false} [B2] \end{cases}$
$isOrder=\begin{cases}\text{if true} [] \\ \text{if false} [B3, V4] \end{cases}$

#### 仅功能确认
$\large{号码短验 \to 开通功能资费确认}$    
$isLogin=\begin{cases}\text{if true} [] \\ \text{if false} [A1] \end{cases}$
$isCrbt=\begin{cases}\text{if true} [] \\ \text{if false} [B2, V2] \end{cases}$
$isOrder=\begin{cases}\text{if true} [] \\ \text{if false} [V3] \end{cases}$

$isLogin=\begin{cases}\text{if true} [] \\ \text{if false} [A1] \end{cases}$
$isCrbt=\begin{cases}\text{if true} [] \\ \text{if false} [B2] \end{cases}$
$isOrder=\begin{cases}\text{if true} [] \\ \text{if false} [V4] \end{cases}$

#### 仅会员确认
$\large{号码短验 \to 订购会员资费确认}$    
$isLogin=\begin{cases}\text{if true} [] \\ \text{if false} [A1] \end{cases}$
$isCrbt=\begin{cases}\text{if true} [] \\ \text{if false} [] \end{cases}$
$isOrder=\begin{cases}\text{if true} [] \\ \text{if false} [B3, V4] \end{cases}$

#### 单步双确认
$\large{号码短验 \to 开通功能+会员资费确认}$    
$isLogin=\begin{cases}\text{if true} [] \\ \text{if false} [A1] \end{cases}$
$isCrbt=\begin{cases}\text{if true} [] \\ \text{if false} [] \end{cases}$
$isOrder=\begin{cases}\text{if true} [] \\ \text{if false} [B4, V4] \end{cases}$

#### 直接破解/开通
$\large{号码短验}$    
$isLogin=\begin{cases}\text{if true} [] \\ \text{if false} [A4] \end{cases}$

### 联通
#### TSG
$\large{号码短验 \to TSG订购}$    
$isLogin=\begin{cases}\text{if true} [] \\ \text{if false} [A1] \end{cases}$
$isOrder=\begin{cases}\text{if true} [] \\ \text{if false} [BUM] \end{cases}$

#### 功能二次确认+TSG
$\large{号码短验 \to 开通功能资费确认 \to 开通功能资费二次确认 \to 联通TSG订购}$    
$isLogin=\begin{cases}\text{if true} [] \\ \text{if false} [A1] \end{cases}$
$isCrbt=\begin{cases}\text{if true} [] \\ \text{if false} [B2, B21, V2] \end{cases}$
$isOrder=\begin{cases}\text{if true} [] \\ \text{if false} [BUM] \end{cases}$

#### 短验开通功能+TSG
$\large{开通功能短验 \to 联通TSG订购}$    
$isLogin=\begin{cases}\text{if true} [] \\ \text{if false} [A2] \end{cases}$
$isCrbt=\begin{cases}\text{if true} [] \\ \text{if false} [V2] \end{cases}$
$isOrder=\begin{cases}\text{if true} [] \\ \text{if false} [BUM] \end{cases}$

#### 会员短验 双确认
$\large{订购会员短验 \to 订购会员资费确认 \to 开通功能资费确认}$    
$isLogin=\begin{cases}\text{if true} [] \\ \text{if false} [A3] \end{cases}$
$isCrbt=\begin{cases}\text{if true} [] \\ \text{if false} [B2, V2] \end{cases}$
$isOrder=\begin{cases}\text{if true} [] \\ \text{if false} [B3, V3] \end{cases}$

#### 会员短验
$\large{订购会员短验}$    
$isLogin=\begin{cases}\text{if true} [] \\ \text{if false} [] \end{cases}$
$isOrder=\begin{cases}\text{if true} [] \\ \text{if false} [A3, V3] \end{cases}$

### 电信

#### TSG
$\large{号码短验 \to TSG订购}$    
$isLogin=\begin{cases}\text{if true} [] \\ \text{if false} [A1] \end{cases}$
$isOrder=\begin{cases}\text{if true} [] \\ \text{if false} [BTM] \end{cases}$

#### 两步短验+两步确认
$\large{订购功能短验 \to 开通功能资费确认 \to 订购会员短验 \to 订购会员资费确认}$    
$isLogin=\begin{cases}\text{if true} & [] \\ \text{if false} & [A2] \end{cases}$
$isCrbt=\begin{cases}\text{if true} & [] \\ \text{if false} & [B2, V2] \end{cases}$
$isOrder=\begin{cases}\text{if true} & [] \\ \text{if false} & [A3, B3, V3] \end{cases}$

#### 两步短验开通
$\large{订购功能短验 \to 订购会员短验}$    
$isLogin=\begin{cases}\text{if true} & [] \\ \text{if false} & [A2] \end{cases}$
$isCrbt=\begin{cases}\text{if true} & [] \\ \text{if false} & [V2] \end{cases}$
$isOrder=\begin{cases}\text{if true} & [] \\ \text{if false} & [A3, V3] \end{cases}$

#### 双开短验+单步双确认
$\large{开通功能+会员短验 \to 开通彩铃+会员资费确认}$    
$isLogin=\begin{cases}\text{if true} & [] \\ \text{if false} & [A4] \end{cases}$
$isOrder=\begin{cases}\text{if true} & [] \\ \text{if false} & [B4, V4] \end{cases}$

#### 双开短验
$\large{开通功能+会员短验 \to 开通彩铃+会员资费确认}$    
$isLogin=\begin{cases}\text{if true} & [] \\ \text{if false} & [A4] \end{cases}$
$isOrder=\begin{cases}\text{if true} & [] \\ \text{if false} & [V4] \end{cases}$