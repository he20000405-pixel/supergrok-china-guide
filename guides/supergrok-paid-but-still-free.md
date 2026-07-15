---
title: "SuperGrok 付款成功但仍显示 Free：账号、订阅入口、App 同步与卡密核销排查"
description: "SuperGrok 已扣款但未生效、付款成功仍显示 Free 或卡密核销后未到账时，按 grok.com、App Store、Google Play、X Premium+ 和 ChongGrok 订单入口排查。"
permalink: /guides/supergrok-paid-but-still-free/
date_published: 2026-07-12
last_modified_at: 2026-07-12
breadcrumbs:
  - name: "首页"
    url: /
  - name: "专题"
    url: /guides/
  - name: "付款后仍显示 Free"
    url: /guides/supergrok-paid-but-still-free/
faq:
  - question: "SuperGrok 已扣款但仍显示 Free，应该再买一次吗？"
    answer: "不建议。先确认交易状态、购买入口、付款账号和当前登录账号，再检查对应平台的订阅状态。重复购买可能形成多笔订单，使退款和权益核对更复杂。"
  - question: "为什么商店显示订阅有效，Grok 仍提示 Activate 或 Upgrade？"
    answer: "常见方向是登录账号或登录方式不一致、应用版本或本地缓存未刷新。确认商店订阅有效后，更新应用、退出并使用原购买方式重新登录，必要时重启或重装应用。"
  - question: "使用 Apple 隐藏邮箱购买后，应该怎样登录？"
    answer: "应继续使用原来的 Sign in with Apple 登录。不要改用私密转发邮箱通过 Google 或普通邮箱登录，否则可能进入另一个账号，导致订阅无法被识别。"
  - question: "ChongGrok 卡密核销后仍未到账怎么办？"
    answer: "先在核销页查看处理状态，核对提交的 Grok User ID 与当前账号是否一致，并保存订单号、卡密、提交记录和页面截图联系售后；不要重复核销或改填其他 User ID。"
---

# SuperGrok 付款成功但仍显示 Free 怎么办

> **一句话结论：不要重复付款。**先确认钱是从哪个入口支付的、交易是否真正完成，以及当前登录的 Grok 账号是否就是购买订阅的账号，再到对应平台检查订阅状态。

**English summary:** If SuperGrok was charged but Grok still shows Free, Activate or Upgrade, first identify the original purchase channel and sign-in account. Check web billing, App Store or Google Play subscription status, X account linking, or the ChongGrok redemption record before paying again.

**Keywords:** `SuperGrok still Free` · `SuperGrok charged not active` · `Grok Activate Upgrade` · `SuperGrok subscription not showing` · `ChongGrok card key redemption`

<!-- 截图占位：Grok 显示 Free / Activate / Upgrade 的真实脱敏截图。未提供清晰素材前不公开显示。 -->

## 先区分四种状态

“银行卡显示扣款”和“SuperGrok 已经激活”不是同一件事。先记录你实际看到的状态：

| 当前证据 | 能说明什么 | 下一步 |
|---|---|---|
| 银行交易仍显示待处理或授权 | 只能说明支付请求进入银行流程 | 等待交易状态明确，不要重复提交 |
| Apple / Google Play 显示有效订阅 | 商店侧存在订阅 | 核对 Grok 登录账号、登录方式和应用状态 |
| grok.com Billing 显示有效计划 | 网页账号存在订阅 | 退出重登，检查是否用错账号或额度已用完 |
| ChongGrok 核销页显示处理中 | 订单已经进入处理流程 | 保留订单与卡密，在原页面查询状态 |
| 只有付款截图，没有订阅记录 | 暂不能证明权益已经绑定账号 | 回到原购买入口查订单、收据或订阅状态 |

不要把支付页面截图当作唯一验收标准。最终应以**对应购买平台的订阅记录**和**目标 Grok 账号内的权益状态**共同判断。

## 第一步：确认从哪里购买

