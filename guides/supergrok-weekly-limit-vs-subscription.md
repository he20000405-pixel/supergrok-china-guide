---
title: "Grok 提示升级：旧版 SuperGrok 与联合会员周额度排查"
description: "Grok 付费后仍提示升级时，按旧版 SuperGrok 或 X 联合会员核对用量、账号与工作区，区分额度耗尽和订阅未生效，再按新旧订单入口处理。"
permalink: /guides/supergrok-weekly-limit-vs-subscription/
schema_type: Article
date_published: 2026-07-23
last_modified_at: 2026-10-28
breadcrumbs:
  - name: "首页"
    url: /
  - name: "专题"
    url: /guides/
  - name: "周额度与订阅状态"
    url: /guides/supergrok-weekly-limit-vs-subscription/
faq:
  - question: "SuperGrok 提示升级，是否说明订阅已经失效？"
    answer: "不一定。周额度耗尽不等于订阅被取消。旧版 Grok 在 Settings → Usage 核对用量，X 联合会员在 Grok Dashboard 核对目标工作区的 Usage；同时检查套餐、账号和原订单。额外用量可能产生费用，不要用重复购买会员来排障。"
  - question: "在哪里查看 SuperGrok 周额度和重置时间？"
    answer: "旧版 Grok 订阅在 Settings → Usage 查看；X 联合会员在 Grok Dashboard 选择正确工作区后查看 Usage。联合会员每个付费席位的周池只覆盖符合条件的第一方用量，Cursor 第三方模型另计费；剩余额度和重置时间以账号展示为准。"
  - question: "订阅有效但部分功能不可用，应该重新购买吗？"
    answer: "不应该。先核对 Usage、原购买渠道和当前账号。已有有效订阅、成功扣款或待处理交易时重复购买，可能形成多笔订阅或退款困难。"
  - question: "何时应该联系 ChongGrok 售后？"
    answer: "ChongGrok 订单的卡密或处理状态异常时，先按产品查原订单：X 联合会员使用 verify-x，旧版 SuperGrok 使用 verify-grok 并核对 User ID。向售后提供订单号和脱敏状态截图，不发送 SSO。官方订阅、用量或退款问题回原购买平台的支持入口处理。"
---

# Grok 付费后仍提示升级？区分新旧周额度、订阅状态与账号

**直接结论：先不要重复付款。**“提示升级”可能来自周额度已用完、当前账号没有附着订阅、登录方式不一致，或原订单尚未完成；它不能单独证明 SuperGrok 已经失效。

先确认订阅体系，再查看对应账号与用量页：

