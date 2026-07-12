---
title: "Grok User ID 怎么找：userId 获取、UUID 核对与安全说明"
description: "Grok User ID 查询教程：登录 grok.com 后打开 api/auth/session，复制 userId 字段，区分邮箱、X 用户名和 xUserId。"
permalink: /guides/grok-user-id/
date_published: 2026-07-11
last_modified_at: 2026-07-11
breadcrumbs:
  - name: "首页"
    url: /
  - name: "专题"
    url: /guides/
  - name: "Grok User ID"
    url: /guides/grok-user-id/
faq:
  - question: "Grok User ID 是邮箱或 X 用户名吗？"
    answer: "不是。需要复制 grok.com/api/auth/session 返回内容中的 userId 字段，通常是带横线的 UUID。"
  - question: "Grok User ID 是密码吗？"
    answer: "不是，它不能单独用于登录账号。但它仍属于账号标识，不应公开发布，应只在确认的充值核销流程中提交。"
  - question: "找不到 userId 怎么办？"
    answer: "先确认浏览器已经登录正确的 grok.com 账号，再在同一浏览器打开 session 地址。仍找不到时停止提交并联系售后核对。"
---

# Grok User ID 怎么找

**Grok User ID** 是用于识别 Grok 账号的字段。SuperGrok 充值需要的是 JSON 中的 `userId`，不是邮箱、昵称、X 用户名、手机号码或 `xUserId`。

## 30 秒获取步骤

1. 打开 [grok.com](https://grok.com)，登录要升级的账号。
2. 保持登录状态，在同一浏览器打开 `https://grok.com/api/auth/session`。
3. 在返回的 JSON 文本中找到 `userId`。
4. 复制引号内的完整值，不要手动输入。
5. 回到 [chonggrok.com 卡密核销页](https://chonggrok.com/verify)，核对后提交。

<img src="../../img/grok-login-homepage.webp" alt="先确认已经登录目标 Grok 账号" width="1600" height="824" loading="lazy">

<img src="../../img/grok-user-id-session-url.webp" alt="在地址栏打开 Grok session 页面" width="1600" height="950" loading="lazy">

## 正确格式是什么

常见格式是 UUID，例如：

```text
12345678-1234-1234-9234-123456789abc
```

它通常由字母、数字和横线组成。复制前后不要带空格，也不要漏掉字符。

<img src="../../img/grok-user-id-json-example.webp" alt="使用虚构数据制作的 Grok User ID JSON 示意图" width="1600" height="824" loading="lazy">

上图使用虚构 UUID 和隐藏邮箱，仅用于说明字段位置，不是真实用户数据。

## 最常见的五种填错

| 错误内容 | 为什么不对 |
|---|---|
| 登录邮箱 | 邮箱不是 `userId` |
| X 用户名 | X 平台公开用户名不能替代 Grok 账号标识 |
| 昵称 | 昵称可重复，也可能随时修改 |
| `xUserId` | 字段名称不同，不应混用 |
| 截图 OCR 识别结果 | 容易漏字符或把字母数字识别错 |

最稳妥的方法是直接复制 `userId`，不要手打，不要依靠截图识别。

## 安全边界

User ID 不是密码，也不能单独登录账号，但仍不应随意公开。session 页面还可能包含邮箱、头像或其他账号信息，因此：

- 不要把整段 JSON 发布到公开平台；
- 不向服务方提供密码、验证码或恢复码；
- 只在已确认的 [核销页面](https://chonggrok.com/verify)提交所需的 `userId`；
- 发现账号不一致时立即停止，不要尝试多个 User ID。

## 页面显示未登录怎么办

回到 grok.com 重新登录，确认页面右上角或账户设置显示的是目标账号，然后再次打开 session 地址。若浏览器存在多个账户或隐私窗口，注意两个页面必须处于同一个登录会话。

主站补充图文：[Grok User ID 怎么找](https://chonggrok.com/blog/grok-user-id-zenme-zhao)。准备提交前也可查看[完整充值流程]({{ '/guides/supergrok-auto-recharge/' | relative_url }})。

如果 User ID 已提交、订单也已付款，但账号仍显示 Free，请停止尝试其他 User ID，转到[付款后仍显示 Free 排查]({{ '/guides/supergrok-paid-but-still-free/' | relative_url }})核对核销状态和当前登录账号。

{% include faq.html %}
