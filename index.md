---
title: "Grok 联合会员、旧版 SuperGrok 与付款排障指南"
description: "区分 X 联合会员、Grok Bot 与旧版 SuperGrok 续费，查询共享周额度、账号凭据、付款失败和已付款未生效的处理路径。"
permalink: /
schema_type: CollectionPage
last_modified_at: 2026-10-28
breadcrumbs:
  - name: 首页
    url: /
item_list:
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
  - question: "国内如何用支付宝或微信开通 SuperGrok？"
    answer: "符合旧版订阅条件的账号可先在 chonggrok.com/supergrok 核对资格、商品周期与交付，再付款，获得卡密后前往 chonggrok.com/verify-grok 核销，再按页面提示提交自己的 Grok User ID 并验收订阅状态。"
  - question: "chonggrok.com 充值 SuperGrok 需要密码吗？"
    answer: "不需要。流程只要求本次升级所需的 Grok User ID，不应提交登录密码、邮箱验证码或恢复码。"
  - question: "开通 SuperGrok 后一定能看到 Grok 4.5 吗？"
    answer: "不能仅凭订阅名称保证。xAI 的 2026 年 7 月 16 日发布页明确了 Grok Build、Cursor 和 SpaceXAI console 等入口，但普通 grok.com 账号的可用性应以账号模型选择器和官方实时说明为准。"
  - question: "这个仓库提供 Grok API 充值吗？"
    answer: "不提供。本仓库和 chonggrok.com 这里只讨论 Grok / SuperGrok 会员订阅，不提供 API 额度、成品号、接码或批量注册服务。"
---

<section class="product-hero">
  <div>
    <p class="eyebrow">ChongGrok · Grok Knowledge Base</p>
    <h1>Grok 联合会员、旧版续费与付款排障指南</h1>
    <p class="lead">先区分 X 联合会员新购、旧版 SuperGrok 续费与官方转换，再查看 Grok Bot 资格、每周用量、凭据要求和付款排障。</p>
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
      <li>付款后保存订单和卡密，再进入核销页。</li>
      <li>旧版兑换用 User ID；联合会员兑换要求 SSO，两者不同。</li>
      <li>本站不办理旧会员转联合会员；转换走官方流程。</li>
      <li>已扣款或交易待处理时不要重复购买。</li>
    </ul>
  </aside>
</section>

> ChongGrok 是独立的会员订阅充值服务网站，与 xAI、X 不存在隶属、授权或官方合作关系。套餐、权益和模型可用性以官方页面及账号内实时展示为准。

## 从三个入口开始

新购用户或准备使用 Grok Bot，请先读 [X 联合会员与 Grok Bot]({{ '/guides/x-subscription-grok-bot-guide/' | relative_url }})。以下充值与 User ID 步骤用于符合条件的旧版 SuperGrok；不能套用于联合会员 SSO 兑换。

<div class="route-grid">
  <section class="route-card"><span class="card-label">完整流程</span><h3>SuperGrok 自助充值</h3><p>选择周期、支付宝或微信付款、取得卡密、核销并回官方页面验收。</p><a class="link-arrow" href="{{ '/guides/supergrok-auto-recharge/' | relative_url }}">查看充值流程</a></section>
  <section class="route-card"><span class="card-label">账号核对</span><h3>Grok User ID</h3><p>确认 `userId` 字段，避免把邮箱、昵称或 X 用户名当作账号标识。</p><a class="link-arrow" href="{{ '/guides/grok-user-id/' | relative_url }}">核对 User ID</a></section>
  <section class="route-card"><span class="card-label">订阅决策</span><h3>套餐怎么选</h3><p>先分联合会员新购与旧版续费，再按功能、额度和周期判断。</p><a class="link-arrow" href="{{ '/guides/supergrok-plans/' | relative_url }}">比较功能与周期</a></section>
</div>

## 新旧订阅与核心专题

<p class="section-intro">充值、账号、报错、开发工具和版本更新分别由独立页面回答，避免不同问题混在一起。</p>

<div class="guide-grid">
  <section class="guide-card"><h3><a href="{{ '/guides/x-subscription-grok-bot-guide/' | relative_url }}">X 联合会员与 Grok Bot</a></h3><p>四档功能、共享周额度、额外费用和旧会员官方转换。</p></section>
  <section class="guide-card"><h3><a href="{{ '/guides/supergrok-auto-recharge/' | relative_url }}">自助充值流程</a></h3><p>下单、卡密、核销、User ID 和到账验收。</p></section>
  <section class="guide-card"><h3><a href="{{ '/guides/grok-user-id/' | relative_url }}">Grok User ID</a></h3><p>准确查找、复制和脱敏，避免常见填错。</p></section>
  <section class="guide-card"><h3><a href="{{ '/guides/supergrok-plans/' | relative_url }}">Grok 新旧套餐选择</a></h3><p>先比较联合会员与旧版续费；旧版商品按 1 个月或 3 个月核对。</p></section>
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

## 旧版 SuperGrok 续费与 User ID 核验

| 步骤 | 用户要做什么 | 核对重点 |
|---|---|---|
| 1. 确认账号 | 登录 grok.com，确认是自己的目标账号 | 账号可正常使用 |
| 2. 选择套餐 | 先确认旧版资格，再按实时商品选择周期 | 新购联合会员另走对应流程 |
| 3. 完成付款 | 使用支付宝或微信，保存订单和卡密 | 不向他人发送密码 |
| 4. 核销卡密 | 打开 `chonggrok.com/verify-grok` 验证卡密 | 使用确认的核销入口 |
| 5. 提交 User ID | 复制 `userId` 并核对账号 | 不是邮箱、昵称或 X 用户名 |
| 6. 验收结果 | 回到 grok.com 查看订阅状态 | 未刷新时重新登录后再查 |

<img class="workflow-image" src="{{ '/img/chonggrok-supergrok-home-hero.webp' | relative_url }}" alt="旧版 SuperGrok 充值页历史示例，当前商品以主站为准" width="1600" height="824" loading="lazy">

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

- [SuperGrok 充值完整教程](https://chonggrok.com/blog/supergrok-chongzhi-zhinan)
- [SuperGrok 安全充值检查清单](https://chonggrok.com/blog/supergrok-safe-recharge-checklist)
- [Grok User ID 怎么找](https://chonggrok.com/blog/grok-user-id-zenme-zhao)
- [SuperGrok 国内充值失败排查](https://chonggrok.com/blog/supergrok-payment-failed-ai-recharge-2026)
- [Grok 新旧套餐怎么选](https://chonggrok.com/blog/supergrok-taocan-zenme-xuan)
- [旧版与 X 联合会员对比](https://chonggrok.com/blog/supergrok-vs-x-premium-plus)

{% include faq.html %}

<section class="service-panel">
  <h2>按新旧方案查服务，已有订单先查状态</h2>
  <p>先核对现有订阅及账号资格。联合会员新购与旧版续费分别办理，本站不办理旧会员转换；有待处理订单时先查询原订单。</p>
  <div class="hero-actions"><a class="primary-link" href="https://chonggrok.com/x-subscription">联合会员方案</a><a class="secondary-link" href="https://chonggrok.com/supergrok">旧版续费方案</a><a class="secondary-link" href="https://chonggrok.com/verify-x">联合会员兑换</a><a class="secondary-link" href="https://chonggrok.com/verify-grok">旧版 Grok 兑换</a></div>
</section>

<p class="meta">最后更新：2026-10-28</p>
