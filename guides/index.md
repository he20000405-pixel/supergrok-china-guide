---
title: "Grok 联合会员、旧版续费与付款排障专题"
description: "X 联合会员、Grok Bot、共享额度、旧版 SuperGrok 续费、User ID、付款失败、仍显示 Free、Grok Build 403 和历史版本专题目录。"
permalink: /guides/
schema_type: CollectionPage
last_modified_at: 2026-10-28
breadcrumbs:
  - name: "首页"
    url: /
  - name: "专题"
    url: /guides/
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
  - name: Grok 4.5 更新
    url: /guides/grok-4-5-update/
  - name: Grok 新旧周额度与订阅状态
    url: /guides/supergrok-weekly-limit-vs-subscription/
  - name: SuperGrok 续费失败
    url: /guides/supergrok-renewal-failed/
  - name: Grok Automations 定时任务与邮件触发器
    url: /guides/grok-automations/
  - name: Grok Connectors 连接器使用指南
    url: /guides/grok-connectors/
  - name: SuperGrok 取消订阅与退款
    url: /guides/supergrok-cancel-refund/
  - name: Grok 实时搜索与来源核验
    url: /guides/grok-real-time-search-verification/
  - name: Grok Build Mode 创建与发布
    url: /guides/grok-build-mode/
  - name: Grok Imagine Video 1.5 使用指南
    url: /guides/grok-imagine-video-1-5/
  - name: Grok Google Workspace 使用指南
    url: /guides/grok-google-workspace/
  - name: Grok Microsoft 365 使用指南
    url: /guides/grok-microsoft-365/
  - name: Grok User ID / UUID English Guide
    url: /en/guides/grok-user-id/
  - name: Grok Build 403 English Guide
    url: /en/guides/grok-build-login-403/
  - name: SuperGrok Card Declined English Guide
    url: /en/guides/supergrok-card-declined/
  - name: SuperGrok Paid but Still Free English Guide
    url: /en/guides/supergrok-paid-but-still-free/
---

<p class="eyebrow">SuperGrok Topic Index</p>
# Grok 订阅与排障专题目录

<p class="lead">将充值、账号标识、付款报错、开发工具和版本更新拆成独立页面。先按问题类型选择专题，再执行对应检查，避免把不同原因混在一起。</p>

> **不知道先读哪篇？** 新购或使用 Bot 先看“X 联合会员”；保留旧版则看套餐或充值流程；第一次付款报错看“付款失败”；会员到期或自动续费报错看“续费失败”；已扣款看“仍显示 Free”；计划有效但功能受限先检查“周额度”；Grok Build 报 403 进入开发工具专题。

