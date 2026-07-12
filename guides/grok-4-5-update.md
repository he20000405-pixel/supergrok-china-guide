---
title: "Grok 4.5 正式发布：更新内容、首发入口与 SuperGrok 可用性"
description: "xAI 于 2026 年 7 月 8 日发布 Grok 4.5。本文整理官方确认的编程、智能体和知识工作能力，并说明 SuperGrok 是否可用的事实边界。"
permalink: /guides/grok-4-5-update/
date_published: 2026-07-11
date_modified: 2026-07-12
breadcrumbs:
  - name: "首页"
    url: /
  - name: "专题"
    url: /guides/
  - name: "Grok 4.5"
    url: /guides/grok-4-5-update/
faq:
  - question: "Grok 4.5 什么时候发布？"
    answer: "xAI 官方发布页日期为 2026 年 7 月 8 日。"
  - question: "Grok 4.5 主要更新了什么？"
    answer: "官方重点强调编程、智能体任务和知识工作，并公布了多项软件工程与终端任务基准结果。"
  - question: "开通 SuperGrok 一定能使用 Grok 4.5 吗？"
    answer: "不能仅根据订阅名称保证。发布页明确列出 Grok Build、Cursor 和 SpaceXAI console 等入口，但普通 grok.com / SuperGrok 账号是否可见，应以账号模型选择器和官方实时说明为准。"
  - question: "本文提供 Grok 4.5 API 充值吗？"
    answer: "不提供。本文只做版本信息和会员订阅入口说明，chonggrok.com 不提供 API 额度服务。"
---

# Grok 4.5 正式发布：更新内容与 SuperGrok 可用性

xAI 于 **2026 年 7 月 8 日**发布 Grok 4.5。对普通用户最重要的不是只看跑分，而是分清三件事：官方确认了哪些能力、当前从哪些入口提供、自己的 SuperGrok 账号是否已经实际可见。

## 先说结论

- Grok 4.5 已正式发布，不是传闻或预告。
- 官方将重点放在编程、智能体任务和知识工作。
- 官方发布页明确列出的入口包括 Grok Build、Cursor 和 SpaceXAI console。
- 该发布页没有明确承诺所有普通 grok.com / SuperGrok 账户都能立即在模型选择器看到 Grok 4.5。
- 因此，购买 SuperGrok 前应检查自己的模型选择器，不能把充值宣传成“保证解锁 Grok 4.5”。

## 官方确认了什么

根据 [xAI Grok 4.5 官方发布页](https://x.ai/news/grok-4-5)，Grok 4.5 面向：

- coding；
- agentic tasks；
- knowledge work。

官方还说明该模型与 Cursor 协同训练，并公布 Terminal Bench 2.1、DeepSWE、SWE Bench Pro 等基准结果。基准可以帮助理解技术方向，但不能替代用户在自己任务上的实际测试。

## 首发入口与订阅边界

官方“Getting started”部分明确提到 Grok Build、Cursor 和 SpaceXAI console。这里必须区分：

1. **模型已经发布**，不等于每个消费级账号同时开放；
2. **某个工具可接入**，不等于普通 grok.com 模型选择器必然出现；
3. **历史上 SuperGrok 能使用某些 Grok 模型**，也不能自动证明 Grok 4.5 当天已向所有 SuperGrok 账户开放。

最可靠的检查顺序是：

1. 登录自己的 grok.com 账号；
2. 查看模型选择器和订阅页面；
3. 阅读 xAI 最新官方说明；
4. 再决定是否购买或续费。

## 国内用户是否值得开通 SuperGrok

如果你本来就持续使用 Grok 做写作、检索、分析或编程辅助，SuperGrok 的价值应根据当前账号实际权益判断，而不是只为了追一个新版本名称。若账号模型列表尚未出现 Grok 4.5，应等待官方逐步开放或查看当前可用入口，不要把第三方承诺当作官方可用性证明。

没有稳定境外支付方式时，可查看 [chonggrok.com SuperGrok 充值页](https://chonggrok.com/supergrok)。该服务使用支付宝/微信付款，只提交自己的 Grok User ID，不需要密码；但它解决的是会员订阅付款问题，**不承诺某个模型必然已向你的账号开放**。

## 本文不讨论 API 充值

Grok 4.5 官方发布内容包含开发者入口，但本仓库只服务于 Grok / SuperGrok 会员订阅信息，不提供 API 额度、开发者控制台充值、成品号、接码或批量注册建议。

## 信息来源

- [xAI: Grok 4.5（2026-07-08）](https://x.ai/news/grok-4-5)
- [xAI News](https://x.ai/news?category=all)
- [Grok plans](https://grok.com/plans)

继续阅读：[Grok Build 登录与 403 排查]({{ '/guides/grok-build-login-403/' | relative_url }})、[SuperGrok 与 X Premium+ 对比]({{ '/guides/supergrok-vs-x-premium-plus/' | relative_url }})、[SuperGrok 充值流程]({{ '/guides/supergrok-auto-recharge/' | relative_url }})。

{% include faq.html %}
