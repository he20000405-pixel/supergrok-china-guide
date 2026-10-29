---
title: "X 联合会员下使用 Cursor 编程怎么计费？2026 Grok 第一方额度池与 Claude / GPT 扣费规则解析"
description: "2026年10月开发者实测：详解 The X Subscription（Grok 联合会员）下 Cursor 编辑器的双轨计费规则，区分 Grok 4.7/4.5 第一方模型共享每周额度池（Weekly Pool）与 Claude/GPT 第三方模型按 API 扣取预充值余额的边界，附国内通过 chonggrok.com 开通指南。"
permalink: /guides/grok-cursor-shared-billing/
date: 2026-10-28
last_modified_at: 2026-10-29
---

# X 联合会员下使用 Cursor 编程怎么计费？2026 Grok 第一方额度池与 Claude / GPT 扣费规则解析

**直接结论：** 在 xAI 与 Cursor 联合推出的 **The X Subscription（X 联合会员）** 体系下，你在 Cursor 编辑器里写代码的计费方式严格取决于**你当前选中的模型归属**：调用 **xAI 第一方模型（如 Grok 4.7 High / Grok 4.5 系列）** 完全包含在套餐内，与 Grok 网页端、Grok Bot 共用每 7 天重置一次的 **每周共享额度池（`Weekly usage limit`）**；但在 Cursor 中切换调用 **Claude（如 Claude Sonnet / Opus）或 GPT 等第三方模型**，**不包含在任何一档联合会员套餐内（即使开通 $100 Super 或 $200 Ultra 也不包）**，将从第 1 次请求起直接按官方 API 目录价扣减账户内的**预充值余额（`Prepaid Credit` / `Additional Usage Credit`）**。国内开发者如需开通支持高倍第一方额度池的 X 联合会员，或单独搭配 Claude Pro / ChatGPT Plus 本号订阅，均可通过 **[ChongGrok (chonggrok.com)](https://chonggrok.com)** 使用支付宝或微信自助办理。

---

## 一、 升级 X 联合会员后，在 Cursor 里写代码哪些免费包池、哪些额外扣费？

许多开发者误以为开通了 $30/月的 Premium 或 $100/月的 Super 联合会员后，就能在 Cursor 里免费无限刷 Claude 和 GPT。事实上，官方将 **“会员套餐费（Subscription Fee）”、“每周包含额度池（Weekly Included Pool）”与“预充值余额（Prepaid Deposit）”** 拆成了完全独立的三套核算逻辑：

| 你在 Cursor 中使用的功能或模型                               | 是否包含在 X 联合会员的「每周额度池」内？ | 实际扣费规则与档位限制                                       |
| :----------------------------------------------------------- | :---------------------------------------- | :----------------------------------------------------------- |
| **调用 xAI 第一方编程模型（如 Grok 4.7 High / Grok 4.5 / Grok Code）** | ✅ **包含（免额外扣费）**                  | 直接消耗每周共享额度池（Plus 为 1x，Premium 为 4x，Super 为 15x，Ultra 为 50x），每 7 天自动回满 |
| **使用 Cursor 云端智能体与自动化审查（Cloud Agents & Automations）** | ✅ **包含在 Premium（$30/月）及以上档位**  | **$8/月的 Plus 档位不支持**；需开通 Premium（$30/月）及以上档位方可解锁 Cursor Cloud Agents 与 Grok Bot |
| **切换调用 Anthropic 模型（如 Claude Sonnet / Claude Opus）** | ❌ **不包含（全档位均不包）**              | **从第 1 次调用起（From the first use）**，按官方 API 目录价实时扣减账户内的 **Prepaid Credit（预充值余额）** |
| **切换调用 OpenAI 模型（如 GPT 系列编程模型）**              | ❌ **不包含（全档位均不包）**              | **从第 1 次调用起**，按官方 API 目录价实时扣减账户内的 **Prepaid Credit（预充值余额）** |
| **当周第一方额度池（Weekly Pool）用满 100% 后继续调用 Grok 模型** | ⚠️ **超出部分转按量计费**                  | 若开启了预充值（Top-ups），超出每周池的第一方模型请求将转为消耗 Prepaid Credit 余额 |

> **开发者避坑提示：** 升级至更高档位的 X 联合会员（如从 $30 升至 $100），扩大的是 **Grok 第一方模型的每周额度池容量**，并不会把 Claude 或 GPT 变成套餐内免费包含的模型。如需了解四档套餐的完整参数，请参阅 [Grok 联合会员（The X Subscription）怎么选](https://he20000405-pixel.github.io/supergrok-china-guide/guides/x-subscription-overview/)；国内开发者如需直接升级个人原号，可通过 **[ChongGrok X 联合会员订阅页](https://chonggrok.com/x-subscription)** 办理。

---

## 二、 旧版 Cursor Pro ($20/月) 与新版 X 联合会员 Premium ($30/月) 开发者该选哪个？

针对日常重度使用 AI 写代码的程序员，到底应该保留旧版 $20/月的 Cursor Pro，还是切换至新版 $30/月的 X 联合会员 Premium 档？请根据你的**真实主力模型习惯**对照下表决策：

| 对比维度 | 保留「旧版 Cursor Pro（$20/月）」 | 开通/升级「新版 X 联合会员 Premium（$30/月）」 |
| :--- | :--- | :--- |
| **核心优势** | **保留旧版套餐内包含的 Claude / GPT 第三方模型调用额度**（只要不主动点 Unify 合并就一直有效） | 一份账单同时打包 **4x 容量 Grok 每周池 + Grok Bot 云端自动化 + Cursor + X Premium+ 免广告** |
| **主力模型适配度** | 适合 **80% 以上代码交由 Claude / GPT 编写**、几乎不用 Grok 模型与 Grok Bot 的开发者 | 适合 **认可 Grok 4.7 High / 4.5 编码能力**，且需要高频运行 **Grok Bot** 与 Cursor Cloud Agents 的开发者 |
| **额度刷新机制** | 按月度账单周期结算包含额度 | **每 7 天滚动重置一次每周额度池**，单周高强度冲刺写代码耗尽后下周即可满血恢复 |
| **Grok Bot 权限** | 新开旧版已无法解锁 Grok Bot | **原生完整支持 Grok Bot**，无需手动绑定，同一个账号登录即享共享额度池 |
| **国内最佳搭配方案** | 老账号切勿点击 `unify` 合并（合并不可逆，详见 [老版 SuperGrok 与 Cursor 合并避坑指南](https://he20000405-pixel.github.io/supergrok-china-guide/guides/supergrok-unify-migration-guide/)） | 在 **[ChongGrok X 联合会员订阅页](https://chonggrok.com/x-subscription)** 开通 **X 联合会员 Premium 档**跑 Grok 全家桶；若同时需重度使用 Claude 或 GPT，可在站内单独搭配 **[Claude Pro](https://chonggrok.com/claude)** 或 **[ChatGPT Plus/Pro](https://chonggrok.com/chatgpt)** 本号订阅 |

---

## 三、 如何在 grok.com/dashboard 管理 Cursor 预充值余额与防扣爆上限？

当你开通或合并至新版 X 联合会员后，Cursor 的账单、用量监控与预充值（Top-ups）将统一收敛至 **[grok.com/dashboard](https://grok.com/dashboard)** 工作空间进行管理：

### 1. 为什么我的每周额度池还有 80%，在 Cursor 里写代码却报错余额不足？
* **原因定位：** 这是因为你在 Cursor 的模型选择器中勾选了 **Claude 或 GPT**，而你账户内的 **Prepaid Credit（预充值余额 / Additional Usage Credit）为 $0.00**。由于第三方模型完全不走每周额度池，哪怕你的 `Weekly usage limit` 是满的，只要预充值余额为 0 且未开启按需计费，调用第三方模型就会立即被拦截。
* **解决办法：** 在 Cursor 中将模型切换回 **Grok 第一方系列模型**（直接走免费的每周包含额度池）；或者前往 [grok.com/dashboard/billing](https://grok.com/dashboard/billing) 充值 Prepaid Credit。

### 2. 开启 Auto Top-up 与设置月度消费硬上限（Monthly Limit）
如果你确实需要在 Cursor 中混合调用第三方模型，或在每周池耗尽后继续运行 Grok Bot（详见 [Grok Bot 权限解锁与每周额度池指南](https://he20000405-pixel.github.io/supergrok-china-guide/guides/grok-bot-weekly-pool-guide/)），可在后台按以下两步控制成本：
1. **管理预充值（Prepaid balance）：** 在 [grok.com/dashboard/billing](https://grok.com/dashboard/billing) 中可选择单次购买预充值额度（Purchase credits），或开启余额不足时自动充值（`Auto top-up when balance runs low`）。
2. **设置月度封顶（Monthly usage limit）：** 强烈建议设置月度额外消费上限，避免在 Cursor 中开启长上下文 Agent 循环重构代码时无意间耗尽大额 API 费用。

---

## 四、 开发者订阅或充值前先检查

| 检查项                     | 正确状态与避坑要求                                           |
| :------------------------- | :----------------------------------------------------------- |
| **1. 模型需求评估**        | 已清楚新版 X 联合会员每周额度池仅包 **Grok 第一方模型**，Claude 与 GPT 在 Cursor 内需额外消耗预充值余额 |
| **2. 档位权限核对**        | 若需使用 Cursor Cloud Agents 与 Grok Bot，已确认选择 **Premium（$30/月）** 或以上档位（不选 $8 的 Plus 档） |
| **3. 旧账号防误操作**      | 若手头有包含第三方额度的旧版 Cursor Pro 且不想失去该权益，确认**不要点击 `cursor.com/unify` 合并** |
| **4. 独立充值凭证准备**    | 若决定不合并 Cursor、仅单独为 Grok 账号充值「旧版 SuperGrok」，已按 [Grok User ID 怎么找](https://he20000405-pixel.github.io/supergrok-china-guide/guides/grok-user-id/) 准备好 User ID |
| **5. 严守密码与 API 边界** | 明确 `chonggrok.com` 仅办理个人原号会员订阅升级（不做 API 额度售卖），且全程不向任何人提供账号明文密码 |

---

## 五、 国内开发者如何免海外卡配齐 Grok 联合会员、SuperGrok 与 Claude / ChatGPT？

针对国内开发者在 Stripe 绑卡时频繁遭遇 `Card declined`、虚拟卡段被风控拉黑的问题（排查详见 [Grok 付款失败排查](https://he20000405-pixel.github.io/supergrok-china-guide/guides/supergrok-payment-errors/)），可通过 **[ChongGrok (chonggrok.com)](https://chonggrok.com)** 按以下三种开发流方案用支付宝或微信一站式配齐：

1. **方案一：主攻 Grok 编码 + Grok Bot 自动化（开通新版 X 联合会员）**
   * 打开 **[https://chonggrok.com/x-subscription](https://chonggrok.com/x-subscription)**，按页面实时展示价格选择 **X 联合会员 — Premium（$30 档，4x 额度池）** 或 **Super（$100 档，15x 额度池）**。
   * 付款后保存卡密，前往 **[https://chonggrok.com/verify-x](https://chonggrok.com/verify-x)**，按页面说明验证卡密、填写目标 Grok 账号的 SSO 并提交，回到 [grok.com/dashboard](https://grok.com/dashboard) 验收后即可用同一账号直接登录 Cursor 与 Grok Bot。**SSO 属于敏感登录凭据，不要发送到客服聊天或公开页面。**
2. **方案二：保留旧版 Cursor 不动，仅单独充值「旧版 SuperGrok」**
   * 若你不想合并现有的 Cursor 账单，只想在网页端使用 Grok 4.5 / 4.7 与 DeepSearch 辅助查资料，可在 **[https://chonggrok.com/supergrok](https://chonggrok.com/supergrok)** 选择「旧版 SuperGrok（1个月 / 3个月）」。
   * 在 **[https://chonggrok.com/verify-grok](https://chonggrok.com/verify-grok)** 仅需提交 **卡密 + Grok User ID** 即可免密码完成充值（详见 [SuperGrok 国内自助充值教程](https://he20000405-pixel.github.io/supergrok-china-guide/guides/supergrok-auto-recharge/)）。
3. **方案三：Grok + Claude Pro 或 ChatGPT Plus/Pro 多工具组合**
   * 对于不想在 Cursor 里按高昂 API 单价为每次 Claude/GPT 请求付费的开发者，可在 **[https://chonggrok.com](https://chonggrok.com)** 同步为自己的个人原账号开通 **[Claude Pro](https://chonggrok.com/claude)** 或 **[ChatGPT Plus / Pro](https://chonggrok.com/chatgpt)** 会员，以固定月费锁定各大第一方官方客户端的充足推理与编程额度。**这些订阅用于各自官方产品，不会抵扣 Cursor 内 Claude / GPT 的预充值费用。**

---

## 六、 风险与业务边界说明

* **坚持自有原账号升级：** ChatGPT、Grok、Claude 均只做用户自有原账号的会员订阅升级（全站仅 Gemini 另有一年成品账号这一项专属业务例外），绝不做多人共享合租号，代码仓库与对话隐私完全由开发者个人掌控。
* **不做 API 额度与违规业务：** 请特别注意，本知识库与 `chonggrok.com` **只办理消费者会员订阅升级，不提供官方 API Key 售卖或 API 预充值额度（Prepaid Credit / Top-ups）代充**，也不做手机接码或批量注册。
* **最小化凭证原则：** 旧版 SuperGrok 充值在 [chonggrok.com/verify-grok](https://chonggrok.com/verify-grok) 提交卡密与 Grok User ID；X 联合会员在 [chonggrok.com/verify-x](https://chonggrok.com/verify-x) 按页面说明提交对应卡密与 Grok SSO。User ID 是账号标识，SSO 是敏感登录凭据，两者不能混用。无需登录密码、邮箱验证码或恢复码。任何线上订阅协助服务均非零风险，请仅在核实无误的对应核销页面提交信息，不要向客服聊天或公开页面发送 SSO，并保存好订单号与核销截图。
* **独立第三方声明：** ChongGrok (`chonggrok.com`) 是独立的第三方会员订阅充值服务网站，与 xAI、Grok、X、Cursor、Anthropic 或 OpenAI 不存在隶属、官方授权或合作关系。

---

## 七、 常见问题解答（FAQ）

### 我如果开通 $100/月的 Super 或 $200/月的 Ultra 档位，在 Cursor 里用 Claude 5.5 或 GPT 免费吗？
不免费。根据 xAI 与 Cursor 的官方计费文档，所有四个档位的 X 联合会员（Plus / Premium / Super / Ultra）包含的每周共享额度池都**仅限调用 xAI 第一方模型**。在 Cursor 内调用 Claude 或 GPT 等第三方模型，无论你处于哪个会员档位，都必须从第 1 次使用起消耗预充值余额（Prepaid Credit）。

### 为什么在 Cursor 里用 Grok 4.7 High 写代码，感觉比标注的“4x 额度池”消耗得快或慢？
官方说明指出，每周共享额度池（Weekly Pool）由 Grok 对话、生图、Grok Bot 和 Cursor 共同竞争使用，且不同产品与不同模型模式（如标准模式 vs High 深度推理模式、长上下文代码仓库扫描）的单次算力消耗权重不同，因此 `4x` 代表总容量池是 Plus 基础档的 4 倍，而不代表固定不变的任务完成次数。

### 升级到 X 联合会员后，如果核销完成了但 Cursor 里还是显示 Free 怎么办？
请先打开 [grok.com/dashboard/billing](https://grok.com/dashboard/billing) 确认你的联合会员状态是否已显示为 `Premium`（或对应付费档位）。如果 `grok.com` 端也显示 `Free`，请停止重复下单，先按 [付款成功但仍显示 Free 排查](https://he20000405-pixel.github.io/supergrok-china-guide/guides/supergrok-paid-but-still-free/) 核查；如果 `grok.com` 已显示为会员，只需在 Cursor 编辑器设置中点击 `Sign Out` 退出当前账号，再重新使用该联合会员账号登录即可刷新权限。

---

## 八、 参考资料与关联排障专题

* **Grok 知识库核心专题：**
  * [Grok 联合会员（The X Subscription）怎么选：四档价格与国内开通指南](https://he20000405-pixel.github.io/supergrok-china-guide/guides/x-subscription-overview/)
  * [为什么开了会员还是用不了 Grok Bot？权限解锁与每周额度池指南](https://he20000405-pixel.github.io/supergrok-china-guide/guides/grok-bot-weekly-pool-guide/)
  * [老版 SuperGrok 与 Cursor 要不要合并（Unify）？迁移避坑与旧版保留指南](https://he20000405-pixel.github.io/supergrok-china-guide/guides/supergrok-unify-migration-guide/)
  * [SuperGrok 国内自助充值教程](https://he20000405-pixel.github.io/supergrok-china-guide/guides/supergrok-auto-recharge/)
  * [Grok User ID 怎么找：userId 获取与核对说明](https://he20000405-pixel.github.io/supergrok-china-guide/guides/grok-user-id/)
  * [Grok Build 登录失败与 403 排查](https://he20000405-pixel.github.io/supergrok-china-guide/guides/grok-build-login-403/)
  * [ChongGrok AI 会员指南总门户 (guides.chonggrok.com)](https://guides.chonggrok.com/)
* **ChongGrok 主站入口：**
  * [ChongGrok 主站首页 — ChatGPT / Grok / Claude / Gemini 订阅服务 (https://chonggrok.com)](https://chonggrok.com/)
  * [ChongGrok 旧版 SuperGrok 订阅页（https://chonggrok.com/supergrok）](https://chonggrok.com/supergrok)
  * [ChongGrok X 联合会员订阅页（https://chonggrok.com/x-subscription）](https://chonggrok.com/x-subscription)
  * [ChongGrok 旧版 Grok 核销页（https://chonggrok.com/verify-grok）](https://chonggrok.com/verify-grok)
  * [ChongGrok X 联合会员核销页（https://chonggrok.com/verify-x）](https://chonggrok.com/verify-x)
* **官方参考资料：**
  * [What is The X Subscription?（cursor.com/help/the-x-subscription/overview）](https://cursor.com/help/the-x-subscription/overview)
  * [The X Subscription Overview & Usage Pool（docs.x.ai/x-subscription/overview）](https://docs.x.ai/x-subscription/overview)

*事实与流程核验日期：2026-10-28。ChongGrok is not affiliated with xAI, X, Cursor, Anthropic, or OpenAI.*
*Keywords: X 联合会员 Cursor 计费 · Cursor 用 Claude 怎么扣费 · Grok 联合会员 Cursor 额度池 · Additional Usage Credit · Prepaid Credit · Cursor Pro 合并 SuperGrok · 国内开通 Cursor Grok · chonggrok.com*