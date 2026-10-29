---
title: "老版 SuperGrok 与 Cursor 要不要合并（Unify）？2026 X 联合会员迁移避坑、苹果退费与旧版保留指南"
description: "2026年10月最新实测：详解 xAI 与 Cursor 账号合并（accounts.x.ai/unify）的永久不可逆规则、Apple App Store 与 Google Play 退费差异，对比保留旧版独立订阅与升级新版 X 联合会员的利弊，附国内通过 chonggrok.com 续费旧版 SuperGrok 或开通新版 X 联合会员的流程。"
permalink: /guides/supergrok-unify-migration-guide/
date: 2026-10-28
last_modified_at: 2026-10-29
---

# 老版 SuperGrok 与 Cursor 要不要合并（Unify）？2026 X 联合会员迁移避坑、苹果退费与旧版保留指南

**直接结论：** xAI 与 Cursor 推出的账号合并功能（[accounts.x.ai/unify](https://accounts.x.ai/unify) 或 [cursor.com/unify](https://cursor.com/unify)）是**完全自愿且永久不可逆**的。一旦将现有的旧版 SuperGrok 或旧版 Cursor Pro 合并升级为新版 **The X Subscription（X 联合会员）**，**永久无法退回旧版独立套餐，联系官方客服也无法撤销**。如果你重度依赖旧版 Cursor Pro 套餐内赠送的 Claude / GPT 固定额度，或平时只需要单用 `grok.com` 对话与生图功能，**请勿点击合并**，可直接在 **[ChongGrok 旧版 SuperGrok 订阅页](https://chonggrok.com/supergrok)** 选择「旧版 SuperGrok」通道，仅凭 **Grok User ID + 卡密** 完成免密续期；如果你希望用一份账单同时解锁 **Grok + Grok Bot + Cursor + X Premium+**，则可通过 **[ChongGrok X 联合会员订阅页](https://chonggrok.com/x-subscription)** 核对账号条件并开通新版 X 联合会员（需使用 Grok Bot 请必选 **Premium $30/月** 及以上档位）。**ChongGrok 不办理旧会员转换；已有 SuperGrok 或 Cursor 订阅需要合并（Unify）时，请按[官方合并指南](https://docs.x.ai/x-subscription/unify-accounts)操作。**

---

## 一、 老版 SuperGrok 和 Cursor Pro 合并（Unify）后会发生什么？（5 条不可逆规则）

当你在 `grok.com` 账单页或 Cursor 设置中点击 `Unify`（合并账户）并完成结账后，你的账号底层结构将发生以下 5 项永久性变更：

| 变更维度                           | 合并前（旧版 SuperGrok / 旧版 Cursor Pro 独立订阅）          | 合并后（The X Subscription 联合会员统一订阅）                |
| :--------------------------------- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| **1. 是否支持回退旧套餐**          | 可保持原独立价格、原周期与原权益继续续费                     | **永久不可逆（Permanent）**，一旦完成合并无法退回旧版，官方客服也无法撤销 |
| **2. 账单与额度管理入口**          | Grok 与 Cursor 各自在独立后台出账、分开管理额度              | 合并为单一工作空间与单一账单，统一在 **[grok.com/dashboard](https://grok.com/dashboard)** 管理订阅、用量与预充值 |
| **3. Cursor 内 Claude / GPT 计费** | 旧版 Cursor Pro 用户在未合并前，可继续使用旧套餐内包含的第三方模型额度 | **每周共享额度池仅包 xAI 第一方模型**；在 Cursor 中调用 Claude 或 GPT 从第 1 次起直接按 API 目录价扣预充值余额 |
| **4. 多个 Cursor 账号的处理**      | 以前因配合 SuperGrok 与 Grok Bot 可能存在多个关联账号        | 合并时需指定一个**主账号（Primary Cursor Account）**，其余关联账号将被合并至主账号下 |
| **5. 账单周期与旧余额结算**        | 按各自原有的月度或季度到期日独立结算                         | **合并当天立即开启全新的计费周期**；原网页端未用完的时长将按比例折算退费（Apple 内购除外） |

> **选型与续费提示：** 如果看完上述规则后，你决定保留旧版 SuperGrok 不合并，可通过 **[旧版 SuperGrok 订阅页](https://chonggrok.com/supergrok)** 使用支付宝或微信付款，并在 **[旧版 Grok 核销页](https://chonggrok.com/verify-grok)** 完成核销；如果希望直接将免费账号升级为新版 X 联合会员，可通过 **[X 联合会员订阅页](https://chonggrok.com/x-subscription)** 使用支付宝或微信付款，并在 **[X 联合会员核销页](https://chonggrok.com/verify-x)** 完成兑换。

---

## 二、 哪些人千万别点合并（Unify）？哪些人适合立刻合并升级？

官方明确说明：切换至 The X Subscription 是可选操作（Optional），不主动切换的老用户可继续沿用现有计划。在操作前，请先对照以下分流标准判断：

### 1. 建议「停止合并、保留旧版独立订阅」的 3 类用户
* **主力使用 Claude / GPT 写代码的旧版 Cursor Pro 用户：** 旧版 $20/月的 Cursor Pro 包含一定额度的第三方模型调用；一旦合并到新版 X 联合会员，即便开通 $30 的 Premium 或 $100 的 Super 档位，扩大也只是 Grok 第一方模型的每周额度池（详见 [X 联合会员下使用 Cursor 编程的计费规则](https://he20000405-pixel.github.io/supergrok-china-guide/guides/grok-cursor-shared-billing/)），Claude 和 GPT 将全部变为额外按量扣费。
* **仅使用 `grok.com` 对话、DeepSearch 与生图的纯 Grok 用户：** 如果你完全不用 Cursor 写代码，也不需要运行 Grok Bot 自动化脚本，保留旧版 SuperGrok 独立订阅（支持在 **[chonggrok.com/supergrok](https://chonggrok.com/supergrok)** 按 1 个月或 3 个月周期凭 **Grok User ID** 免密充值）在操作上更轻量，无需改动现有账号绑定关系。
* **一个账号属于个人、另一个账号属于团队（Team）的用户：** 个人计划与团队计划必须分开独立合并（个人走 [cursor.com/unify](https://cursor.com/unify)，团队管理员走 [cursor.com/unify/team](https://cursor.com/unify/team)），不能将个人号与团队号混同合并。

### 2. 建议「直接开通或合并升级新版 X 联合会员」的 3 类用户
* **需要使用 Grok Bot 云端自动化任务的用户：** 新体系下 Grok Bot 已不再支持通过单买 Cursor Pro 解锁，必须使用 **X 联合会员 — Premium（$30/月）** 及以上档位（详见 [为什么开了会员还是用不了 Grok Bot](https://he20000405-pixel.github.io/supergrok-china-guide/guides/grok-bot-weekly-pool-guide/)）。
* **同时重度使用 Grok + Cursor + X Premium+ 的全栈用户：** 以前分开订阅三项服务每月合计需约 $90，合并至 **Premium（$30/月）** 档位后可直接打包全部权益，并获得 4 倍每周共享额度池（四档完整对比见 [Grok 联合会员怎么选](https://he20000405-pixel.github.io/supergrok-china-guide/guides/x-subscription-overview/)）。
* **当前处于 Free 免费状态的新订阅用户：** 新用户目前已无旧版独立套餐入口，直接从新版 X 联合会员起步即可。

---

## 三、 原订阅走苹果 App Store 或 Google Play，合并时怎么防止双边扣费？

这是老用户合并时最容易发生资金损失的环节。**不同支付渠道的原订阅，在合并（Unify）时的自动取消与退费规则完全不同**，请务必对照下表核查你的原付款渠道：

| 你原有的订阅产品与付款渠道                                   | 网页端合并（Unify）时系统会自动取消旧账单吗？ | 剩余未用完时长的退费规则                                     | 用户必须手动执行的操作                                       |
| :----------------------------------------------------------- | :-------------------------------------------- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| **网页端（Stripe 信用卡/直充）的 Grok、Cursor 或 X Premium** | ✅ **会自动取消**                              | 系统自动按未使用天数比例（Prorated）原路退回或在结账时抵扣   | 无需手动取消；若原 Cursor 账户有余额（Credit balance），结账后会先抵扣新账单并将剩余额度结转至联合会员 |
| **通过 Apple App Store（iPhone / iPad）内购的 Cursor 订阅**  | ❌ **完全无法自动取消**                        | 网页端无法退还苹果内购费用                                   | **合并后必须立即在 iPhone / iPad「设置 -> Apple ID -> 订阅」中[手动取消 Cursor 订阅](https://support.apple.com/zh-cn/118428)**，并向 Apple [申请退费](https://support.apple.com/zh-cn/118223)，否则苹果会继续每个月扣你的钱 |
| **通过 Apple App Store 内购的 Grok、Grok Bot 或 X Premium**  | ⚠️ **系统会代为取消并向苹果发起退费请求**      | **由 Apple 决定最终是否退费及退费金额**；若苹果拒绝退费，旧订阅不再续期并保留至原周期结束 | 建议合并后同步检查 iOS「设置 -> 订阅」列表，确认续费状态已关闭 |
| **通过 Google Play 内购的 Grok、Grok Bot 或 X Premium**      | ⚠️ **部分需手动核验**                          | 按平台结算规则处理                                           | **合并完成后必须打开 Google Play「付款和订阅」检查**，若仍显示自动续订，需手动点击取消 |
| **好友赠送的 X Premium（Gifted）或苹果家庭共享（Family Sharing）** | ❌ **不会取消**                                | **不支持任何退费或抵扣**                                     | 合并后直接被新版 X 联合会员权益覆盖，原赠送时长不退费        |

> **特殊状态提醒（Legacy Request-Based Cursor）：** 如果你的旧版个人 Cursor 账号仍处于早期的“按请求次数计费（Legacy request-based plan）”模式，直接访问合并页会报错。你必须先登录 Cursor 仪表盘点击 **`Opt In to New Pricing`** 切换为按量计费后，才能执行合并。

---

## 四、 决定保留旧版或合并升级前先检查

在动手点击官方合并按钮或前往 **[chonggrok.com](https://chonggrok.com)** 下单前，请逐项核对以下清单：

| 检查项                    | 正确状态与停止条件                                           |
| :------------------------ | :----------------------------------------------------------- |
| **1. 明确不可逆后果**     | 已清楚一旦合并为 X 联合会员就**永远无法退回旧版独立套餐**；若仍想保留旧版 Cursor 的 Claude/GPT 赠送额度，**请立即停止合并** |
| **2. 核查原付款渠道**     | 已查清旧订阅是网页端付款还是 Apple App Store / Google Play 内购；若是苹果内购的 Cursor，已准备好手动去 iOS 设置里关停续费 |
| **3. 确认主账号归属**     | 若手头有多个 Cursor 账号，已确认好把哪一个设为主账号（Primary Account）；若要绑定个人 X 账号领蓝标，确认该 X 账号未绑定过其他 Grok 账号（每个 X 账号仅限绑定一个 Grok 账号） |
| **4. 准备好对应核销标识** | 若在 [旧版 SuperGrok 订阅页](https://chonggrok.com/supergrok)选择续费「旧版 SuperGrok」，已提前按 [Grok User ID 怎么找](https://he20000405-pixel.github.io/supergrok-china-guide/guides/grok-user-id/)准备好 User ID；若选择开通「新版 X 联合会员」，已确认目标档位（需用 Grok Bot 必选 Premium $30 档及以上），并了解需在 [X 联合会员核销页](https://chonggrok.com/verify-x)按指引提交对应卡密和 Grok SSO |
| **5. 严守密码安全边界**   | 明确不会向任何人提供登录密码、邮箱验证码或恢复码，并准备好保存订单号与卡密截图 |

---

## 五、 国内如何免境外卡续费「旧版 SuperGrok」或开通「新版 X 联合会员」？

无论你最终决定**不合并（继续单充旧版 SuperGrok）**，还是决定**直接开通新版 X 联合会员**，若遇到国内银行卡被 Stripe 拒付（`Card declined`，详见 [Grok 付款失败排查](https://he20000405-pixel.github.io/supergrok-china-guide/guides/supergrok-payment-errors/)），均可按以下双轨流程通过支付宝或微信办理。**以下流程不用于旧会员 Unify 转换；已有订阅需要合并时，请按[官方合并指南](https://docs.x.ai/x-subscription/unify-accounts)操作。**

### 路径一：不合并老账号，仅凭 User ID 免密续费「旧版 SuperGrok」
1. **选择旧版方案：** 打开 **[https://chonggrok.com/supergrok](https://chonggrok.com/supergrok)**（或主站 **[https://chonggrok.com](https://chonggrok.com)**），在旧版 SuperGrok 专区按实时页面展示选择 1 个月或 3 个月周期（价格随汇率动态调整，本文不固定写死人民币价格），使用支付宝或微信完成付款并保存卡密。
2. **提交 User ID 核销：** 登录 `grok.com` 确认目标账号无误后，打开 **[https://chonggrok.com/verify-grok](https://chonggrok.com/verify-grok)** 进入旧版 Grok 卡密核销页面，**仅提交「卡密 + Grok User ID」**（无需登录密码或验证码，详细步骤见 [SuperGrok 国内自助充值教程](https://he20000405-pixel.github.io/supergrok-china-guide/guides/supergrok-auto-recharge/)）。
3. **官方页面验收：** 核销完成后返回 `grok.com` 刷新检查会员状态。

### 路径二：直接开通或升级「新版 X 联合会员（The X Subscription）」
1. **选择联合会员档位：** 打开 **[https://chonggrok.com/x-subscription](https://chonggrok.com/x-subscription)**，在「X 联合会员」专区选择目标档位（需要使用 Grok Bot 请选择 **Premium $30 档**、Super $100 档或 Ultra $200 档），完成支付宝或微信付款并保存订单号与卡密。
2. **完成本号兑换：** 进入 **[https://chonggrok.com/verify-x](https://chonggrok.com/verify-x)**，验证对应卡密，再按页面说明填写目标 Grok 账号的 SSO 并提交，随后查看处理结果。SSO 的获取方式以该页图文说明为准。**SSO 属于敏感登录凭据，不要发送到客服聊天或公开页面。**
3. **统一后台验收：** 升级完成后，前往 [grok.com/dashboard/billing](https://grok.com/dashboard/billing)确认订阅档位，再从 [grok.com/dashboard](https://grok.com/dashboard)侧栏进入 **Usage（用量）** 查看每周额度池状态。若页面仍显示 `Free`，请勿重复付款，按 [付款成功但仍显示 Free 排查](https://he20000405-pixel.github.io/supergrok-china-guide/guides/supergrok-paid-but-still-free/)核实。

---

## 六、 风险与业务边界说明

* **坚持自有原账号升级：** ChatGPT、Grok、Claude 均只做用户自有原账号的会员订阅升级（全站仅 Gemini 另有一年成品账号这一项专属业务例外），绝不售卖多人共享合租号，账号与数据归用户个人独立管理。
* **最小化凭证与安全意识：** 旧版 SuperGrok 充值使用 [旧版 Grok 核销页](https://chonggrok.com/verify-grok)，提交卡密与 Grok User ID；X 联合会员使用 [联合会员核销页](https://chonggrok.com/verify-x)，按页面指引提交对应卡密与 Grok SSO。User ID 是账号标识，SSO 是敏感登录凭据，两者不能混用。不需要提交登录密码、短信/邮箱验证码或恢复码。不要求密码能减少不必要的账号暴露，但不等于绝对零风险；请只在确认无误的对应核销页面提交信息，不要向客服聊天或公开页面发送 SSO。
* **不做 API 与违规业务：** 全站只处理消费者会员订阅，不提供 API 额度充值、接码或批量注册服务。
* **独立第三方声明：** ChongGrok (`chonggrok.com`) 是独立的第三方会员订阅充值服务网站，与 xAI、Grok、X、Cursor 或 OpenAI 不存在隶属、官方授权或合作关系。

---

## 七、 常见问题解答（FAQ）

### 我手头既有旧版 SuperGrok 又有旧版 Cursor Pro，合并应该从哪个入口发起？
官方支持从两个入口发起：若从 Grok 或 X 侧开始，可访问 [accounts.x.ai/unify](https://accounts.x.ai/unify)（或在 `grok.com` 进入 `Settings › Billing` 点击 `Get started`）；若你当前持有付费的 Cursor 计划，官方建议优先从 Cursor 侧入口 [cursor.com/unify](https://cursor.com/unify)发起合并，并按提示登录要绑定的 Grok 与个人 X 账号。

### 我不小心把旧版 Cursor Pro 合并成了 X 联合会员，发现 Claude 模型要额外扣费，能找客服退回旧版吗？
不能。xAI 与 Cursor 官方文档明确声明：账号合并一旦完成即永久生效（Permanent），无法自行撤销，联系官方客服（Support）也无法帮你回退到旧版独立套餐。如果需要使用 Claude 编程且不想按 API 计费，可考虑在 [ChongGrok Claude Pro 订阅页](https://chonggrok.com/claude)单独配置 Claude Pro 会员搭配使用。

### 以前为了用 Grok Bot 搞出了两个 Cursor 账号，合并时代码配置和额度怎么处理？
在执行 `unify` 合并流程时，系统会允许你登录并添加多个符合条件的 Cursor 账号，并在下一步让你指定其中一个作为**主账号（Primary Account）**，其余 Cursor 账号的权益将统一归并到该主账号名下（注意：并非所有特殊类型账号均支持多号合并，以页面实际提示为准）。

### 如果我不点合并，还能在国内继续单独给旧版 SuperGrok 续费吗？
可以。只要你的账号本身符合旧版独立订阅条件且未主动执行 `unify` 合并，就可以继续保留旧版计划，并通过 [chonggrok.com/supergrok](https://chonggrok.com/supergrok)选择 1 个月或 3 个月方案，仅凭 Grok User ID 和卡密在 [chonggrok.com/verify-grok](https://chonggrok.com/verify-grok)完成免密续费。

---

## 八、 参考资料与关联排障专题

* **Grok 知识库核心专题：**
  * [Grok 联合会员（The X Subscription）怎么选：四档价格与国内开通指南](https://he20000405-pixel.github.io/supergrok-china-guide/guides/x-subscription-overview/)
  * [为什么开了会员还是用不了 Grok Bot？权限解锁与每周额度池指南](https://he20000405-pixel.github.io/supergrok-china-guide/guides/grok-bot-weekly-pool-guide/)
  * [X 联合会员下使用 Cursor 编程怎么计费？第一方额度池与 Claude/GPT 扣费规则](https://he20000405-pixel.github.io/supergrok-china-guide/guides/grok-cursor-shared-billing/)
  * [SuperGrok 国内自助充值教程](https://he20000405-pixel.github.io/supergrok-china-guide/guides/supergrok-auto-recharge/)
  * [Grok User ID 怎么找：userId 获取与核对说明](https://he20000405-pixel.github.io/supergrok-china-guide/guides/grok-user-id/)
  * [Grok / SuperGrok 付款失败：card declined 与 3DS 排查](https://he20000405-pixel.github.io/supergrok-china-guide/guides/supergrok-payment-errors/)
  * [Grok Build 登录失败与 403 排查](https://he20000405-pixel.github.io/supergrok-china-guide/guides/grok-build-login-403/)
  * [ChongGrok AI 会员指南总门户 (guides.chonggrok.com)](https://guides.chonggrok.com/)
* **ChongGrok 主站入口：**
  * [ChongGrok 主站首页 (https://chonggrok.com)](https://chonggrok.com/)
  * [ChongGrok 旧版 SuperGrok 订阅页（https://chonggrok.com/supergrok）](https://chonggrok.com/supergrok)
  * [ChongGrok X 联合会员订阅页（https://chonggrok.com/x-subscription）](https://chonggrok.com/x-subscription)
  * [ChongGrok 旧版 Grok 核销页（https://chonggrok.com/verify-grok）](https://chonggrok.com/verify-grok)
  * [ChongGrok X 联合会员核销页（https://chonggrok.com/verify-x）](https://chonggrok.com/verify-x)
* **官方参考资料：**
  * [How to unify accounts under The X Subscription（官方账号合并指南）](https://docs.x.ai/x-subscription/unify-accounts)
  * [Unification eligibility: Who can combine accounts（账号合并资格说明）](https://docs.x.ai/x-subscription/eligibility)
  * [What is The X Subscription（Cursor 官方联合会员概述）](https://cursor.com/help/the-x-subscription/overview)

*事实与流程核验日期：2026-10-28。ChongGrok is not affiliated with xAI, X, or Cursor.*
*Keywords: SuperGrok 合并 Cursor · accounts.x.ai/unify · cursor.com/unify · X 联合会员合并不可逆 · Cursor 苹果内购退费 · 旧版 SuperGrok 续费 · Grok User ID 免密充值 · chonggrok.com*