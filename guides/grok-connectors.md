---
title: "Grok Connectors：连接 Gmail、Drive、Outlook 与 GitHub"
description: "从 Grok 技能和连接器页面完成 OAuth 授权，连接 Gmail、Google Drive、Outlook 或 GitHub，并通过只读任务验证账号、权限和数据范围。"
permalink: /guides/grok-connectors/
schema_type: Article
date_published: 2026-08-15
last_modified_at: 2026-08-15
breadcrumbs:
  - name: "首页"
    url: /
  - name: "专题"
    url: /guides/
  - name: "Grok Connectors"
    url: /guides/grok-connectors/
faq:
  - question: "使用 Grok Connectors 必须订阅 SuperGrok 吗？"
    answer: "不必须。xAI 官方 Connectors 文档说明，连接器向所有 Grok 用户开放。不同账号的使用额度和功能可用性可能不同，应以当前账号页面为准；不要因为暂时看不到入口就重复购买订阅。"
  - question: "连接 Gmail 或 Outlook 需要把邮箱密码交给 Grok 吗？"
    answer: "不需要。正确流程会从 Grok 官方页面跳转到 Google 或 Microsoft 的 OAuth 授权页面，由用户自己登录并核对权限。不要把邮箱密码、验证码、恢复码或 OAuth 令牌发送给客服或其他人。"
  - question: "为什么 Grok 中找不到某个连接器？"
    answer: "先在 grok.com/connectors 搜索连接器名称，并检查当前 Grok 账号和应用版本。Business 或 Enterprise 团队还需要管理员先为组织启用连接器；Microsoft 工作或学校账号也可能要求管理员批准。"
  - question: "连接后为什么 Grok 仍然找不到邮件或文件？"
    answer: "先确认 OAuth 授权时选择了正确的外部账号，再用文件名、邮件主题、发件人或日期范围执行一次具体的只读查询。如果仍无结果，检查权限是否包含读取范围，并断开后重新连接一次。"
  - question: "Grok Connectors 可以发送邮件或修改文件吗？"
    answer: "取决于连接器和实际授权权限。部分连接器先提供只读权限，写入、发送或修改能力可能需要额外权限或组织管理员启用。第一次测试应只读，不要直接发送邮件、删除文件或修改日历。"
  - question: "怎样彻底断开 Grok 与 Google 或 Microsoft 账号？"
    answer: "先在 grok.com/connectors 找到对应连接器并选择 Disconnect。需要进一步撤销时，再到 Google 账号的第三方访问权限页面或 Microsoft My Apps 页面移除 Grok 的授权。"
---

# Grok Connectors 怎么用？连接 Gmail、Google Drive、Outlook 与 GitHub 完整流程

