---
title: "X 联合会员与 Grok Bot：套餐、每周额度和旧会员转换指南"
description: "区分 The X Subscription 四档、Grok Bot 资格、共享周额度与额外费用；说明旧会员官方转换、新购和旧版 SuperGrok 续费的不同路径。"
permalink: /guides/x-subscription-grok-bot-guide/
date_published: 2026-10-28
last_modified_at: 2026-10-28
breadcrumbs:
  - name: "首页"
    url: /
  - name: "专题"
    url: /guides/
  - name: "X 联合会员与 Grok Bot"
    url: /guides/x-subscription-grok-bot-guide/
faq:
  - question: "Plus 能用 Grok Bot 吗？"
    answer: "The X Subscription 的 Plus 不含 Grok Bot，Premium、Super、Ultra 包含。已有旧版 Cursor 付费套餐或符合条件的 SuperGrok/X Premium+ 绑定用户，应先检查原有 Bot 资格，不要直接重复购买。"
  - question: "ChongGrok 能把旧会员转换成 X 联合会员吗？"
    answer: "不能。ChongGrok 不办理旧会员转联合会员；需要转换的用户应使用官方 Unify 流程。本站联合会员新购和符合条件的旧版 SuperGrok 续费分别核对账号条件。"
  - question: "联合会员和旧版 SuperGrok 在哪里兑换？"
    answer: "已有相应卡密时，联合会员使用 chonggrok.com/verify-x，按该页要求提交 Grok SSO；旧版 SuperGrok 使用 chonggrok.com/verify-grok，提交卡密和 User ID。两类凭据不能互换。"
---

# X 联合会员与 Grok Bot：套餐、每周额度和旧会员转换指南

想用 Grok Bot，先分清自己是新购用户，还是已有旧会员。**The X Subscription 的 Premium 及以上包含 Grok Bot，Plus 不包含；已有旧版 Cursor 付费套餐或符合条件的 SuperGrok、X Premium+ 用户，则可能已有 Bot 资格，不一定需要重新购买。**

本文由 ChongGrok 维护，依据官方文档及本站服务页核查于 **2026 年 10 月 28 日**。这是规则与操作路径说明，未进行账号迁移、付费兑换或 Bot 任务实测。ChongGrok 是独立第三方服务，不是 xAI、X 或 Cursor 的官方授权销售方。

## 先按现有订阅选择路径

| 当前情况 | 先检查什么 | 下一步 |
|---|---|---|
| 没有付费订阅，准备使用 Grok、Cursor 或 X | 免费功能是否已够用，是否需要 Bot 或云端代理 | 比较下方联合会员档位 |
| 已有 Cursor Pro/Pro+/Ultra 或 SuperGrok、X Premium+ | 原账号是否已有 Bot 资格、每周用量及关联状态 | 先核对旧版权益，不因看到新名称重复购买 |
| 只准备续费旧版 SuperGrok | 账号是否仍符合旧版独立订阅条件 | 保留原体系，核对当前商品条件 |
| 已有旧会员，考虑合并账单 | 旧权益、第三方模型费用、原付款渠道及不可撤销条件 | 使用官方 Unify 流程；本站不办理转换 |
| 已扣款、卡密处理中或订阅未显示 | 原订单、当前账号及实际套餐 | 先看[付款后仍显示 Free]({{ '/guides/supergrok-paid-but-still-free/' | relative_url }})，不要再买一次 |

