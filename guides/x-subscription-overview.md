---
title: "Grok 联合会员（The X Subscription）怎么选？2026 四档价格、Grok Bot 权限与国内开通指南"
description: "2026年10月最新实测：详解 xAI 新版 The X Subscription 联合会员 Plus ($8)、Premium ($30)、Super ($100)、Ultra ($200) 四档差异，对比新版联合会员与旧版 SuperGrok 选型，附国内通过 chonggrok.com 支付宝/微信本号升级与 UID 免密核销全流程。"
permalink: /guides/x-subscription-overview/
date: 2026-10-28
last_modified_at: 2026-10-28
---

# Grok 联合会员（The X Subscription）怎么选？2026 四档价格、Grok Bot 权限与国内开通指南

**直接结论：** xAI 已于 2026 年 10 月正式推出 **The X Subscription（X 联合会员 / X 联合订阅）**，首次将 **Grok、Grok Bot、Cursor 与 X Premium** 四大产品整合为四档计费方案（Plus $8 / Premium $30 / Super $100 / Ultra $200）。其中 **$8/月的 Plus 档位完全不包含 Grok Bot 权限**，需要使用 Grok Bot 云端自动化任务的用户，必须开通 **Premium（$30/月）** 及以上档位。国内用户若没有境外信用卡或遇到 Stripe 绑卡被拒（`Card declined`），可通过独立订阅协助平台 **[ChongGrok (chonggrok.com)](https://chonggrok.com)** 使用支付宝或微信完成个人原账号升级，并在 **[chonggrok.com/verify](https://chonggrok.com/verify)** 自助核销，最后回到 `grok.com` 官方后台验收订阅状态。

---

## 一、 新版 Grok 联合会员（The X Subscription）4 个档位有什么区别？

新版联合会员取消了此前多项产品各自独立计费的模式，改为由 Grok 对话生图、Grok Bot 任务与 Cursor 编码共用同一个每 7 天自动刷新的 **每周共享额度池（`Weekly usage limit` / Weekly Pool）**。不同档位对 Grok Bot 和 Cursor 的权限限制差异极大，购买前请先对照下表：

| 套餐档位    | 官方月费（年付价）     | 每周共享额度池 | Grok Bot 权限                   | Cursor 编辑器权限边界                                 | X (Twitter) 平台权益           | 适用人群与选型结论                                           |
| :---------- | :--------------------- | :------------- | :------------------------------ | :---------------------------------------------------- | :----------------------------- | :----------------------------------------------------------- |
| **Plus**    | $8 / 月（$80/年）      | **1x 基础池**  | **不支持（无权限）**            | 仅限调用 Grok 自家模型                                | 蓝标认证、时间线广告减半       | 仅适合日常轻度问答与刷 X，**需要使用 Grok Bot 的用户切勿误选此档** |
| **Premium** | $30 / 月（$300/年）    | **4x 额度池**  | **完整支持（含云端环境）**      | 支持云端 Agent 与代码审查（Claude/GPT 按 API 价另计） | 完整 X Premium+ 权益（免广告） | **90% 用户的性价比首选**，将原总价 $90/月的三大核心会员打包整合 |
| **Super**   | $100 / 月（$1,000/年） | **15x 额度池** | **完整支持 + 高峰优先调度**     | 完整可用 + 15 倍大容量第一方模型额度池                | 完整 X Premium+ 顶级权益       | 适合每天高频挂机运行 Grok Bot 自动化工作流与重度编码的开发者 |
| **Ultra**   | $200 / 月（$2,000/年） | **50x 额度池** | **完整支持 + 新功能最优先体验** | 完整可用 + 50 倍超大额度池                            | 完整 X Premium+ 顶级权益       | 适合将 Grok Bot 与 Cursor 作为全天候主力生产流水线的极客与团队 |

> **选型与开通提示：** 如需在国内免境外卡直接开通支持 Grok Bot 的 **Premium（$30/月）** 或更高档位，可直接在 **[chonggrok.com](https://chonggrok.com)** 选择对应档位完成个人原账号升级；若开通后遇到 Grok Bot 权限或额度池疑问，请延伸阅读 [Grok Bot 权限解锁与每周额度池（Weekly Pool）指南](https://he20000405-pixel.github.io/supergrok-china-guide/guides/grok-bot-weekly-pool-guide/)。

---

## 二、 该开「新版 X 联合会员」还是充「旧版 SuperGrok」？

xAI 官方目前并未强制取消存量用户的旧版独立套餐。在 **[chonggrok.com](https://chonggrok.com)** 与 **[chonggrok.com/supergrok](https://chonggrok.com/supergrok)** 页面中，目前同时提供「新版 X 联合会员」与「旧版 SuperGrok 独立充值」两条通道。下单前请对照下表判断自己适合哪一种：

| 对比维度               | 方案 A：新版 X 联合会员（The X Subscription）                | 方案 B：旧版 SuperGrok 独立充值                              |
| :--------------------- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| **包含的产品范围**     | 一份账单同时打包 **Grok + Grok Bot + Cursor + X Premium+**（需选 Premium $30 档及以上） | 仅包含 **`grok.com` 核心模型权益**（Grok 4.5、DeepSearch、生图与语音），不含 Cursor 与 X 蓝标 |
| **适合什么账号状态**   | 目前处于 `Free` 免费状态的新老账号，或决定将多端账单合并管理的用户 | 账号符合旧版 SuperGrok 独立续费资格，且不希望改动现有独立账单结构的老用户 |
| **国内核销所需资料**   | 在 `chonggrok.com/verify` 按 X 联合会员兑换通道指引完成本号校验升级 | **仅需提交「卡密 + Grok User ID」**，全程不需要提供登录密码、邮箱验证码或恢复码 |
| **可选周期与退回限制** | 按月或按年订阅；**一旦将旧版账号合并（Unify）至新版联合会员，永久不可逆，无法退回旧版** | 支持按 **1 个月或 3 个月** 周期灵活充值，保留原有独立订阅规则 |

如果只需要单独使用 Grok 模型且希望用 User ID 免密续期，可结合 [SuperGrok 套餐怎么选](https://he20000405-pixel.github.io/supergrok-china-guide/) 与 [Grok User ID 怎么找](https://he20000405-pixel.github.io/supergrok-china-guide/guides/grok-user-id/) 准备资料。

---

## 三、 下单前先检查

| 检查项             | 正确状态                                                     |
| :----------------- | :----------------------------------------------------------- |
| **账号登录状态**   | 可以正常打开并登录 `grok.com`，确认当前浏览器登录的是准备升级的目标账号 |
| **套餐与档位选择** | 已分清本次要买的是「新版 X 联合会员（需用 Grok Bot 必选 Premium $30 档及以上）」还是「旧版 SuperGrok」 |
| **核销凭证准备**   | 能按照 `chonggrok.com/verify` 当前页面说明准备最小必要标识（如旧版 SuperGrok 仅需 Grok User ID） |
| **安全边界确认**   | 明确不会向任何人提交账号登录密码、邮箱验证码或两步验证恢复码 |
| **订单记录留存**   | 准备好保存订单号、卡密（Card Key）、付款时间和核销状态截图   |

如果账号无法正常登录，或打开网页时提示 `403 Forbidden`，请先按 [Grok Build 登录与 403 排查](https://he20000405-pixel.github.io/supergrok-china-guide/guides/grok-build-login-403/) 解决账号访问问题后再下单。

---

## 四、 国内如何免境外卡开通 Grok 联合会员与 SuperGrok？（6 步完整流程）

针对国内没有境外 Visa/MasterCard 信用卡，或在 Stripe 支付页反复遇到 `Your card was declined`、账单地址不匹配、3DS 验证失败的用户，可按以下 6 步通过支付宝或微信完成本号升级：

### 第一步：进入 ChongGrok 服务页确认实时方案
打开 **[https://chonggrok.com](https://chonggrok.com)** 或 Grok 专项服务页 **[https://chonggrok.com/supergrok](https://chonggrok.com/supergrok)**，查看「新版 X 联合会员」各档位或「旧版 SuperGrok」的当前可选周期与实时价格。
由于跨境结算汇率与通道成本可能动态调整，本指南不固定写死人民币价格，请以服务页实时展示的金额为准。

### 第二步：选择目标档位并完成支付宝/微信付款
根据实际用途选择对应套餐（如为了使用 Grok Bot 与 Cursor，请认准 **Premium $30 档** 或以上；如仅需单充旧版，请选择对应月数），使用支付宝或微信完成付款。
付款完成后，请立即保存：
* 订单号；
* 卡密（Card Key）；
* 付款时间与所购套餐名称截图。

### 第三步：进入官方核销页验证卡密
在浏览器打开核销通道 **[https://chonggrok.com/verify](https://chonggrok.com/verify)**，根据购买的产品类型选择对应的兑换入口（新版 X 联合会员兑换或旧版 Grok 卡密核销），粘贴卡密并点击验证。
卡密是唯一兑付凭证，请勿在公开社区或群聊中泄露截图。

### 第四步：按核销页说明提交最小必要标识
确保浏览器已登录你本人要升级的 Grok 目标账号，按照核销页当前显示的指引提交信息：
* **办理「旧版 SuperGrok」：** 仅提交页面明确要求的 **Grok User ID**（准确获取与脱敏核对见 [Grok User ID 怎么找](https://he20000405-pixel.github.io/supergrok-china-guide/guides/grok-user-id/)），不要把注册邮箱、昵称、X 用户名或密码填进去。如果页面说明与本文不一致，或你不理解当前页面要求提交哪一项，应立即停止操作并联系售后客服确认。
* **办理「新版 X 联合会员」：** 按核销页当前提示完成个人原号校验或配合客服完成订阅写入。

### 第五步：核对目标账号信息并确认提交
核销系统识别出待充值账号信息后，请再次核对该账号确实是你本人的目标账号，确认无误后点击提交升级。若识别出的账号与预期不符，请立即停止提交并检查浏览器是否登错了小号。

### 第六步：回到 grok.com 官方后台验收订阅状态
核销提示完成后，返回 `grok.com`（或直接访问账单面板 `grok.com/dashboard/billing`）：
* 检查页面显示的订阅档位标识（如 `Premium`、`Super` 或 `SuperGrok`）是否已更新；
* 检查 `Usage` 页面的每周额度池（`Weekly usage limit`）以及 Grok Bot / 高阶模型入口是否已解锁；
* 若页面仍显示旧状态，请先退出账号（Log out）再重新登录刷新一次令牌；
* 若重新登录后仍显示 `Free`、`Activate` 或 `Upgrade`，**切勿重复下单付款**，请保留订单号与核销截图，直接对照 [付款成功但仍显示 Free 排查](https://he20000405-pixel.github.io/supergrok-china-guide/) 核实或联系售后处理。

---

## 五、 风险与业务边界说明

* **坚持自有原账号升级：** ChatGPT、Grok、Claude 均只为用户自有的个人原账号办理会员订阅升级（全站仅 Gemini 另有一年成品账号这一项专属业务例外），不做多人共享合租号，升级后聊天记录与工作流完全归用户个人掌控。
* **最小化凭证与安全边界：** 旧版 SuperGrok 充值仅需 Grok User ID，不要求提供登录密码、邮箱验证码或恢复码。不要求密码能显著减少账号暴露面，但任何第三方线上协助服务都不等于绝对零风险，请仅在核实无误的 `chonggrok.com/verify` 页面提交信息。
* **不做 API 与灰黑产业务：** 本知识库与 `chonggrok.com` 仅处理消费者端的正版会员订阅服务，不售卖 API 充值额度、不提供手机接码或批量注册服务。
* **诚实履约预期：** 受官方账单同步机制影响，本文不作“固定几秒必到账”或“100% 永不风控”等夸大承诺，所有订单均以官方后台最终验收状态为准。
* **独立第三方声明：** ChongGrok (`chonggrok.com`) 是独立的第三方会员订阅充值服务网站，与 xAI、Grok、X、Cursor 或 OpenAI 不存在隶属、官方授权或合作关系。

---

## 六、 常见问题解答（FAQ）

### Grok 联合会员（The X Subscription）8 刀的 Plus 档可以使用 Grok Bot 吗？
不能。根据 xAI 官方规则，$8/月的 Plus 档位仅包含基础版 Grok 对话和仅限调用 Grok 自家模型的受限版 Cursor，完全不包含 Grok Bot 权限。需要使用 Grok Bot 云端自动化任务的用户，必须开通 **Premium（$30/月）**、**Super（$100/月）** 或 **Ultra（$200/月）** 档位。

### 国内没有海外信用卡，在 Grok 官网绑卡提示 card declined 怎么办？
国内发行的双币卡在 Stripe 支付网关常因发卡行拒付、账单地址不匹配或 3DS 验证失败被拦截（具体原因排查见 [Grok / SuperGrok 付款失败排查](https://he20000405-pixel.github.io/supergrok-china-guide/guides/supergrok-payment-errors/)）。若不想折腾海外虚拟卡，可直接通过 `chonggrok.com` 使用支付宝或微信为自己的个人原账号开通 X 联合会员或充值旧版 SuperGrok。

### 老版本的 SuperGrok 账号一旦合并（Unify）到新版 X 联合会员，还能退回旧版吗？
不能。通过官方入口（`accounts.x.ai/unify` 或 `cursor.com/unify`）将旧版独立订阅合并升级为新版 X 联合会员的操作是**永久不可逆**的，联系官方客服也无法撤销。如果你只需要单用 Grok 且想保留旧版独立计费，请勿点击合并，直接在 `chonggrok.com` 选择旧版 SuperGrok 通道凭 User ID 续期即可。

### 在 chonggrok.com 充值 Grok 会员需要提供账号密码吗？
办理旧版 SuperGrok 独立充值时，全程只需提交卡密与 Grok User ID，不需要提供账号登录密码、邮箱验证码或恢复码；办理新版 X 联合会员时，也仅需按 `chonggrok.com/verify` 页面说明完成最小化核销校验，切勿向任何人透露明文密码。

---

## 七、 参考资料与关联排障专题

* **Grok 知识库核心专题：**
  * [Grok Bot 权限解锁与每周额度池（Weekly Pool）指南](https://he20000405-pixel.github.io/supergrok-china-guide/guides/grok-bot-weekly-pool-guide/)
  * [SuperGrok 国内自助充值教程](https://he20000405-pixel.github.io/supergrok-china-guide/guides/supergrok-auto-recharge/)
  * [Grok User ID 怎么找：userId 获取与核对说明](https://he20000405-pixel.github.io/supergrok-china-guide/guides/grok-user-id/)
  * [Grok / SuperGrok 付款失败：card declined 与 3DS 排查](https://he20000405-pixel.github.io/supergrok-china-guide/guides/supergrok-payment-errors/)
  * [Grok Build 登录失败与 403 排查](https://he20000405-pixel.github.io/supergrok-china-guide/guides/grok-build-login-403/)
  * [Grok 4.5 更新内容与可用性说明](https://he20000405-pixel.github.io/supergrok-china-guide/guides/grok-4-5-update/)
  * [ChongGrok AI 会员指南总门户 (guides.chonggrok.com)](https://guides.chonggrok.com/)
* **ChongGrok 主站入口：**
  * [ChongGrok 主站首页 (https://chonggrok.com)](https://chonggrok.com/)
  * [ChongGrok SuperGrok 与联合会员专区 (https://chonggrok.com/supergrok)](https://chonggrok.com/supergrok)
  * [ChongGrok 卡密与会员自助核销页 (https://chonggrok.com/verify)](https://chonggrok.com/verify)
* **官方参考资料：**
  * xAI Consumer FAQ & The X Subscription Billing Documentation
  * Grok Billing & Plans (`grok.com/dashboard/billing`)

*事实与流程核验日期：2026-10-28。ChongGrok is not affiliated with xAI, X, or Cursor.*
*Keywords: Grok 联合会员 · The X Subscription · X 联合订阅 · Grok Bot 怎么开通 · SuperGrok 国内充值 · Grok User ID 免密充值 · Grok 绑卡被拒 card declined · chonggrok.com*