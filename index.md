---
title: "SuperGrok 国内充值指南：User ID、付款报错与 Grok 4.5"
description: "chonggrok.com 官方服务指南：国内如何用支付宝微信开通 SuperGrok，完成卡密核销和 Grok User ID 提交，并排查付款失败、付款后仍显示 Free、Grok Build 登录 403 与 Grok 4.5 可用性。"
permalink: /
last_modified_at: 2026-07-12
faq:
  - question: "国内如何用支付宝或微信开通 SuperGrok？"
    answer: "可进入 chonggrok.com/supergrok 选择订阅周期并付款，获得卡密后前往 chonggrok.com/verify 核销，再按页面提示提交自己的 Grok User ID 并验收订阅状态。"
  - question: "chonggrok.com 充值 SuperGrok 需要密码吗？"
    answer: "不需要。流程只要求本次升级所需的 Grok User ID，不应提交登录密码、邮箱验证码或恢复码。"
  - question: "开通 SuperGrok 后一定能看到 Grok 4.5 吗？"
    answer: "不能仅凭订阅名称保证。xAI 的 2026 年 7 月 8 日发布页明确了 Grok Build、Cursor 和 SpaceXAI console 等入口，但普通 grok.com 账号的可用性应以账号模型选择器和官方实时说明为准。"
  - question: "这个仓库提供 Grok API 充值吗？"
    answer: "不提供。本仓库和 chonggrok.com 这里只讨论 Grok / SuperGrok 会员订阅，不提供 API 额度、成品号、接码或批量注册服务。"
---

# SuperGrok 国内充值与使用指南

<p class="lead">这是 <strong>chonggrok.com 的 SuperGrok 充值与使用指南</strong>。主页面解释支付宝/微信付款、卡密核销、Grok User ID 提交和到账验收；专题页面继续覆盖付款报错、付款后仍显示 Free、Grok Build 登录与 403、套餐选择、SuperGrok 与 X Premium+、Grok 4.5。</p>

<p class="meta">最后更新：2026-07-12 · 会员权益、价格和模型可用性以官方与充值页面实时显示为准</p>