<div class="catalog-list">
  <a class="catalog-item" href="{{ '/guides/x-subscription-grok-bot-guide/' | relative_url }}"><span class="catalog-number">新</span><span class="catalog-copy"><strong>X 联合会员与 Grok Bot</strong><p>四档、共享周额度、旧版资格与官方转换；新购和续费分开办理。</p><span class="catalog-meta">完成目标：确定套餐、费用与适用办理路径</span></span><span class="intent-label">订阅 / 用量</span></a>
  <a class="catalog-item" href="{{ '/guides/supergrok-auto-recharge/' | relative_url }}"><span class="catalog-number">01</span><span class="catalog-copy"><strong>SuperGrok 自助充值流程</strong><p>支付宝/微信、卡密核销、User ID 和到账验收。</p><span class="catalog-meta">约 7 分钟 · 完成目标：提交最小资料并回官方页面验收</span></span><span class="intent-label">旧版 / 流程</span></a>
  <a class="catalog-item" href="{{ '/guides/grok-user-id/' | relative_url }}"><span class="catalog-number">02</span><span class="catalog-copy"><strong>Grok User ID 的用途与核对</strong><p>识别正确的账号标识，并避免公开或提交其他账号信息。</p><span class="catalog-meta">约 5 分钟 · 完成目标：只提交当前核销流程要求的 User ID</span></span><span class="intent-label">账号 / 凭据</span></a>
  <a class="catalog-item" href="{{ '/guides/supergrok-plans/' | relative_url }}"><span class="catalog-number">03</span><span class="catalog-copy"><strong>Grok 新旧套餐怎么选</strong><p>先比较联合会员与旧版，再选择功能、额度或 1/3 个月旧版商品。</p><span class="catalog-meta">约 5 分钟 · 完成目标：判断现在是否需要付费</span></span><span class="intent-label">套餐 / 选择</span></a>
  <a class="catalog-item" href="{{ '/guides/supergrok-payment-errors/' | relative_url }}"><span class="catalog-number">04</span><span class="catalog-copy"><strong>Grok 付款失败排查</strong><p>card declined、3DS、账单地址和发卡行限制。</p><span class="catalog-meta">约 8 分钟 · 完成目标：识别原支付渠道和拒付责任方</span></span><span class="intent-label">报错 / 搜索</span></a>
  <a class="catalog-item" href="{{ '/guides/supergrok-paid-but-still-free/' | relative_url }}"><span class="catalog-number">05</span><span class="catalog-copy"><strong>付款成功但仍显示 Free</strong><p>按新旧订单核对购买入口、账号与工作区、额度和兑换状态。</p><span class="catalog-meta">约 9 分钟 · 完成目标：区分订单、订阅和账号权益</span></span><span class="intent-label">付款 / 状态</span></a>
  <a class="catalog-item" href="{{ '/guides/grok-build-login-403/' | relative_url }}"><span class="catalog-number">06</span><span class="catalog-copy"><strong>Grok Build 登录与 403</strong><p>浏览器授权、设备码、版本、旧会话和订阅权益。</p><span class="catalog-meta">约 9 分钟 · 完成目标：判断 403 属于登录、版本还是权益</span></span><span class="intent-label">开发者 / 搜索</span></a>
  <a class="catalog-item" href="{{ '/guides/supergrok-vs-x-premium-plus/' | relative_url }}"><span class="catalog-number">07</span><span class="catalog-copy"><strong>旧版与 X 联合会员对比</strong><p>区分旧版 SuperGrok、X Premium+ 与联合会员，理解关联与转换。</p><span class="catalog-meta">约 6 分钟 · 完成目标：避免在两个入口建立重复订阅</span></span><span class="intent-label">新旧 / 对比</span></a>
  <a class="catalog-item" href="{{ '/guides/grok-4-5-update/' | relative_url }}"><span class="catalog-number">08</span><span class="catalog-copy"><strong>Grok 4.5 发布记录</strong><p>2026 年 7 月发布时的能力、首发入口与边界。</p><span class="catalog-meta">约 6 分钟 · 完成目标：判断版本更新是否影响自己的入口选择</span></span><span class="intent-label">历史 / 版本</span></a>
  <a class="catalog-item" href="{{ '/guides/supergrok-weekly-limit-vs-subscription/' | relative_url }}"><span class="catalog-number">09</span><span class="catalog-copy"><strong>新旧周额度用完还是订阅未生效</strong><p>分清旧版 Settings 与联合会员工作区，核对用量、额外费用和原订单。</p><span class="catalog-meta">约 9 分钟 · 完成目标：判断是等待重置、检查用量还是查询原订单</span></span><span class="intent-label">用量 / 续费</span></a>
  <a class="catalog-item" href="{{ '/guides/supergrok-renewal-failed/' | relative_url }}"><span class="catalog-number">10</span><span class="catalog-copy"><strong>SuperGrok 续费失败排查</strong><p>回到 grok.com、Apple、Google Play 或 X Premium+ 原购买平台处理。</p><span class="catalog-meta">约 10 分钟 · 完成目标：找到原购买平台并恢复或结束续费</span></span><span class="intent-label">用量 / 续费</span></a>
  <a class="catalog-item" href="{{ '/guides/grok-automations/' | relative_url }}"><span class="catalog-number">11</span><span class="catalog-copy"><strong>Grok Automations 使用教程</strong><p>创建和测试定时任务，并理解邮件触发器与 SuperGrok 的套餐边界。</p><span class="catalog-meta">约 10 分钟 · 完成目标：建立并验证第一项自动化任务</span></span><span class="intent-label">使用 / 教程</span></a>
  <a class="catalog-item" href="{{ '/guides/supergrok-cancel-refund/' | relative_url }}"><span class="catalog-number">12</span><span class="catalog-copy"><strong>取消订阅、退款与更换付款方式</strong><p>按 grok.com、Apple、Google Play 或 X 原购买渠道处理。</p><span class="catalog-meta">约 10 分钟 · 完成目标：停止续费并找到正确退款责任方</span></span><span class="intent-label">订阅管理 / 搜索</span></a>
  <a class="catalog-item" href="{{ '/guides/grok-real-time-search-verification/' | relative_url }}"><span class="catalog-number">13</span><span class="catalog-copy"><strong>Grok 实时搜索与来源核验</strong><p>搜索网页和 X，并按发布者、日期、原文与多方证据检查回答。</p><span class="catalog-meta">约 12 分钟 · 完成目标：把实时搜索结果变成可复查的证据</span></span><span class="intent-label">使用 / 教程</span></a>
  <a class="catalog-item" href="{{ '/guides/grok-build-mode/' | relative_url }}"><span class="catalog-number">14</span><span class="catalog-copy"><strong>Grok Build Mode 使用指南</strong><p>从模式选择器创建网站、应用或游戏，检查预览并发布 grok.me 链接。</p><span class="catalog-meta">约 12 分钟 · 完成目标：完成第一个可检查、可分享的 Build Mode 项目</span></span><span class="intent-label">热点 / 教程</span></a>
  <a class="catalog-item" href="{{ '/guides/grok-imagine-video-1-5/' | relative_url }}"><span class="catalog-number">15</span><span class="catalog-copy"><strong>Grok Imagine Video 1.5 使用指南</strong><p>从图片、动作、镜头和声音提示开始，生成并验收第一段短视频。</p><span class="catalog-meta">约 14 分钟 · 完成目标：完成一次图生视频并判断失败原因</span></span><span class="intent-label">热点 / 教程</span></a>
  <a class="catalog-item" href="{{ '/guides/grok-connectors/' | relative_url }}"><span class="catalog-number">16</span><span class="catalog-copy"><strong>Grok Connectors 使用指南</strong><p>连接 Gmail、Google Drive、Outlook 与 GitHub，核对 OAuth 权限并完成第一次安全测试。</p><span class="catalog-meta">约 12 分钟 · 完成目标：连接一项服务并确认 Grok 只能访问已授权数据</span></span><span class="intent-label">使用 / 教程</span></a>
  <a class="catalog-item" href="{{ '/guides/grok-google-workspace/' | relative_url }}"><span class="catalog-number">17</span><span class="catalog-copy"><strong>Grok Google Workspace 使用指南</strong><p>安装 SpaceXAI 官方插件，在 Google Docs、Sheets 和 Slides 中完成第一次安全测试。</p><span class="catalog-meta">约 14 分钟 · 完成目标：核对权限并在测试文件中验收一次修改</span></span><span class="intent-label">办公 / 教程</span></a>
  <a class="catalog-item" href="{{ '/guides/grok-microsoft-365/' | relative_url }}"><span class="catalog-number">18</span><span class="catalog-copy"><strong>Grok Microsoft 365 使用指南</strong><p>分别安装 Word、Excel、PowerPoint 和 Outlook 插件，核对套餐、权限与组织限制。</p><span class="catalog-meta">约 16 分钟 · 完成目标：在一个 Microsoft 365 应用中完成安全测试</span></span><span class="intent-label">办公 / 教程</span></a>
