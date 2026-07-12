# 2026 SuperGrok 国内充值指南：Grok User ID、支付宝微信与 Grok 4.5

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-在线阅读-111827)](https://he20000405-pixel.github.io/supergrok-china-guide/)
[![SuperGrok Recharge](https://img.shields.io/badge/chonggrok.com-SuperGrok%20充值-087f5b)](https://chonggrok.com/supergrok)

这是 **chonggrok.com 的 SuperGrok 充值与使用指南仓库**。主 README 负责长期常青的国内开通流程，`guides/` 持续收录 Grok User ID、付款失败、Grok Build 登录与 403、套餐选择、SuperGrok 与 X Premium+ 对比、Grok 4.5 更新等专题。

> **English summary:** A first-party service guide and independent knowledge base for SuperGrok subscription recharge in China. It covers Grok User ID, Alipay/WeChat payment, card-key redemption, payment troubleshooting, Grok Build login and 403 errors, and the Grok 4.5 update. ChongGrok is not affiliated with xAI or X.

**Keywords:** `SuperGrok China` · `Grok recharge` · `Grok User ID` · `Grok payment failed` · `Grok Build 403` · `Grok 4.5` · `chonggrok.com`

## 先说结论

- 有可用境外支付方式：可以直接尝试官方订阅，并按官方页面完成验证。
- 没有境外卡或反复付款失败：可使用 [chonggrok.com SuperGrok 充值页](https://chonggrok.com/supergrok)，支持支付宝/微信付款。
- chonggrok.com 的 Grok 充值只需要账号的 **Grok User ID**，不需要登录密码、邮箱验证码或恢复码。
- 账号始终归用户自己；升级完成后，应由用户回到 grok.com 检查订阅状态。
- User ID 虽不是密码，仍属于账号标识，应只在确认无误的核销页面提交。
- 任何线上订阅服务都不是零风险；本文不作“绝对安全”“100% 不封号”等承诺。

## chonggrok.com SuperGrok 充值流程

1. 打开 [https://chonggrok.com/supergrok](https://chonggrok.com/supergrok)。
2. 确认当前 Grok 账号可以正常登录，并选择主站实时展示的订阅周期。
3. 使用支付宝或微信付款，保存订单信息和卡密。
4. 打开 [https://chonggrok.com/verify](https://chonggrok.com/verify)，提交卡密并完成验证。
5. 按页面提示提交自己的 Grok User ID，核对账号后确认充值。
6. 等待系统处理，完成后回到 grok.com 验收订阅状态；如未刷新，退出后重新登录再检查。

![chonggrok.com SuperGrok 充值页](img/chonggrok-supergrok-home-hero-hd.png)

套餐和价格可能调整，本文不固定展示金额，请以下单页实时信息为准。

## Grok User ID 怎么找

1. 在浏览器登录 [grok.com](https://grok.com)。
2. 在同一浏览器打开 `https://grok.com/api/auth/session`。
3. 在返回的 JSON 中找到 `userId`，复制完整 UUID。
4. 不要把邮箱、X 用户名、昵称或 `xUserId` 当作 Grok User ID。

![Grok User ID 的虚构数据示意图](img/grok-user-id-json-example-hd.png)

上图仅为虚构数据示意，不包含真实用户信息。详细步骤见 [Grok User ID 查找与核对指南](guides/grok-user-id.md)。

## 充值方式对比

| 方式 | 适合谁 | 优点 | 需要注意 |
|---|---|---|---|
| 官方页面直接订阅 | 有稳定境外支付方式的用户 | 自己完成支付与续费 | 可能遇到卡片、3DS、账单地址或地区验证问题 |
| 应用商店订阅 | 熟悉对应商店账户的用户 | 对部分用户更方便 | 价格、退款、续费和权益同步以商店为准 |
| chonggrok.com 代充自己的账号 | 希望支付宝/微信付款的用户 | 不用密码，账号归自己，有售后对接 | 需准确提交 Grok User ID，线上服务非零风险 |

本仓库不推荐多人共享账号或成品号，也不提供 API 额度、接码或批量注册服务。

## 内容集群

| 专题 | 解决的问题 |
|---|---|
| [SuperGrok 自助充值完整流程](guides/supergrok-auto-recharge.md) | 从下单、卡密核销、User ID 到到账验收 |
| [Grok User ID 怎么找](guides/grok-user-id.md) | 找到正确的 `userId`，避免提交邮箱或 X 用户名 |
| [SuperGrok 1/2/3 个月怎么选](guides/supergrok-plans.md) | 按体验、工作流和项目周期选择 |
| [Grok 付款失败排查](guides/supergrok-payment-errors.md) | card declined、3DS、账单地址与权益未刷新 |
| [Grok Build 登录与 403 排查](guides/grok-build-login-403.md) | 浏览器授权、设备码、版本、旧会话与订阅权益 |
| [SuperGrok vs X Premium+](guides/supergrok-vs-x-premium-plus.md) | 按 Grok 与 X 的真实使用场景选择 |
| [Grok 4.5 更新说明](guides/grok-4-5-update.md) | 官方已确认能力、入口与 SuperGrok 可用性边界 |

## Grok 4.5：热点入口，订阅可用性需分开核实

xAI 于 **2026 年 7 月 8 日**发布 Grok 4.5，官方将其定位于编程、智能体任务和知识工作。发布页明确写到首发入口包括 Grok Build、Cursor 和 SpaceXAI console，但没有在该页明确承诺所有普通 grok.com / SuperGrok 账号都能立即在模型选择器看到 Grok 4.5。

因此，开通 SuperGrok 前应检查自己账号内的模型选择器和官方实时说明，不应把“购买 SuperGrok”理解为“保证立即获得 Grok 4.5”。详见 [Grok 4.5 更新与 SuperGrok 可用性说明](guides/grok-4-5-update.md)。

## 安全与业务边界

- 不需要 Grok 登录密码、邮箱验证码、短信验证码或恢复码。
- 只提交本次升级所需的 Grok User ID；账号和聊天数据仍由用户自己管理。
- 保存订单号、卡密、提交的 User ID 和核销状态，方便异常时追溯。
- 不承诺零风险、绝对安全、永久不封号或固定到账时间。
- 只做 ChatGPT、Grok、Claude、Gemini 的会员订阅代充；不做 API、成品号、接码或批量注册。
- ChongGrok 与 xAI、X 不存在隶属或官方合作关系。

## 主站深度资料

- [SuperGrok 充值完整教程](https://chonggrok.com/blog/supergrok-chongzhi-zhinan)
- [Grok User ID 怎么找](https://chonggrok.com/blog/grok-user-id-zenme-zhao)
- [SuperGrok 国内充值失败排查](https://chonggrok.com/blog/supergrok-payment-failed-ai-recharge-2026)
- [SuperGrok 安全充值检查清单](https://chonggrok.com/blog/supergrok-safe-recharge-checklist)
- [SuperGrok 套餐怎么选](https://chonggrok.com/blog/supergrok-taocan-zenme-xuan)
- [SuperGrok 与 X Premium+ 对比](https://chonggrok.com/blog/supergrok-vs-x-premium-plus)

## 官方参考

- [xAI: Grok 4.5](https://x.ai/news/grok-4-5)
- [Grok plans](https://grok.com/plans)

## 仓库入口

- GitHub Pages：<https://he20000405-pixel.github.io/supergrok-china-guide/>
- English guide：[README_EN.md](README_EN.md)
- 专题索引：[guides/](guides/)
- SuperGrok 充值：<https://chonggrok.com/supergrok>
- 卡密核销：<https://chonggrok.com/verify>
