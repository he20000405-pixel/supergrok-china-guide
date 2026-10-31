---
title: "Grok 联合会员、旧版 SuperGrok 与付款排障指南"
description: "区分 X 联合会员新购、旧版 SuperGrok 订单与历史卡兑换，查询 Grok Bot、共享周额度、账号凭据和付款排障路径。"
permalink: /
schema_type: CollectionPage
last_modified_at: 2026-10-31
breadcrumbs:
  - name: 首页
    url: /
item_list:
  - name: "Grok 联合会员四档与国内开通"
    url: /guides/x-subscription-overview/
  - name: "Grok Bot 权限与每周额度池"
    url: /guides/grok-bot-weekly-pool-guide/
  - name: "SuperGrok 与 Cursor 合并指南"
    url: /guides/supergrok-unify-migration-guide/
  - name: "X 联合会员下的 Cursor 计费"
    url: /guides/grok-cursor-shared-billing/
  - name: X 联合会员与 Grok Bot
    url: /guides/x-subscription-grok-bot-guide/
  - name: SuperGrok 自助充值
    url: /guides/supergrok-auto-recharge/
  - name: Grok User ID 怎么找
    url: /guides/grok-user-id/
  - name: Grok 新旧套餐怎么选
    url: /guides/supergrok-plans/
  - name: Grok 付款失败排查
    url: /guides/supergrok-payment-errors/
  - name: SuperGrok 付款后仍显示 Free
    url: /guides/supergrok-paid-but-still-free/
  - name: Grok Build 登录与 403
    url: /guides/grok-build-login-403/
  - name: 旧版与 X 联合会员对比
    url: /guides/supergrok-vs-x-premium-plus/
  - name: Grok 4.5 发布记录
    url: /guides/grok-4-5-update/
faq:
  - question: "还能在 ChongGrok 购买旧版 SuperGrok 月度或季度商品吗？"
    answer: "本站已停止销售旧版月度、季度商品。新购买请到 chonggrok.com/x-subscription 核对联合会员方案与办理条件；已有历史 Grok 卡密仍可在 chonggrok.com/verify-grok 兑换。旧订阅是否保留、续费或迁移，应按官方规则和原购买渠道核对。"
  - question: "历史 Grok 卡密与新联合会员卡分别在哪里兑换？"
    answer: "历史 Grok 卡密使用 chonggrok.com/verify-grok，按提示提交卡密与 Grok User ID；新联合会员卡使用 chonggrok.com/verify-x，按提示提交 Grok SSO。SSO 是敏感登录凭证，两种资料不能混用；不要把密码、验证码或登录凭证发到客服聊天或公开内容中。"
  - question: "开通 SuperGrok 后一定能看到 Grok 4.5 吗？"
    answer: "不能仅凭订阅名称保证。xAI 的 2026 年 7 月 16 日发布页明确了 Grok Build、Cursor 和 SpaceXAI console 等入口，但普通 grok.com 账号的可用性应以账号模型选择器和官方实时说明为准。"
  - question: "这个仓库提供 Grok API 充值吗？"
    answer: "不提供。本仓库和 chonggrok.com 这里只讨论 Grok / SuperGrok 会员订阅，不提供 API 额度、成品号、接码或批量注册服务。"
---

<section class="product-hero">
  <div>
    <p class="eyebrow">ChongGrok · Grok Knowledge Base</p>
    <h1>Grok 联合会员、旧订阅与付款排障指南</h1>
    <p class="lead">先区分 X 联合会员新购、旧订阅管理与历史卡兑换，再查看 Grok Bot 资格、每周用量、凭据要求和付款排障。</p>
    <div class="hero-actions">
      <a class="primary-link" href="{{ '/guides/x-subscription-grok-bot-guide/' | relative_url }}">了解联合会员与 Grok Bot</a>
      <a class="secondary-link" href="{{ '/guides/' | relative_url }}">浏览全部专题</a>
    </div>
    <form class="product-search" action="{{ site.portal_url }}search/" method="get" role="search">
      <label for="knowledge-search">搜索 ChatGPT、Grok、Claude、Gemini 知识库</label>
      <div class="search-control"><input id="knowledge-search" name="q" type="search" placeholder="例如：User ID、付款失败、Grok Build 403"><button type="submit">搜索</button></div>
    </form>
  </div>
  <aside class="hero-panel" aria-label="服务边界摘要">
    <strong>先确认方案与凭据，避免重复购买</strong>
    <ul>
      <li>本站已停售旧版商品；新购买查看联合会员。</li>
      <li>历史 Grok 卡兑换用 User ID；联合会员兑换要求 SSO。</li>
      <li>本站不办理旧会员转联合会员；转换走官方流程。</li>
      <li>已扣款或交易待处理时不要重复购买。</li>
    </ul>
  </aside>