| 当前订阅 | 在哪里查 | 需要分清的规则 |
|---|---|---|
| 旧版 Grok / SuperGrok | `Settings → Billing` 与 `Settings → Usage` | Grok 功能共享周用量；额度耗尽后可等待重置，或查看账号开放的额外用量选项 |
| The X Subscription（X 联合会员） | [Grok Dashboard](https://grok.com/dashboard) 中购买时的工作区、套餐与 Usage | 每个付费席位有自己的第一方共享周池；Cursor 第三方模型与超出包含额度的第一方用量属于 Additional Usage |

联合会员不会把多个旧套餐的额度相加，团队不同席位也不共用同一个周池。先确认工作区和席位，再判断额度是否耗尽。新旧套餐与 Grok Bot 的资格见[联合会员指南]({{ '/guides/x-subscription-grok-bot-guide/' | relative_url }})；本文继续处理“额度用完”与“订阅未生效”的区别。

## 先看症状、含义和动作

| 看到的状态 | 可能含义 | 现在应该做什么 |
|---|---|---|
| Usage 显示周额度已用完并给出重置时间 | 订阅可能有效，但付费功能暂时停用 | 等待官方显示的重置，不要重复购买 |
| Billing 显示有效订阅，Usage 仍有额度 | 可能是应用状态、功能入口或账号问题 | 更新应用、退出并用原方式重登 |
| 商店显示有效订阅，Grok 显示 Free / Upgrade | 当前 Grok 登录账号可能不是原购买账号 | 核对 Apple / Google Play 与 Grok 登录身份 |
| 银行交易显示“待处理”，没有有效订阅记录 | 银行已经记录付款请求，但尚未确认款项最终付给商户 | 等交易结果明确，保留证据，不要再付一次 |
| ChongGrok 联合会员订单处理中 | 联合会员兑换尚未完成，或目标工作区未核对 | 在 [verify-x](https://chonggrok.com/verify-x) 查原结果，不向聊天发送 SSO |
| ChongGrok 旧版 SuperGrok 订单处理中 | 旧版兑换尚未完成，或 User ID 与目标账号不符 | 在 [verify-grok](https://chonggrok.com/verify-grok) 查状态并核对旧版订单 |
| 订阅已经到期或续费失败 | 最初付款的平台未成功续费 | 回原购买平台处理付款方式或续费 |

## 第一步：查看 Usage，而不是只看升级按钮

登录原购买账号。旧版进入 `Settings → Usage`；联合会员进入 Grok Dashboard，选中购买时的工作区再打开 Usage。记录：

1. 周用量池已使用比例；
2. 使用明细；
3. 页面显示的下一次重置时间；
4. Extra Usage Credits 的余额和设置（如果页面提供）；
5. 当前账号和登录方式；
6. 是否只有某项付费功能不可用。

周额度规则和具体消耗会变化，本文不写死固定请求次数，也不承诺某个统一重置时刻。应以当前账号 Usage 页面为准。

> 额度耗尽本身不等于订阅被取消。等待重置或使用官方提供的额外用量，是与重新购买第二份会员不同的操作；额外用量可能继续计费。

### 如果确实是周额度用完

先确认对应账号或工作区仍显示有效计划，并且 Usage 已到上限。联合会员可等待重置，或在官方账单页检查额外用量余额、自动补充和花费上限；第三方模型从使用时就属于额外付费，不会先消耗第一方周池。具体费用以账号及[官方用量说明](https://docs.x.ai/x-subscription/usage-limits)为准。

**以下是旧版 Grok 消费者 FAQ 对应的选项**，不要将其固定金额或免费层说明直接套到联合会员：

1. **等待重置。**以 Usage 页面显示的日期和时间为准。重置前不要反复退出账号或新增订阅。
2. **继续使用免费额度。**xAI 当前说明，付费额度用完后仍可在免费层级限制内使用 Chat 和 Voice；实际可用功能以账号页面为准。
3. **在网页端使用 Extra Usage Credits。**如果 Usage 页面提供该选项，可按页面提示购买额外用量。xAI 当前说明最低购买金额为 5 美元，额外用量按标准费率扣除，未使用余额通常在购买后一年到期，除非页面另有说明。
4. **设置 Auto Top Up。**如果账号页面提供自动补充，可设置单次补充金额和每月上限。先设置可接受的最高支出，再确认保存。
5. **长期频繁触顶时再比较更高套餐。**升级前先确认原计划没有待处理交易，并核对新套餐的实时额度与价格。

完成任何付费操作后，回到本订阅对应的 Usage 页面查看余额或用量状态。若银行已扣款但余额未更新，停止再次付款，保存收据并联系原支付方及官方支持。

> Extra Usage Credits 是 xAI 面向消费者账号提供的额外用量功能。ChongGrok 不销售 API 额度，也不提供 API 充值服务。

## 第二步：核对订阅是否仍有效

回到原购买入口，不要跨平台检查：

| 原购买入口 | 应检查的位置 | 主要处理方 |
|---|---|---|
| 旧版 Grok 网页订阅 | `Settings → Billing` | xAI |
| 官方 X 联合会员 | Grok Dashboard 中目标工作区的套餐与账单 | 官方订阅支持；商店收款时按原商店规则 |
| iPhone / iPad | Apple ID 的订阅与购买记录 | Apple |
| Android | Google Play 原购买账号的订阅记录 | 取消由 Google Play 管理；SuperGrok 退款按 xAI FAQ 由 xAI 处理 |
| X Premium+ | X Premium 设置及 Grok 账号连接 | X |
| ChongGrok X 联合会员 | verify-x 处理结果、目标工作区与套餐 | ChongGrok 核对原订单，不在聊天收取 SSO |
| ChongGrok 旧版 SuperGrok | verify-grok 状态、User ID 和处理记录 | ChongGrok 核对旧版订单 |

如果 Billing 或商店显示有效，而 Usage 又未达到上限，优先检查登录账号、登录方式、应用版本和本地缓存，不要直接新增订阅。

## 第三步：确认购买账号与当前账号一致

以下组合最容易造成“已经付费却仍提示升级”：

- 购买时使用 Apple 登录，后来改用 Google 或普通邮箱登录；
- Google Play 使用一个 Google 账号付款，Grok App 登录了另一个账号；
- X Premium+ 归属一个 X 账号，当前 Grok 连接的是另一个账号；
- 浏览器保留了多个 Grok 登录状态；
- 联合会员当前选中的工作区不是购买时的工作区；
- ChongGrok 旧版 SuperGrok 核销时提交的 User ID 与当前账号不一致。

退出后必须使用**原购买时的登录方式**重新登录。相同邮箱显示或相同昵称，不足以证明是同一个底层账号。

## 第四步：区分“仍显示 Free”和“额度已用完”

| 判断证据 | 更接近哪类问题 |
|---|---|
| Billing 有效，Usage 明确显示已到周上限 | 周额度问题 |
| Billing 无有效计划，银行只有“待处理”记录 | 银行尚未确认款项最终付给商户 |
| 商店有效，但 Grok 当前账号无权益 | 账号绑定或登录方式问题 |
| 订单成功且账号一致，仍无权益 | 已付款未生效问题 |
| 续费日后计划消失或降级 | 续费失败或订阅到期 |

如果已经成功扣款，但账号仍显示 Free、Activate 或 Upgrade，请进入[付款成功但仍显示 Free 排查]({{ '/guides/supergrok-paid-but-still-free/' | relative_url }})。如果付款本身被拒，请使用[付款失败专题]({{ '/guides/supergrok-payment-errors/' | relative_url }})。

## 第五步：按责任方准备证据

先对截图脱敏，再保留：

- 当前 Grok 账号与登录方式；
- Billing 或应用商店订阅状态；
- Usage 页面与重置时间；
- 订单号、付款时间、金额和交易状态；
- 错误原文与发生时间；
- 应用和 Grok Build 版本（如涉及）；
- ChongGrok 订单产品、卡密、兑换状态与提交记录（仅适用于本站订单）。联合会员先查 verify-x，旧版先查 verify-grok。

不要公开密码、验证码、恢复码、卡密、完整会话、支付卡完整号码或完整 User ID。联合会员 SSO 是临时登录凭证，不应发给客服聊天或放进状态截图；售后使用订单号与脱敏状态截图核对。

## 应联系谁

- grok.com 网页订阅、账号权益：xAI 支持；
- 官方 X 联合会员的工作区、席位及用量：联合会员官方支持；
- Apple 订单和退款：Apple；
- Google Play 订阅状态和取消：Google Play；
- Google Play 购买的 SuperGrok 退款：按 xAI 当前 FAQ 提交 xAI Refund Request；
- X Premium+ 订阅：X；
- ChongGrok 订单：联合会员查 verify-x，旧版 SuperGrok 查 verify-grok；兑换异常交 ChongGrok 售后，官方用量问题交官方支持；
- 银行交易显示“待处理”或被拒付：发卡行。

如果账号已有有效订阅、成功扣款或待处理交易，先处理原订单。只有原支付方确认没有有效订阅、待处理交易或退款流程，才重新比较方案；这不代表账号具备旧版续费资格。

新购可先核对官方 X 联合会员；考虑第三方协助时，在 [ChongGrok 联合会员服务页](https://chonggrok.com/x-subscription)确认账号与交付条件。保留旧版的用户，只有确认符合当前旧版商品条件后，才查看 [旧版 SuperGrok 续费页](https://chonggrok.com/supergrok?utm_source=github_guides&utm_medium=referral&utm_campaign=supergrok_weekly_limit)。ChongGrok 不办理旧会员转联合会员，需要转换时使用[官方 Unify 流程](https://docs.x.ai/x-subscription/unify-accounts)。

## 业务与风险边界

- ChongGrok 与 xAI、X 没有隶属关系；
- 旧版 User ID 是账号标识；联合会员 SSO 是临时登录凭证，两者不可互换；
- 不索要密码、邮箱验证码或恢复码；
- 不索要密码不等于不涉及敏感凭据；SSO 不发到聊天或公开页面；
- 不提供 API 额度、成品号、接码或批量注册；
- 不保证固定恢复时间、固定额度或所有账号结果；
- 任何线上订阅与第三方协助都不是零风险。

[官方购买政策](https://x.ai/pricing)明确未授权第三方销售，并说明相关账号可能被暂停或终止。服务页展示不等于官方认可。

{% include faq.html %}

## 官方来源

- [xAI Grok Website / Apps FAQ](https://docs.x.ai/grok/faq)
- [X 联合会员用量规则](https://docs.x.ai/x-subscription/usage-limits)
- [X 联合会员总览](https://docs.x.ai/x-subscription/overview)
- [AI 订阅付款排障决策树](https://he20000405-pixel.github.io/resources/ai-subscription-payment-troubleshooting/)

**本次更新：2026 年 10 月 28 日。**复核了新旧用量入口、官方周额度说明与 ChongGrok 兑换流程；没有执行真实购买、兑换或付费额度测试。套餐、费用与账号状态仍以对应平台实时页面为准。