SuperGrok、X Premium+ 和应用商店订阅由不同平台管理。先选择与你实际购买方式一致的路径：

| 购买入口 | 应检查的位置 | 主要责任方 |
|---|---|---|
| grok.com 网页 | Grok `Settings → Billing` | xAI |
| iPhone / iPad | Apple ID 的订阅和购买记录 | Apple 处理交易与退款 |
| Android | Google Play 的订阅记录 | Google Play 管理订阅，退款按 xAI 官方 FAQ 指引 |
| X Premium+ | X 的 Premium 设置与 Grok 账号连接 | X 处理 X Premium 订阅问题 |
| chonggrok.com | 卡密核销状态、订单和提交的 User ID | ChongGrok 售后核对 |

如果自己已经记不清入口，先查收据、账单商户、应用商店订阅列表和订单邮件，不要在另一个入口再次购买。

## grok.com 网页订阅怎么查

登录付款时使用的 Grok 账号，打开 [Grok Billing](https://grok.com/?_s=billing) 或进入 `Settings → Billing`：

1. 查看当前计划是否显示有效；
2. 核对付款账号与当前页面账号是否一致；
3. 如果管理订阅按钮无法打开，关闭可能拦截页面的扩展，或改用无痕窗口和其他浏览器；
4. 仍无法确认时，通过 [xAI 官方消费者 FAQ](https://docs.x.ai/grok/faq)中的支持入口提交问题。

网页 Billing 没有有效订阅时，不要仅凭银行扣款判断已经开通。保存付款时间、金额、账单状态和账号信息，交由原支付方核对。

## App Store 或 Google Play 显示有效，但 Grok 仍提示升级

xAI 官方 FAQ 建议同时确认应用和商店两侧的订阅状态：

1. 将 Grok App 更新到最新版本；
2. 在 App Store 或 Google Play 的订阅列表确认订阅仍有效；
3. 确认 Grok App 登录的是购买时的同一个账号；
4. 完全关闭并重新打开应用；
5. 退出账号后，使用原购买时的登录方式重新登录；
6. 必要时清理缓存，或删除后重新安装应用。

不要把网页账号、Apple 登录、Google 登录和 X 登录看成天然相同的账号。即使显示同一个昵称，也可能对应不同登录身份。

### Apple Hide My Email 的特殊情况

如果购买时使用了 Apple 的“隐藏邮件地址”，应继续使用 **Sign in with Apple** 登录。不要复制私密转发邮箱，再通过 Google 或普通邮箱登录；官方 FAQ 明确指出，这样可能无法识别原订阅。

退款也必须回到原购买入口处理：Apple App Store 购买由 Apple 负责；网页和 Google Play 购买按 xAI 官方 FAQ 的对应流程处理。

## X Premium+ 已生效，Grok 为什么仍显示 Free

X Premium+ 权益属于购买它的 X 账号。先确认：

1. 当前 X Premium+ 确实处于有效状态；
2. Grok 连接的是这个 X 账号，而不是另一个个人账号；
3. 在 Grok `Settings → Account` 检查 X 账号连接；
4. 必要时通过 [xAI Accounts](https://accounts.x.ai)核对登录方式；
5. X Premium 订阅、退款或账号问题按 [X Premium 官方 FAQ](https://help.x.com/en/using-x/x-premium-faq)处理。

不要把 X Premium+、SuperGrok 网页订阅和普通 X 账号混成同一份订单。订阅只能绑定到实际购买和连接的账号。

## 可能不是订阅失效，而是付费周额度已用完

xAI 官方 FAQ 说明，付费用户使用共享的周额度池。达到周额度后，付费功能会暂停到额度重置，但 Chat 和 Voice 仍可使用独立的免费额度。

因此，如果 Billing 明确显示订阅有效，但部分高级功能暂停或页面出现升级提示，应同时检查 `Settings → Usage`：

- 是否已经用完本周付费额度；
- 是否只有部分付费功能暂停；
- 是否把“仍能使用免费额度”误判成订阅消失。

额度用完与付款未生效是两类问题。重复购买同一订阅并不是通用解决方案。

## ChongGrok 卡密核销后仍未到账

如果是在 chonggrok.com 购买，先不要去其他入口重复下单。按下面顺序核对：

1. 打开 [卡密核销与状态查询](https://chonggrok.com/verify)；
2. 查看卡密是未使用、处理中、完成还是异常状态；
3. 核对提交的 `userId` 是否属于当前登录的 Grok 账号；
4. 回到 grok.com 退出后重新登录，再检查订阅；
5. 保存订单号、卡密、付款时间、提交的 User ID 和状态截图；
6. 仍未更新时，用这些记录联系 ChongGrok 售后核对。

Grok User ID 不是登录密码，但仍属于账号标识。不要公开订单、卡密、完整 session JSON 或 User ID，也不要在问题未确认时改填其他账号的 User ID。

详细操作见 [SuperGrok 自助充值流程]({{ '/guides/supergrok-auto-recharge/' | relative_url }})和 [Grok User ID 核对指南]({{ '/guides/grok-user-id/' | relative_url }})。

## 联系售后前准备哪些证据

| 证据 | 用途 | 隐私处理 |
|---|---|---|
| 原购买入口和付款时间 | 确认由谁处理订单 | 不公开完整银行卡信息 |
| 订单号或商店收据 | 定位交易 | 只发给对应支持渠道 |
| 当前登录方式 | 排查账号不一致 | 不提供密码、验证码或恢复码 |
| Billing / 订阅状态截图 | 判断权益是否绑定 | 隐藏邮箱和个人信息 |
| ChongGrok 卡密与提交记录 | 核对核销流程 | 不公开发布卡密或 User ID |
| Free / Activate / Upgrade 页面截图 | 说明实际现象 | 先隐藏账号标识 |

描述问题时写清楚“从哪个入口购买、哪个账号登录、哪里显示有效、哪里仍显示 Free”，比只说“没有到账”更容易定位。

## 什么时候才适合重新购买

只有在原支付方明确确认**没有有效订单或订阅**，并且不存在待处理交易、重复订阅或退款流程时，才重新评估购买。

如果最终确认尚未成功开通，且没有合适的海外付款方式，可以查看 [chonggrok.com SuperGrok 充值页](https://chonggrok.com/supergrok)。该流程支持支付宝或微信，提交自己的 Grok User ID，不需要登录密码；但任何线上订阅服务都不是零风险，也不能保证固定到账时间或特定功能立即开放。

主站延伸阅读：[SuperGrok 充值完整教程](https://chonggrok.com/blog/supergrok-chongzhi-zhinan)与[SuperGrok 国内充值失败排查](https://chonggrok.com/blog/supergrok-payment-failed-ai-recharge-2026)。

## 风险与业务边界

- 本文只讨论 Grok / SuperGrok 会员订阅，不提供 API 额度、成品号、接码或批量注册服务。
- 不要求用户提供 Grok、X、Apple、Google 或邮箱密码，也不应提交验证码和恢复码。
- User ID 不是密码，但仍应只通过确认的会员核销流程提交。
- ChongGrok 是独立第三方充值协助服务，与 xAI、X、Apple 或 Google 没有隶属或官方合作关系。
- 订阅权益、额度、退款和页面状态以对应官方平台实时显示为准。

需要在 grok.com、App Store、Google Play、X 和第三方订单之间判断责任方时，可使用[跨产品 AI 订阅付款排障决策树](https://he20000405-pixel.github.io/resources/ai-subscription-payment-troubleshooting/)。

## 官方资料

- [xAI: FAQ - Grok Website / Apps](https://docs.x.ai/grok/faq)
- [X Premium FAQ](https://help.x.com/en/using-x/x-premium-faq)
- [xAI Accounts](https://accounts.x.ai)

{% include faq.html %}