</section>

> ChongGrok 是独立的会员订阅充值服务网站，与 xAI、X 不存在隶属、授权或官方合作关系。套餐、权益和模型可用性以官方页面及账号内实时展示为准。

## 从三个入口开始

新购用户或准备使用 Grok Bot，请先读 [X 联合会员与 Grok Bot]({{ '/guides/x-subscription-grok-bot-guide/' | relative_url }})。本站已停止销售旧版月度、季度商品；以下旧版流程资料用于历史订单与卡密核对，不能套用于联合会员 SSO 兑换。

<div class="route-grid">
  <section class="route-card"><span class="card-label">历史订单</span><h3>旧版充值流程参考</h3><p>查阅历史流程，核对已有卡密、User ID 与到账状态；不作为当前旧版购买指引。</p><a class="link-arrow" href="{{ '/guides/supergrok-auto-recharge/' | relative_url }}">查看历史流程</a></section>
  <section class="route-card"><span class="card-label">账号核对</span><h3>Grok User ID</h3><p>确认 `userId` 字段，避免把邮箱、昵称或 X 用户名当作账号标识。</p><a class="link-arrow" href="{{ '/guides/grok-user-id/' | relative_url }}">核对 User ID</a></section>
  <section class="route-card"><span class="card-label">订阅决策</span><h3>套餐怎么选</h3><p>比较联合会员与已有旧订阅，按功能、额度和原购买渠道判断。</p><a class="link-arrow" href="{{ '/guides/supergrok-plans/' | relative_url }}">查看新旧方案说明</a></section>
</div>

## 新旧订阅与核心专题

<p class="section-intro">充值、账号、报错、开发工具和版本更新分别由独立页面回答，避免不同问题混在一起。</p>

<div class="guide-grid">
  <section class="guide-card"><h3><a href="{{ '/guides/x-subscription-overview/' | relative_url }}">Grok 联合会员四档与国内开通</a></h3><p>四档价格、Grok Bot 权限与国内开通流程。</p></section>
  <section class="guide-card"><h3><a href="{{ '/guides/grok-bot-weekly-pool-guide/' | relative_url }}">Grok Bot 权限与每周额度池</a></h3><p>无权限排查、Weekly Pool 与 Top-ups 使用说明。</p></section>
  <section class="guide-card"><h3><a href="{{ '/guides/supergrok-unify-migration-guide/' | relative_url }}">SuperGrok 与 Cursor 合并指南</a></h3><p>Unify 迁移、苹果退费与旧版订阅保留说明。</p></section>
  <section class="guide-card"><h3><a href="{{ '/guides/grok-cursor-shared-billing/' | relative_url }}">X 联合会员下的 Cursor 计费</a></h3><p>Grok 第一方额度池与 Claude、GPT 扣费规则。</p></section>
  <section class="guide-card"><h3><a href="{{ '/guides/x-subscription-grok-bot-guide/' | relative_url }}">X 联合会员与 Grok Bot</a></h3><p>四档功能、共享周额度、额外费用和旧会员官方转换。</p></section>
  <section class="guide-card"><h3><a href="{{ '/guides/supergrok-auto-recharge/' | relative_url }}">自助充值流程</a></h3><p>历史流程参考：卡密、核销、User ID 和到账验收；旧版商品已停售。</p></section>
  <section class="guide-card"><h3><a href="{{ '/guides/grok-user-id/' | relative_url }}">Grok User ID</a></h3><p>准确查找、复制和脱敏，避免常见填错。</p></section>
  <section class="guide-card"><h3><a href="{{ '/guides/supergrok-plans/' | relative_url }}">Grok 新旧套餐选择</a></h3><p>比较联合会员与已有旧订阅；文中旧版商品周期为历史记录，本站当前不再销售。</p></section>
  <section class="guide-card"><h3><a href="{{ '/guides/supergrok-payment-errors/' | relative_url }}">付款失败排查</a></h3><p>card declined、3DS、发卡行和账单地址。</p></section>
  <section class="guide-card"><h3><a href="{{ '/guides/supergrok-paid-but-still-free/' | relative_url }}">付款后仍显示 Free</a></h3><p>购买入口、账号、App 同步、额度和卡密状态。</p></section>
  <section class="guide-card"><h3><a href="{{ '/guides/grok-build-login-403/' | relative_url }}">Grok Build 登录与 403</a></h3><p>浏览器授权、设备码、版本、旧会话与订阅权益。</p></section>
  <section class="guide-card"><h3><a href="{{ '/guides/supergrok-vs-x-premium-plus/' | relative_url }}">旧版与 X 联合会员对比</a></h3><p>保留旧权益、关联 Bot 与官方 Unify 是不同操作。</p></section>
  <section class="guide-card"><h3><a href="{{ '/guides/grok-4-5-update/' | relative_url }}">Grok 4.5 发布记录</a></h3><p>官方能力、首发入口和普通账号可用性边界。</p></section>