**直接结论：**打开 [grok.com/connectors](https://grok.com/connectors)，选择一个连接器，再在 Google、Microsoft、GitHub 等服务自己的授权页面完成 OAuth 授权。第一次连接后只做一项只读测试，确认 Grok 使用的是正确账号、能够找到指定数据，并且没有获得任务以外的权限。

xAI 官方说明，**Connectors 向所有 Grok 用户开放**，因此看不到入口不等于必须先购买 SuperGrok。先检查登录账号、应用版本和组织权限；已有有效订阅或待处理订单时，不要再次购买。

**English summary:** Grok Connectors let users access email, calendars, cloud files, repositories and other authorized services inside a Grok conversation. Connect one service at a time, review the OAuth permissions, and begin with a read-only test.

**关键词：** `Grok Connectors` · `Grok 连接器` · `Grok Gmail` · `Grok Google Drive` · `Grok Outlook` · `Grok GitHub`

## 先理解连接器是什么

连接器是一条由你授权的数据通道。授权完成后，Grok 可以在对话中按你的问题搜索邮件、读取云端文件、查看日历或检查代码仓库。它与手动上传文件不同：上传只提供当前选中的文件，连接器可以在你已授权的服务中继续查找相关内容。

连接器不会替你判断哪些资料可以交给 AI。连接前仍要确认三个问题：

1. 当前 Grok 登录的是不是你准备使用的账号；
2. 授权页面显示的是不是正确的 Google、Microsoft 或 GitHub 账号；
3. 页面申请的读取、写入或发送权限是否符合当前任务。

任意一项不一致，都应退出授权页面，不要继续点击允许。

## 按任务选择第一个连接器

第一次不要同时连接多个服务。先从最容易验证的一项任务开始：

| 你想完成的任务 | 选择的连接器 | 第一次安全测试 |
|---|---|---|
| 查找并总结邮件 | Gmail 或 Outlook Mail | 查找一封不含敏感信息的测试邮件，只让 Grok 概括主题 |
| 查看未来安排 | Google Calendar 或 Outlook Calendar | 只读取未来 7 天的测试日程，不创建或删除事件 |
| 分析云端文件 | Google Drive 或 OneDrive | 按准确文件名找到一份测试文档并生成摘要 |
| 查看代码项目 | GitHub | 概括一个公开或测试仓库的 README、Issue 或 Pull Request |
| 查找团队资料 | SharePoint、Teams、Notion 等 | 先选择非敏感页面，并确认组织管理员已经允许使用 |

当前 Grok Web 的“技能和连接器”页面还列出 Box、Canva、Notion、Vercel、Wix 等目录连接器。具体名称和排序可能调整，应以 [Grok Connectors 实时页面](https://grok.com/connectors)为准。

## 连接前准备四项内容

开始授权前，先完成以下准备：

- **准备一个可识别的测试对象。**例如标题为“Connector Test”的邮件或文件。
- **确认外部账号。**如果浏览器同时登录多个 Google 或 Microsoft 账号，先记住应该选择哪一个。
- **确定只读还是写入。**第一次只验证搜索和读取，不发送邮件、不修改文件、不删除内容。
- **关闭无关页面。**授权过程中不要把密码、验证码、恢复码或支付信息粘贴进 Grok 对话。

这样做可以把问题缩小为一条清晰链路：连接是否成功、账号是否正确、读取权限是否有效。

## 第一步：进入“技能和连接器”页面

### 网页端

1. 使用准备连接外部服务的 Grok 账号登录 [grok.com](https://grok.com)。
2. 在左侧导航进入“技能和连接器”，或直接打开 [grok.com/connectors](https://grok.com/connectors)。
3. 确认页面顶部显示“技能和连接器”，并切换到“连接器”区域。
4. 点击“新连接器”，然后选择 Gmail、Google Drive、Outlook、GitHub 或其他目标服务。

xAI 早期发布说明也提到，可以在聊天输入框旁的 `+` 菜单中选择 Connectors，再添加连接器。界面位置可能变化，但授权目标应始终是同一个 Grok 官方连接器页面。

如果页面要求重新登录，先确认地址栏域名仍为 `grok.com`。如果出现陌生域名、要求把密码发给第三方，或要求下载未知程序，应立即停止。

### iOS 和 Android

xAI 官方发布页给出的移动端入口是：

1. 打开 Grok App；
2. 进入 `Settings / 设置`；
3. 选择 `Connectors / 连接器`；
4. 选择需要连接的服务。

如果 App 中没有该入口，先更新应用，再用网页端核对。入口暂时不可见不是重复购买会员的理由。

## 第二步：在服务商页面完成 OAuth 授权

OAuth 是一种授权方式：你在 Google、Microsoft 或 GitHub 自己的页面登录并确认权限，Grok 不需要获得你的邮箱密码。

以 Gmail 为例，完整流程如下：

1. 在 Grok 的连接器列表中选择 Gmail。
2. 点击“连接”。
3. 浏览器跳转到 Google 登录或授权页面后，检查地址栏是否属于 Google 官方域名。
4. 选择真正需要授权的 Google 账号。
5. 阅读权限说明，确认当前任务只需要哪些读取或写入能力。
6. 同意后返回 Grok，等待连接状态更新。

Google Calendar、Google Drive、Outlook 和 GitHub 的逻辑相同：**先从 Grok 发起，再在服务商自己的页面确认账号和权限，最后返回 Grok。**

在以下情况中应停止授权：

- 页面中的外部账号不是目标账号；
- 申请的权限明显超过当前任务需要；
- 工作或学校账号显示“需要管理员批准”；
- 页面要求通过聊天发送密码、验证码或令牌；
- 返回 Grok 后没有出现已连接状态，却反复要求重新授权。

遇到管理员批准提示时，应联系本单位管理员。不要改用个人账号绕过组织的数据管理规则。

## 第三步：完成第一次只读测试

连接状态显示正常后，新建一段 Grok 对话，只测试一个明确对象。

### Gmail 或 Outlook 测试

可以输入：

> 在我已连接的邮箱中查找主题包含“Connector Test”的最新一封邮件。只告诉我发件人、日期和两句话摘要，不要回复、转发、删除或修改邮件。

正确结果应满足：找到指定邮件、没有混入其他账号内容、没有执行写入操作。

### Google Drive 或 OneDrive 测试

可以输入：

> 在我已连接的云盘中查找文件名为“Connector Test”的文档。告诉我文件标题、最后修改时间和三点摘要，不要修改、移动或删除文件。

如果 Grok 找到多个同名文件，应先让它列出文件位置，再由你选择，不要让它自行修改任何一份。

### Google Calendar 或 Outlook Calendar 测试

可以输入：

> 查看未来 7 天标题包含“Connector Test”的日程，只列出日期、时间和标题，不要创建、修改或取消事件。

### GitHub 测试

可以输入：

> 使用已连接的 GitHub，打开仓库 owner/repository，只概括 README 的用途，并列出当前打开的 3 个 Issue 标题。不要创建 Issue、评论或修改代码。

测试成功后，再逐步增加任务范围。不要在第一次测试中同时要求“读取邮件、修改日历、更新文档并发送通知”，否则失败时无法判断是哪一步出错。

## 第四步：根据结果判断下一步

| 看到的结果 | 说明 | 下一步 |
|---|---|---|
| 找到正确数据，且没有执行写入 | 账号和基础读取权限正常 | 保留连接器，再逐项测试需要的能力 |
| 找到的是另一个账号的数据 | OAuth 时选择了错误账号 | 立即断开，撤销权限后用正确账号重连 |
| 显示已连接，但找不到测试对象 | 查询条件、账号或读取权限不匹配 | 用准确标题和日期重试一次，再检查授权范围 |
| 能读取，但不能发送或修改 | 当前只有只读权限，或写入能力未启用 | 只有任务确实需要时才申请额外权限 |
| 显示需要管理员批准 | 组织策略阻止个人启用 | 联系 Business/Enterprise 管理员或 Microsoft 管理员 |
| 连接后持续报错 | 连接状态或服务暂时异常 | 保存报错和时间，停止反复授权，再检查 xAI 状态或支持入口 |

每次只改变一个条件。例如先改查询关键词，再检查账号，最后才考虑重连。这样可以避免把账号、权限和服务故障混为一谈。

## 常见故障的排查顺序

### 1. 列表中没有目标连接器

1. 直接打开 [grok.com/connectors](https://grok.com/connectors)。
2. 点击“新连接器”，用英文名称再次搜索。
3. 检查 Grok App 是否为当前版本。
4. 如果是 Business 或 Enterprise 团队账号，询问管理员是否已经在团队控制台启用该连接器。

上述步骤仍找不到时，记录账号类型、平台、应用版本和缺失的连接器名称，再联系 xAI。不要为了获得一个入口重复购买订阅。

### 2. 授权后仍然显示未连接

1. 确认授权页面最后是否返回 Grok。
2. 刷新一次连接器页面。
3. 查看 Google、Microsoft 或 GitHub 账号的第三方授权列表中是否出现 Grok。
4. 如果外部账号已有授权、Grok 仍显示未连接，先撤销旧授权，再从 Grok 发起一次新的连接。

只重连一次。仍失败时保存原始报错，不要连续重复授权。

### 3. 已连接但 Grok 没有使用连接器

1. 在问题中明确写出“使用已连接的 Gmail / Google Drive / GitHub”。
2. 给出可验证的文件名、邮件主题、仓库名或日期范围。
3. 确认测试对象确实属于授权账号。
4. 检查当前对话是否显示连接器被调用或是否返回权限错误。

如果普通聊天能够回答，却没有引用你的私有数据，不应假设它已经访问连接器。应以能否找到指定测试对象作为验收标准。

### 4. Microsoft 提示需要管理员批准

Outlook 和 Outlook Calendar 可能使用工作或学校账号。组织可以要求管理员先批准 Grok 应用权限。出现此提示时：

1. 不要反复登录；
2. 保存提示页面和申请的权限名称；
3. 联系组织的 Microsoft Entra / Azure AD 管理员；
4. 等管理员批准后再从 Grok 重新发起连接。

这属于组织权限问题，个人用户无法通过充值或更换浏览器解决。

## 怎样断开并撤销权限

不再使用连接器时，建议同时检查 Grok 和外部服务两端。

### 在 Grok 中断开

1. 打开 [grok.com/connectors](https://grok.com/connectors)。
2. 找到已经连接的服务。
3. 选择 `Disconnect / 断开连接`。
4. 刷新页面，确认状态不再显示已连接。

### 在 Google 中撤销

打开 [Google 账号第三方访问权限](https://myaccount.google.com/permissions)，找到 Grok 或对应授权项并移除访问权限。

### 在 Microsoft 中撤销

打开 [Microsoft My Apps](https://myapps.microsoft.com)，在账号的应用权限中找到对应授权并撤销。工作或学校账号的选项可能由管理员控制。

断开后，再用刚才的测试问题询问一次。Grok 不应再能找到该账号中的测试邮件、文件或日程。

## 个人账号与团队账号的区别

个人用户可以从 Grok 的连接器页面连接自己的服务。Business 和 Enterprise 团队则多一层组织控制：管理员先在团队控制台启用连接器，团队成员才能连接自己的账号。

因此，团队成员看不到连接器时，应先询问管理员，而不是重新注册个人账号。管理员启用连接器也不等于自动获得每位成员的数据；成员仍需使用自己的外部账号完成授权。

## Connectors 与 SuperGrok 的关系

xAI Connectors 总览明确写明，连接器向所有 Grok 用户开放。SuperGrok 可能提供更高的消费端使用额度，但不应把“能否连接 Gmail 或 Drive”写成必须购买会员才能使用。

如果你已经确认当前账号没有有效订阅、没有待处理订单，并且确实需要更高的 Grok 使用额度，可以查看 [ChongGrok SuperGrok 实时方案](https://chonggrok.com/supergrok)。ChongGrok 的订阅协助不需要邮箱密码，也不需要 Google、Microsoft 或 GitHub 的 OAuth 令牌；用于会员核销的 Grok User ID 与连接器授权是两件不同的事。

## 隐私与安全边界

- 只在 `grok.com` 发起连接，并在服务商官方域名完成登录和授权。
- 第一次只使用不含敏感信息的测试邮件、测试文件或测试仓库。
- 权限范围以 OAuth 页面实时显示为准；不需要写入时不要启用发送、删除或修改权限。
- 不把邮箱密码、验证码、恢复码、OAuth 令牌或 GitHub Token 发给任何客服。
- xAI 官方连接器文档说明其不会使用 Gmail、Google Calendar、Google Drive 或 Outlook 连接器数据训练模型，并说明这些数据按请求实时访问；具体处理仍应以最新官方隐私说明为准。
- 目录中的第三方连接器可能有自己的服务条款和隐私政策，授权前应分别核对。
- 任何线上授权都不是零风险；不再使用时应主动断开并撤销权限。
- 本文只讨论 Grok 消费端连接器，不提供自定义 MCP、API 额度或 API 接入教程。
- ChongGrok 与 xAI、X、Google、Microsoft、GitHub 不存在隶属、授权或官方合作关系。

## 完成验收清单

- [ ] Grok 和外部服务均使用了正确账号；
- [ ] 授权发生在服务商官方页面；
- [ ] 已阅读并确认权限范围；
- [ ] 只读测试能够找到指定对象；
- [ ] 测试没有发送、删除或修改内容；
- [ ] 知道如何在 Grok 和外部账号中撤销授权；
- [ ] 没有向任何人提交密码、验证码、恢复码或 OAuth 令牌。

只有以上项目都确认后，才适合把连接器用于真实工作资料。

## 官方资料

- [xAI：Grok Connectors 总览](https://docs.x.ai/grok/connectors)
- [xAI：Connectors in web, iOS, and Android](https://x.ai/news/grok-connectors)
- [xAI：Gmail & Google Calendar Connector](https://docs.x.ai/grok/connectors/gmail-google-calendar)
- [xAI：Google Drive Connector](https://docs.x.ai/grok/connectors/google-drive)
- [xAI：Outlook Mail & Calendar Connector](https://docs.x.ai/grok/connectors/outlook)
- [xAI：Business / Enterprise Connector Management](https://docs.x.ai/grok/connector-management)

**事实核验日期：2026-08-15。**连接器名称、按钮位置、权限和套餐规则可能调整，请以 Grok 账号实时页面及 xAI 最新官方文档为准。

{% include faq.html %}