旧版 Cursor 付费套餐及符合条件的 SuperGrok/X Premium+ 关联仍有各自的 Bot 规则。旧版关联提供的是 Bot 用量资格，不等于获得 Cursor 订阅；关联与 Cursor 套餐的 Bot 用量不会相加。详见 [Cursor：Grok Bot 的套餐和账单](https://cursor.com/help/grok-bot/plans)。

## 四档联合会员如何选

The X Subscription 将 Grok、Cursor 与 X 放在一个订阅体系中。X 权益需要连接个人 X 账号，并按档位提供；不能理解为三份旧套餐的额度直接相加。

| 个人档位 | 官方月付标价 | 官方年付总额 | 包含用量，相对 Plus | Grok Bot |
|---|---|---|---|---|
| Plus | $8/月 | $80/年 | 基础量 | 不含 |
| Premium | $30/月 | $300/年 | 4 倍 | 包含 |
| Super | $100/月 | $1,000/年 | 15 倍 | 包含 |
| Ultra | $200/月 | $2,000/年 | 50 倍 | 包含 |

以上为官方美元标价，不含适用税费，不是 ChongGrok 人民币服务报价；付款以当时结账页为准。[官方定价说明](https://docs.x.ai/x-subscription/pricing)

- **只做轻量问答与编程：**可先比较免费方案及 Plus。Plus 支持规定范围的 Cursor 自有模型，但不含第三方模型、云端代理或 Grok Bot。
- **需要 Bot、云端代理或自动化：**新购联合会员从 Premium 开始比较。第三方模型可用，不代表费用已包含。
- **经常耗尽每周用量：**再根据实际用量考虑 Super 或 Ultra。更大额度不等于无限运行，也不能据此保证某个工作流能全天执行。

上述功能边界见 [Cursor：Models & Pricing](https://cursor.com/docs/models-and-pricing)。先记录自己的任务及用量，再决定是否升档；套餐倍数不是固定消息次数或任务数量。

## 每周额度池包含什么，在哪里看

联合会员每个付费席位有一个共享周额度池，符合条件的 Grok、Cursor 与 Grok Bot 第一方使用从中消耗。任务、模型和产品消耗不同；团队各席位有自己的周额度，不是全队共用一个无限池。[官方用量规则](https://docs.x.ai/x-subscription/usage-limits)

登录 [Grok Dashboard](https://grok.com/dashboard)，打开 **Usage**，检查已用量及下一次重置时间。核对当前工作区和账号，避免将另一个席位或旧账号的状态看成自己的余额。

额度用完后有三种选择：等待页面显示的重置时间、按需升级，或在官方账单页购买额外用量。额外用量会收费，先看预付余额、自动充值开关及月度额外消费上限。

Cursor 中的 Claude、GPT 等第三方模型不使用套餐包含的周额度，从首次请求开始按官方列出的价格另计；Grok API 也独立计费，不消耗订阅额度池。不要把“拥有 API 访问入口”当作“赠送 API 额度”。[Cursor 额外用量说明](https://cursor.com/docs/models-and-pricing)、[官方定价 FAQ](https://x.ai/pricing)

## 旧会员要不要转换：先核对四件事

转换是可选的，旧套餐可继续保留。完成 Unify 后不可撤销，官方支持也不能恢复原方案。转换前分别记录：

1. **已有权益：**旧套餐名称、用量规则、到期日，尤其是 Cursor 第三方模型的原有计费方式。
2. **要合并的账号：**登录准确的 Grok、Cursor 和 X 账号；邮箱不同不等于不能关联，关键是不要选错个人或工作账号。
3. **新方案的费用：**共享池覆盖什么、第三方模型是否另计、是否需要额外用量。
4. **原付款渠道：**网页、Apple 和 Google Play 的取消与退款处理不同。

确认后可按官方说明从 [Grok/X 的 Unify 入口](https://accounts.x.ai/unify) 或 [Cursor Unify](https://cursor.com/unify) 发起。**ChongGrok 不办理从旧会员转向联合会员；购买本站服务不是官方迁移流程中的一步。**

### 取消和退款不能一概而论

| 原订阅渠道 | 官方转换说明中的处理 |
|---|---|
| 符合条件的网页订阅 | 转换时取消所选旧订阅，并对未使用时间按规则退款；新订阅按新价格计费 |
| Cursor 的 Apple App Store 订阅 | 官方不能代为取消或退款；本人在 Apple 设置中取消，并向 Apple 申请退款 |
| Grok、Grok Bot 或 X Premium 的 Apple App Store 订阅 | 官方取消并向 Apple 请求未使用时间退款，退款由 Apple 决定 |
| Grok、Grok Bot 或 X Premium 的 Google Play 订阅 | 转换后在 Google Play 检查是否仍会续费；若仍续费，在该处取消 |
| 赠送的 X Premium 或 Apple 家庭共享 | 官方转换不会取消或退款这两类权益 |

以上依据 [官方 Unify 流程](https://docs.x.ai/x-subscription/unify-accounts)及 [Cursor App Store 说明](https://docs.x.ai/x-subscription/app-store)。不要先按旧文章取消全部订阅，再发现需要保留的权益已经改变。

## 国内支付协助：新购与旧版续费分开办理

官方可直接订阅。若考虑第三方协助，先了解政策与服务条件：[官方购买 FAQ](https://x.ai/pricing)明确未授权第三方销售，其他来源购买的订阅存在账号被暂停或终止的风险。ChongGrok 提供的支付方式和办理说明属于本站服务信息，不是厂商认可或安全保证。

本站当前页面分别展示：

| 本次需求 | 付款前查看 | 已有对应卡密后的兑换入口 |
|---|---|---|
| X 联合会员新购 | [联合会员服务页](https://chonggrok.com/x-subscription?utm_source=github_guides&utm_medium=referral&utm_campaign=x_subscription_grok_bot&utm_content=new_plan)：核对档位、账号资格、交付、办理时间与售后 | [联合会员兑换](https://chonggrok.com/verify-x?utm_source=github_guides&utm_medium=referral&utm_campaign=x_subscription_grok_bot&utm_content=redeem_x)，页面要求卡密及 Grok SSO |
| 符合条件的旧版 SuperGrok 续费 | [旧版 SuperGrok 服务页](https://chonggrok.com/supergrok?utm_source=github_guides&utm_medium=referral&utm_campaign=x_subscription_grok_bot&utm_content=legacy_plan)：核对旧版资格及 1 个月/3 个月商品 | [旧版 Grok 兑换](https://chonggrok.com/verify-grok?utm_source=github_guides&utm_medium=referral&utm_campaign=x_subscription_grok_bot&utm_content=redeem_legacy)，页面要求卡密及 User ID |

本站页面说明支持支付宝/微信。付款前仍需确认对应商品条件；不能由“支持四个档位”推断所有账号都可以办理。

**两种凭据不能混用。**旧版 User ID 是账号标识；联合会员页面要求的 SSO 是临时登录凭证，涉及账号访问权限。不要在聊天、公开评论或截图中发送 SSO，不要把完整会话内容当作 User ID 提交。需要提供哪些资料应以对应兑换页为准；不提供密码不等于没有风险。

## 完成后怎样验收

- **联合会员：**在 Grok Dashboard 核对套餐、有效期、工作区和 Usage，再分别检查对应 Cursor 功能及个人 X 绑定权益。需要 Bot 的 Premium 及以上用户，再检查 Bot 使用权限。
- **旧版续费：**回原 Grok 账号核对旧套餐和有效期；旧版充值不会自动变成联合会员。
- **结果不一致：**保留订单号与已遮挡凭据的截图，先查询原订单并联系对应服务方，不重复提交、不重复付款。办理时间按原订单约定，不自行假设统一到账时限。

登录或 403 问题请继续阅读 [Grok Build 登录排查]({{ '/guides/grok-build-login-403/' | relative_url }})；套餐有效但功能受限可看[周额度与订阅状态的区别]({{ '/guides/supergrok-weekly-limit-vs-subscription/' | relative_url }})。

{% include faq.html %}