</div>

## 规则更新与开发工具

<div class="resource-grid">
  <section class="resource-card"><span class="resource-icon" aria-hidden="true">X</span><h3><a href="{{ '/guides/x-subscription-grok-bot-guide/' | relative_url }}">联合会员与旧方案怎么衔接</a></h3><p>旧方案可保留，Bot 关联与 Unify 不同；先比较权益和费用再决定。</p></section>
  <section class="resource-card"><span class="resource-icon" aria-hidden="true">403</span><h3><a href="{{ '/guides/grok-build-login-403/' | relative_url }}">Grok Build 登录排查</a></h3><p>按浏览器授权、设备码、账号一致性、版本、旧会话和订阅权益依次判断。</p></section>
</div>

## 遇到这些问题先这样处理

<div class="issue-grid">
  <section class="issue-card"><span class="intent-label">付款前</span><h3><a href="{{ '/guides/supergrok-payment-errors/' | relative_url }}">银行卡被拒或认证失败</a></h3><p>检查发卡行、境外订阅权限、3DS 和账单地址，不要连续换卡重试。</p></section>
  <section class="issue-card"><span class="intent-label">付款后</span><h3><a href="{{ '/guides/supergrok-paid-but-still-free/' | relative_url }}">扣款后仍显示 Free</a></h3><p>停止重复付款，确认购买入口、交易状态和当前登录账号。</p></section>
  <section class="issue-card"><span class="intent-label">开发工具</span><h3><a href="{{ '/guides/grok-build-login-403/' | relative_url }}">登录失败或出现 403</a></h3><p>先区分认证、软件版本和订阅权益；充值不能解决所有 403。</p></section>
</div>

## 历史 Grok 卡密兑换与 User ID 核验

| 步骤 | 用户要做什么 | 核对重点 |
|---|---|---|
| 1. 确认账号 | 登录 grok.com，确认是自己的目标账号 | 账号可正常使用 |
| 2. 确认卡密 | 核对已有卡密确为历史 Grok 卡 | 联合会员卡应使用 verify-x |
| 3. 核对原订单 | 留存订单号，异常时联系原订单支持 | 本站旧版商品已停售，不要重复购买 |
| 4. 核销卡密 | 打开 `chonggrok.com/verify-grok` 验证卡密 | 使用确认的核销入口 |
| 5. 提交 User ID | 复制 `userId` 并核对账号 | 不是邮箱、昵称或 X 用户名 |
| 6. 验收结果 | 回到 grok.com 查看订阅状态 | 未刷新时重新登录后再查 |