</div>

## English troubleshooting guides

- [Grok User ID / UUID: How to Find and Verify It]({{ '/en/guides/grok-user-id/' | relative_url }})
- [Grok Build 403: Login, Device Auth and Subscription Checks]({{ '/en/guides/grok-build-login-403/' | relative_url }})
- [SuperGrok Card Declined: Payment Troubleshooting]({{ '/en/guides/supergrok-card-declined/' | relative_url }})
- [SuperGrok Paid but Still Free: Account and Billing Checks]({{ '/en/guides/supergrok-paid-but-still-free/' | relative_url }})

## 内容原则

- xAI、X 的套餐、模型和产品事实优先引用官方资料；
- ChongGrok 流程只按主站真实展示描述；
- User ID 与 SSO 分开说明，SSO 是临时登录凭证，不包装成零风险资料；
- 不伪造截图、用户评价、成交记录或官方合作关系；
- 不提供 API 额度、成品号、接码或批量注册内容。

<div class="resource-grid">
  <section class="resource-card"><span class="resource-icon" aria-hidden="true">01</span><h3><a href="{{ site.portal_url }}resources/ai-membership-safety-checklist/">订阅安全与验收清单</a></h3><p>付款前后通用的账号、资料和官方页面验收检查。</p></section>
  <section class="resource-card"><span class="resource-icon" aria-hidden="true">02</span><h3><a href="{{ site.portal_url }}resources/ai-subscription-payment-troubleshooting/">付款排障决策树</a></h3><p>已扣款、仍显示 Free 或购买入口不一致时按渠道分流。</p></section>
</div>

<section class="service-panel">
  <h2>服务入口</h2>
  <p>新购联合会员与旧版续费分别核对资格；本站不办理旧会员转换。有待处理订单时先查原订单，方案与交付规则以服务页为准。</p>
  <div class="hero-actions"><a class="primary-link" href="https://chonggrok.com/x-subscription?utm_source=github_guides&utm_medium=referral&utm_campaign=grok_guides_index">联合会员方案</a><a class="secondary-link" href="https://chonggrok.com/supergrok">旧版续费方案</a><a class="secondary-link" href="{{ '/' | relative_url }}">返回 Grok 首页</a></div>
</section>