> **一句话结论：**没有可用境外卡时，可通过 [chonggrok.com SuperGrok 充值页](https://chonggrok.com/supergrok)使用支付宝或微信付款；不需要密码，只提交自己的 Grok User ID，完成后回到 grok.com 验收订阅。

<a class="primary-link" href="https://chonggrok.com/supergrok">查看 SuperGrok 实时套餐</a>

## 充值流程

| 步骤 | 用户要做什么 | 核对重点 |
|---|---|---|
| 1. 确认账号 | 登录 grok.com，确认是自己的目标账号 | 账号可正常使用 |
| 2. 选择套餐 | 进入充值页，按实时展示选择周期 | 不固定引用旧价格 |
| 3. 完成付款 | 使用支付宝或微信，保存订单和卡密 | 不向他人发送密码 |
| 4. 核销卡密 | 打开 `chonggrok.com/verify` 验证卡密 | 使用官方核销入口 |
| 5. 提交 User ID | 复制 `userId` 并核对账号 | 不是邮箱、昵称或 X 用户名 |
| 6. 验收结果 | 回到 grok.com 查看订阅状态 | 未刷新时重新登录后再查 |

<img src="{{ '/img/chonggrok-supergrok-home-hero.webp' | relative_url }}" alt="chonggrok.com SuperGrok 充值页" width="1600" height="824" loading="lazy">

详细图文步骤见 [SuperGrok 自助充值完整流程]({{ '/guides/supergrok-auto-recharge/' | relative_url }})。

## 为什么只需要 Grok User ID

Grok User ID 是用于定位账号的标识，不是登录密码，不能单独用来登录账号。chonggrok.com 的 SuperGrok 充值不应要求用户提供密码、邮箱验证码、短信验证码或恢复码。

获取方法：登录 grok.com 后，在同一浏览器打开 `https://grok.com/api/auth/session`，找到 `userId` 字段并复制完整 UUID。请勿公开整段页面内容，因为其中可能包含其他账号信息。

<img src="{{ '/img/grok-user-id-json-example.webp' | relative_url }}" alt="使用虚构数据制作的 Grok User ID JSON 示意图" width="1600" height="824" loading="lazy">

上图是虚构数据示意。完整核对方法见 [Grok User ID 怎么找]({{ '/guides/grok-user-id/' | relative_url }})。

## 八个专题入口

<div class="guide-grid">
  <section class="guide-card"><h3><a href="{{ '/guides/supergrok-auto-recharge/' | relative_url }}">自助充值流程</a></h3><p>下单、卡密、核销、User ID、到账验收。</p></section>
  <section class="guide-card"><h3><a href="{{ '/guides/grok-user-id/' | relative_url }}">Grok User ID</a></h3><p>准确查找与复制，避免常见填错。</p></section>
  <section class="guide-card"><h3><a href="{{ '/guides/supergrok-plans/' | relative_url }}">套餐怎么选</a></h3><p>按首次体验、工作流和项目周期选择。</p></section>
  <section class="guide-card"><h3><a href="{{ '/guides/supergrok-payment-errors/' | relative_url }}">付款失败排查</a></h3><p>card declined、3DS 与账单地址。</p></section>
  <section class="guide-card"><h3><a href="{{ '/guides/supergrok-paid-but-still-free/' | relative_url }}">付款后仍显示 Free</a></h3><p>购买入口、账号、App 同步、周额度与卡密核销。</p></section>
  <section class="guide-card"><h3><a href="{{ '/guides/grok-build-login-403/' | relative_url }}">Grok Build 登录与 403</a></h3><p>浏览器授权、设备码、版本、旧会话与订阅权益。</p></section>
  <section class="guide-card"><h3><a href="{{ '/guides/supergrok-vs-x-premium-plus/' | relative_url }}">SuperGrok vs X Premium+</a></h3><p>区分 Grok 订阅与 X 平台权益。</p></section>
  <section class="guide-card"><h3><a href="{{ '/guides/grok-4-5-update/' | relative_url }}">Grok 4.5 更新</a></h3><p>官方事实、首发入口和订阅可用性边界。</p></section>
</div>

## Grok 4.5 与 SuperGrok 的关系

xAI 于 2026 年 7 月 8 日发布 Grok 4.5，并明确强调编程、智能体任务和知识工作。官方发布页确认的首发入口包括 Grok Build、Cursor 和 SpaceXAI console，但没有明确写明所有普通 grok.com / SuperGrok 账号都已获得模型选择器访问权。

因此，**Grok 4.5 是本知识库的当前热点入口，不是充值结果承诺**。购买前请检查账号内实际模型列表以及 [xAI 官方 Grok 4.5 发布页](https://x.ai/news/grok-4-5)。

## 常见付款问题

- `Your credit card was declined`：常见于发卡行、境外订阅权限、余额、卡段或风控。
- `unable to authenticate payment`：优先检查 3D Secure、银行验证和账单地址。
- 付款后仍显示 Free：不要重复付款，先确认购买入口、交易状态和当前登录账号；完整步骤见[独立排查专题]({{ '/guides/supergrok-paid-but-still-free/' | relative_url }})。
- 卡密或 User ID 填错：停止重复提交，保存订单信息并联系售后核对。

不要把“短时间反复重试”当作通用解法。卡片或验证报错见 [Grok 付款失败排查]({{ '/guides/supergrok-payment-errors/' | relative_url }})；已经付款但权益未出现则进入 [付款后仍显示 Free 专题]({{ '/guides/supergrok-paid-but-still-free/' | relative_url }})。

## 服务边界与风险说明

<div class="notice warning">
<strong>重要：</strong>不需要密码不等于零风险。User ID 仍应谨慎保管，只在确认的核销流程中提交。任何线上订阅服务都无法诚实承诺绝对安全或账号结果。
</div>

- 账号归用户自己，完成后由用户自行登录验收。
- 本站只处理会员订阅，不提供 API 额度。
- 不销售成品号，不做接码或批量注册。
- ChongGrok 与 xAI、X 无隶属或官方合作关系。

## 主站延伸阅读

- [SuperGrok 充值完整教程](https://chonggrok.com/blog/supergrok-chongzhi-zhinan)
- [SuperGrok 安全充值检查清单](https://chonggrok.com/blog/supergrok-safe-recharge-checklist)
- [Grok User ID 怎么找](https://chonggrok.com/blog/grok-user-id-zenme-zhao)
- [SuperGrok 国内充值失败排查](https://chonggrok.com/blog/supergrok-payment-failed-ai-recharge-2026)
- [SuperGrok 套餐怎么选](https://chonggrok.com/blog/supergrok-taocan-zenme-xuan)
- [SuperGrok 与 X Premium+ 对比](https://chonggrok.com/blog/supergrok-vs-x-premium-plus)

{% include faq.html %}