<img class="workflow-image" src="{{ '/img/chonggrok-supergrok-home-hero.webp' | relative_url }}" alt="旧版 SuperGrok 商品页历史示例，所示旧版商品已停售" width="1600" height="824" loading="lazy">

上图仅保留旧版商品页的历史示例，所示月度、季度商品已停售，不能据此下单。

Grok User ID 是用于定位账号的标识，不是登录密码，不能单独用来登录账号。请勿公开完整 session 页面，因为其中可能包含其他账号信息。

<img class="workflow-image" src="{{ '/img/grok-user-id-json-example.webp' | relative_url }}" alt="使用虚构数据制作的 Grok User ID JSON 示意图" width="1600" height="824" loading="lazy">

上图是虚构数据示意，不是真实用户资料。完整核对方法见 [Grok User ID 怎么找]({{ '/guides/grok-user-id/' | relative_url }})。

## 跨产品安全与付款资源

<div class="resource-grid">
  <section class="resource-card"><span class="resource-icon" aria-hidden="true">01</span><h3><a href="{{ site.portal_url }}resources/ai-membership-safety-checklist/">AI 会员订阅安全清单</a></h3><p>付款前检查账号和套餐，付款后回官方页面验收，并只提交最小必要资料。</p></section>
  <section class="resource-card"><span class="resource-icon" aria-hidden="true">02</span><h3><a href="{{ site.portal_url }}resources/ai-subscription-payment-troubleshooting/">AI 订阅付款排障决策树</a></h3><p>区分银行仍在处理、平台已经收款、订阅是否有效，以及当前账号是否显示会员。</p></section>
</div>

## 服务边界与风险说明

新联合会员查看 [X 联合会员服务页](https://chonggrok.com/x-subscription)，已有对应卡密使用 [verify-x](https://chonggrok.com/verify-x)；该流程要求的 SSO 是临时登录凭证，不是 User ID。[官方购买政策](https://x.ai/pricing)明确未授权第三方销售，相关账号可能被暂停或终止。

<div class="notice warning"><strong>重要：</strong>不需要密码不等于零风险。User ID 仍应谨慎保管，只在确认的核销流程中提交。任何线上订阅服务都无法诚实承诺绝对安全或账号结果。</div>

- 账号归用户自己，完成后由用户自行登录验收；
- 这里只处理会员订阅，不提供 API 额度；
- 不销售成品号，不做接码或批量注册；
- ChongGrok 与 xAI、X 无隶属或官方合作关系。

## 主站延伸阅读

- [历史 Grok 卡密兑换教程](https://chonggrok.com/blog/supergrok-chongzhi-zhinan)
- [SuperGrok 安全充值检查清单](https://chonggrok.com/blog/supergrok-safe-recharge-checklist)
- [Grok User ID 怎么找](https://chonggrok.com/blog/grok-user-id-zenme-zhao)
- [SuperGrok 国内充值失败排查](https://chonggrok.com/blog/supergrok-payment-failed-ai-recharge-2026)
- [Grok 新旧套餐怎么选](https://chonggrok.com/blog/supergrok-taocan-zenme-xuan)
- [旧版与 X 联合会员对比](https://chonggrok.com/blog/supergrok-vs-x-premium-plus)

{% include faq.html %}

<section class="service-panel">
  <h2>按新旧方案查服务，已有订单先查状态</h2>
  <p>新购买查看联合会员，历史 Grok 卡使用独立兑换入口。已有旧订阅先核对原购买渠道；是否迁移由用户按官方规则决定。有待处理订单时先查询原订单。</p>
  <div class="hero-actions"><a class="primary-link" href="https://chonggrok.com/x-subscription">联合会员方案</a><a class="secondary-link" href="https://chonggrok.com/supergrok">Grok 选购与迁移说明</a><a class="secondary-link" href="https://chonggrok.com/verify-x">联合会员兑换</a><a class="secondary-link" href="https://chonggrok.com/verify-grok">历史 Grok 卡密兑换</a></div>
</section>

<p class="meta">最后更新：2026-10-31</p>
