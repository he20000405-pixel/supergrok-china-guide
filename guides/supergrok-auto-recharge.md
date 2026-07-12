---
title: "SuperGrok 国内自助充值教程：支付宝微信、卡密核销与 User ID"
description: "2026 SuperGrok 国内充值完整流程：进入 chonggrok.com 选择周期、支付宝微信付款、核销卡密、提交 Grok User ID 和验收订阅。"
permalink: /guides/supergrok-auto-recharge/
date_published: 2026-07-11
date_modified: 2026-07-12
breadcrumbs:
  - name: "首页"
    url: /
  - name: "专题"
    url: /guides/
  - name: "自助充值"
    url: /guides/supergrok-auto-recharge/
faq:
  - question: "SuperGrok 国内充值需要提供密码吗？"
    answer: "不需要。chonggrok.com 的流程只提交本次升级所需的 Grok User ID，不应提交登录密码、验证码或恢复码。"
  - question: "卡密应该在哪里核销？"
    answer: "付款获得卡密后，进入 https://chonggrok.com/verify 验证卡密，并按页面提示提交 Grok User ID。"
  - question: "充值完成后如何确认到账？"
    answer: "回到自己的 grok.com 账号检查订阅和权益状态；如果页面没有刷新，可退出后重新登录再检查。"
---

# SuperGrok 国内自助充值完整流程

**适合谁：**没有稳定境外卡，希望使用支付宝或微信为自己的 Grok 账号开通 SuperGrok 的用户。

> 结论：进入 [chonggrok.com/supergrok](https://chonggrok.com/supergrok)选择实时套餐并付款，拿到卡密后在 [chonggrok.com/verify](https://chonggrok.com/verify)核销，提交自己的 Grok User ID，最后回到 grok.com 验收订阅。全程不需要登录密码。

## 下单前先检查

| 检查项 | 正确状态 |
|---|---|
| 账号 | 可以正常登录 grok.com，确认是要升级的账号 |
| User ID | 能在 `grok.com/api/auth/session` 找到完整 `userId` |
| 套餐 | 已按当前用途选择主站实时展示的订阅周期 |
| 安全 | 不准备提交密码、邮箱验证码或恢复码 |
| 记录 | 能保存订单号、卡密、付款时间和核销状态 |

如果账号无法正常登录，或无法确认当前登录的是哪个账号，应先解决账号问题再购买。

## 第一步：进入 SuperGrok 充值页

打开 [https://chonggrok.com/supergrok](https://chonggrok.com/supergrok)，查看当前可选周期和实时价格。套餐、活动和价格可能变化，因此本指南不固定展示金额。

![chonggrok.com SuperGrok 充值页](../img/chonggrok-supergrok-home-hero-hd.png)

## 第二步：选择订阅周期并付款

按实际使用周期选择套餐，使用支付宝或微信完成付款。首次尝试、已形成稳定工作流和有连续项目的人，适合的周期不同，具体判断见 [SuperGrok 套餐怎么选]({{ '/guides/supergrok-plans/' | relative_url }})。

付款后保存：

- 订单号；
- 卡密；
- 付款时间；
- 选择的套餐；
- 必要的页面状态截图。

## 第三步：核销卡密

进入 [https://chonggrok.com/verify](https://chonggrok.com/verify)，粘贴卡密并提交验证。卡密属于订单凭证，不要公开发布，也不要让无关人员代为核销。

![chonggrok.com 卡密核销页面](../img/chonggrok-supergrok-redeem-console-hd.png)

## 第四步：提交 Grok User ID

登录目标 Grok 账号，在同一浏览器打开 `https://grok.com/api/auth/session`，复制 `userId` 字段的完整 UUID。它不是邮箱、昵称、X 用户名或 `xUserId`。

不要把整个 session 页面公开给他人；只复制流程明确要求的 `userId`。详细核对见 [Grok User ID 查找指南]({{ '/guides/grok-user-id/' | relative_url }})。

## 第五步：确认账号并提交充值

核销页面识别账号后，确认它确实是自己的目标账号，再点击确认充值。若显示的账号信息与预期不一致，应停止提交并重新核对 User ID。

## 第六步：验收订阅

处理完成后回到 grok.com：

1. 检查当前登录账号是否正确；
2. 查看订阅状态和模型入口；
3. 如果界面仍显示旧状态，退出后重新登录；
4. 仍未更新时，保留订单、卡密和提交记录联系售后，不要重复下单。

## 风险说明

不要求密码能减少不必要的账号暴露，但不等于绝对安全。Grok User ID 仍是账号标识，应只通过已确认的核销页面提交。任何线上订阅服务都不是零风险，也不能诚实承诺固定到账时间或账号结果。

如果购买目的包括 Grok Build，应先查看 [Grok Build 登录与 403 排查]({{ '/guides/grok-build-login-403/' | relative_url }})，确认问题是否真的与订阅权益有关。更多主站图文说明：[SuperGrok 充值完整教程](https://chonggrok.com/blog/supergrok-chongzhi-zhinan)与[安全充值检查清单](https://chonggrok.com/blog/supergrok-safe-recharge-checklist)。

{% include faq.html %}
