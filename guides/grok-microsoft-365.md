---
title: "Grok Microsoft 365 使用指南：安装、权限与排障"
description: "分别安装 SpaceXAI 官方 Grok for Word、Excel、PowerPoint 和 Outlook 插件，核对账号、套餐、文档权限与组织限制，并完成第一次安全测试。"
permalink: /guides/grok-microsoft-365/
schema_type: Article
date_published: 2026-08-15
last_modified_at: 2026-08-15
breadcrumbs:
  - name: "首页"
    url: /
  - name: "专题"
    url: /guides/
  - name: "Grok Microsoft 365"
    url: /guides/grok-microsoft-365/
faq:
  - question: "安装一次 Grok 后，Word、Excel、PowerPoint 和 Outlook 都能使用吗？"
    answer: "不能按一次安装理解。Microsoft Marketplace 为 Word、Excel、PowerPoint 和 Outlook 分别提供 Grok 插件；需要在哪个应用中使用，就应核对并安装对应的插件。"
  - question: "Grok Microsoft 365 插件是免费的吗？"
    answer: "Microsoft Marketplace 可以免费安装插件，但免费安装不等于免费获得全部 Grok 权益。Word、Excel、PowerPoint 和 Outlook 的当前适用套餐并不完全相同，应以各自 Marketplace 页面和 Grok 账号实时显示为准。"
  - question: "X 的付费套餐能使用所有四个 Microsoft 365 插件吗？"
    answer: "不能据此直接推断。xAI 的 Outlook 发布说明写明 Outlook 插件面向付费 X 和 SuperGrok 用户；Word、Excel 和 PowerPoint 的 Marketplace 页面当前列出的是 SuperGrok、Heavy、Business 和 Enterprise 等适用计划。请分别核对目标插件的实时页面。"
  - question: "为什么 Microsoft 365 中找不到 Grok 或无法点击添加？"
    answer: "先检查当前 Office 版本是否支持加载项、网络是否在线，以及是否登录了正确的 Microsoft 账号。公司或学校账号还可能由管理员限制 Marketplace、加载项安装或外部 AI 服务，此时应联系管理员，不要反复更换账号安装。"
  - question: "Grok Microsoft 365 插件和 Grok Connectors 是同一个功能吗？"
    answer: "不是。Microsoft 365 插件在当前打开的 Word 文档、Excel 工作簿、PowerPoint 演示文稿或 Outlook 邮件中工作；Connectors 则从 Grok 对话连接 Outlook、OneDrive、SharePoint、Google Drive 等外部服务。"
  - question: "Grok for Outlook 会自动发送邮件吗？"
    answer: "xAI 当前产品说明写明，Grok 可以起草回复，但在用户亲自发送前不会发出邮件。发送前仍应人工核对收件人、抄送、正文、附件和敏感信息。"
  - question: "不再使用时怎样移除 Grok 插件？"
    answer: "Word、Excel 和 PowerPoint 可在 My Add-ins 或加载项管理中找到 Grok 并移除；Outlook 可在 Add apps 的 Manage your apps 中移除。公司统一部署的插件可能需要管理员处理。"
---

# Grok 怎么在 Word、Excel、PowerPoint 和 Outlook 中使用？安装、权限与排障指南

**直接答案：**Grok 在 Microsoft 365 中不是一个覆盖全部应用的统一安装包。Word、Excel、PowerPoint 和 Outlook 各有独立的 Microsoft Marketplace 插件；你需要先选择一个应用，核对发布者、适用套餐和权限，再用不含敏感信息的测试文件完成第一次验证。

安装成功后，Grok 会作为侧边栏在当前文档、工作簿、演示文稿或邮件中工作。**免费安装插件不等于免费获得全部功能，也不代表一个套餐必然解锁四个插件。**实际可用性应以各插件实时页面、当前 Grok 账号和组织政策为准。

**English summary:** Grok is available as separate Microsoft 365 add-ins for Word, Excel, PowerPoint and Outlook. Verify the SpaceXAI listing, account eligibility and requested permissions for each app, then run a small non-sensitive test before using real work files.

**关键词：** `Grok Microsoft 365` · `Grok Word` · `Grok Excel` · `Grok PowerPoint` · `Grok Outlook` · `Grok Office 插件`

## 先分清三种不同入口

很多安装失败来自入口混淆。先根据工作位置选择正确功能，再继续操作。

| 你要完成的任务 | 应使用的入口 | 数据从哪里来 |
|---|---|---|
| 在当前 Word、Excel、PowerPoint 或 Outlook 中让 Grok 协助处理内容 | **Grok Microsoft 365 插件** | 当前打开的文档、工作簿、演示文稿或邮件 |
| 在 Google Docs、Sheets 或 Slides 中使用 Grok | **Grok for Google Workspace** | 当前打开的 Google 文件 |
| 从 Grok 对话中查找 Outlook、OneDrive、SharePoint、Gmail 或 Drive 内容 | **Grok Connectors** | 你单独授权的外部服务 |
| 临时分析一份文件，不需要持续访问 | **手动上传文件** | 本次对话中选择的文件 |

本文只处理第一种情况。需要 Google 办公插件时，请阅读 [Grok Google Workspace 使用指南]({{ '/guides/grok-google-workspace/' | relative_url }})；需要从 Grok 对话连接外部服务时，请阅读 [Grok Connectors 使用指南]({{ '/guides/grok-connectors/' | relative_url }})。

## 第一步：选择应用并打开对应官方页面

四款插件需要分别核对。不要从搜索结果中的相似名称直接安装。

| 应用与 xAI 介绍 | 官方安装入口 | 第一次适合测试的任务 |
|---|---|---|
| [Grok for Word](https://x.ai/grok/word) | [Microsoft Marketplace](https://marketplace.microsoft.com/en-us/product/office/WA200011055?tab=Overview) | 改写一个测试段落 |
| [Grok for Excel](https://x.ai/grok/excel) | [Microsoft Marketplace](https://marketplace.microsoft.com/en-us/product/office/WA200011056?tab=Overview) | 解释一个小型数据区域 |
| [Grok for PowerPoint](https://x.ai/grok/powerpoint) | [Microsoft Marketplace](https://marketplace.microsoft.com/en-us/product/office/WA200011057?tab=Overview) | 新增一页三点总结 |
| [Grok for Outlook](https://x.ai/grok/outlook) | [Microsoft Marketplace](https://marketplace.microsoft.com/en-us/product/office/WA200011330?tab=Overview) | 总结一封测试邮件并起草回复 |

在每个 Marketplace 页面中核对：

1. 产品名称包含目标应用，例如 `Grok by SpaceXAI for Excel`；
2. 发布者显示为 `SpaceXAI for Office`；
3. 地址栏属于 `marketplace.microsoft.com`；
4. `Works with` 或兼容产品包含你准备使用的应用；
5. 适用套餐与当前 Grok 账号一致。

任意一项不一致，都不要继续安装。

## 第二步：确认账号、套餐和测试材料

安装前准备下面五项内容：

1. **Microsoft 账号。**确认 Office 当前登录的是个人账号，还是公司或学校账号。
2. **Grok 账号。**确认稍后登录插件时应使用哪个 Grok 或 X 账号。
3. **适用套餐。**Word、Excel 和 PowerPoint 的 Marketplace 页面当前列出 SuperGrok、Heavy、Business、Enterprise 等计划；xAI 的 Outlook 发布说明则写明付费 X 和 SuperGrok 用户可用。不同插件的范围并不完全相同。
4. **测试文件。**准备一份不含客户资料、财务记录、密码、订单或私人通信的副本。
5. **恢复手段。**确认 Word、Excel 或 PowerPoint 可以撤销修改，并保存原文件副本。

如果 Marketplace 显示当前计划不适用，先停止安装。不要因为四款插件中的一款不可用，就假设另外三款也不可用；也不要在已有有效订阅或待处理订单时再次购买。

## 第三步：在 Word、Excel 或 PowerPoint 中安装

Microsoft 365 的界面会因 Windows、macOS、Web 版和版本更新而不同。Microsoft 当前提供的常见入口是 `File → Get Add-ins`，或者 `Home → Add-ins → More Add-ins`。

1. 打开准备测试的 Word 文档、Excel 工作簿或 PowerPoint 演示文稿。
2. 进入 **File → Get Add-ins**；如果没有该入口，尝试 **Home → Add-ins → More Add-ins**。
3. 搜索 `Grok`。
4. 打开与当前应用对应的结果，并再次核对发布者和兼容产品。
5. 点击 **Add / 添加**，阅读 Microsoft 显示的权限与隐私说明。
6. 安装完成后，回到 **Home / 开始**选项卡打开 Grok。
7. 侧边栏要求登录时，使用第二步确认的 Grok 账号登录一次。

**预期结果：**当前文件旁边出现 Grok 侧边栏，并且侧边栏显示的是准备使用的 Grok 账号。

**停止条件：**如果“添加”按钮被管理员禁用、页面要求管理员批准、登录后显示错误账号，或者授权页面要求把密码或验证码发给第三方，应立即停止。

## 第四步：在 Outlook 中安装

Outlook 的安装入口与 Word、Excel、PowerPoint 不同。

### 新版 Outlook

1. 打开 Outlook，并进入 **More apps / 更多应用**。
2. 选择 **Add apps / 添加应用**。
3. 搜索 `Grok`，打开 SpaceXAI for Office 发布的 Outlook 插件。
4. 阅读权限和隐私说明后点击添加。
5. 打开一封测试邮件，从邮件工具栏或 **Apps / 应用**中启动 Grok。
6. 使用准备好的 Grok 账号登录。

### 经典版 Outlook

1. 在 **Home / 开始**选项卡查找 **All Apps / 所有应用**或 **Get Add-ins / 获取加载项**。
2. 搜索并添加 Grok for Outlook。
3. 打开测试邮件，从邮件或功能区的应用入口启动 Grok。

**预期结果：**Grok 能读取当前测试邮件的上下文，并在侧边栏生成摘要或回复草稿。

**停止条件：**Outlook 处于离线状态、共享邮箱不支持当前插件、组织禁止外部加载项，或者插件要求超出任务需要的权限时，不要继续测试。

## 第五步：按应用完成第一次安全测试

四种测试只需选择当前安装的那一种。第一次任务必须小、明确且容易人工核对。

### Word：只改写一个测试段落

1. 在测试文档中选中一段不含敏感信息的文字。
2. 输入：`只把选中的段落改写得更简洁，保留所有日期和数字，不要修改其他内容。`
3. 执行前确认选区正确。
4. 完成后逐句比较原文与新内容。
5. 日期、数字或范围错误时立即撤销，不要继续处理整篇文档。

**通过标准：**只修改选中段落，文档其余部分保持不变，所有事实经人工核对。

### Excel：只分析一个小范围

1. 在测试工作簿中准备 3 至 5 行简单数据。
2. 只选择需要分析的单元格。
3. 输入：`先说明所选区域包含哪些列，再在空白列写出收入减支出的公式。不要覆盖原数据。`
4. 检查 Grok 引用的行列与当前选区是否一致。
5. 打开公式栏，手工计算一行结果进行对照。

**通过标准：**解释对应正确单元格，公式可编辑且没有覆盖原始数据。

### PowerPoint：只新增一页

1. 复制一份测试演示文稿。
2. 输入：`根据当前演示文稿的主题新增一页三点总结，不修改其他页面，不补充未经提供的数字。`
3. 检查新页面是否延续现有主题和版式。
4. 核对标题、正文、图片、图表和演讲者备注。
5. 出现虚构数字或错误来源时删除新页面，并缩小指令范围后再试一次。

**通过标准：**新增内容保持可编辑，原页面未被改动，事实和版式已经人工确认。

### Outlook：只生成回复草稿

1. 打开一封不含敏感资料的测试邮件。
2. 输入：`概括这封邮件，并起草一段确认收到的回复。不要发送，不要添加收件人或附件。`
3. 检查摘要是否对应当前邮件。
4. 检查草稿中的收件人、抄送、正文和附件区域。
5. 只有全部确认后，才由你亲自点击发送；第一次测试可以不发送。

xAI 当前说明，Grok 生成回复草稿后，不会在用户点击发送前自动发出邮件。**这并不代替人工检查。**

## 第六步：根据结果进入正确分支

| 看到的结果 | 可能原因 | 下一步 |
|---|---|---|
| Marketplace 找不到对应 Grok 插件 | Office 版本、地区、账号或组织策略不支持 | 确认使用官方链接；仍不可见时联系 Microsoft 365 管理员 |
| “添加”按钮不可用或要求管理员批准 | 公司或学校限制加载项安装 | 保存提示和官方链接，联系组织管理员 |
| 已安装，但 Home 中没有 Grok | 加载项列表未刷新或当前文件未重新打开 | 进入 My Add-ins 刷新，关闭并重新打开测试文件 |
| 侧边栏反复要求登录 | 登录了错误 Grok 账号，或会话未完成 | 关闭侧边栏，确认浏览器中的 Grok 账号后只重试一次 |
| 显示套餐不可用 | 当前账号不符合该插件的实时计划要求 | 核对该插件 Marketplace 页面；不要用另一款插件的规则代替 |
| 插件能打开，但无法修改文件 | 文件权限、组织策略或实际授权范围限制 | 确认拥有编辑权限；只在副本中重试一次 |
| Outlook 中没有入口 | Outlook 版本、离线状态、共享邮箱或组织策略限制 | 切换在线状态并核对版本；组织账号联系管理员 |
| 结果涉及错误区域或错误事实 | 选区或指令范围不明确 | 立即撤销，缩小选区并把任务改成一个动作 |

每次只改变一个条件。重复安装、连续登录或同时更换账号和套餐，会让问题更难判断。

## 权限和数据边界

Microsoft Marketplace 当前明确说明：Word、Excel 和 PowerPoint 插件可以读取或更改当前文档，并把数据发送到互联网服务。Outlook 插件的 Marketplace 页面会列出它在当前邮件上下文中可访问的信息；xAI 产品页还介绍了邮件线程总结和收件箱整理能力。

因此，授权时不要只看教程中的概括，应以 Microsoft 实时同意页面为准，并遵守以下规则：

- 第一次只处理不含敏感资料的测试文件或测试邮件；
- 不把密码、验证码、恢复码、Cookie 或 OAuth 令牌输入插件；
- 公司和学校资料必须遵守组织的 AI 与数据处理政策；
- 不需要收件箱整理时，不要扩大 Outlook 的测试范围；
- Excel 公式、PowerPoint 数字、Word 事实和 Outlook 收件人都必须人工核对；
- 安装插件不等于授权它处理组织中的全部文件，具体范围由当前文件、账号、权限和策略共同决定。

任何外部 AI 加载项都不是零风险。不确定某份资料能否交给外部服务时，应先询问组织管理员或资料所有者。

## 不再使用时怎样移除

### Word、Excel 和 PowerPoint

1. 打开 **Home → Add-ins**或 **File → Get Add-ins**。
2. 进入 **My Add-ins / 我的加载项**。
3. 找到当前应用中的 Grok。
4. 打开更多选项并选择移除。
5. 关闭并重新打开测试文件，确认侧边栏不再出现。

### Outlook

1. 进入 **More apps → Add apps**。
2. 打开 **Manage your apps / 管理你的应用**。
3. 找到 Grok，打开更多选项并选择移除。
4. 重新打开测试邮件，确认 Grok 不再出现。

管理员统一部署的插件可能无法由个人移除。此时应联系管理员，不要删除文件或邮箱来解决插件问题。

## 套餐与 ChongGrok 服务边界

Word、Excel、PowerPoint 和 Outlook 的插件都可以从 Microsoft Marketplace 安装，但它们当前列出的适用账号并不完全相同。应先核对目标插件页面和当前 Grok 账号，不要把“可以安装”理解成“已经获得使用权益”。

如果账号已有有效订阅、成功扣款或待处理订单，应先解决账号、插件或组织权限问题，不要再次购买。只有确认没有有效或待处理订阅，并且目标插件确实需要当前账号尚未具备的 SuperGrok 权益时，才可以查看 [ChongGrok SuperGrok 实时方案](https://chonggrok.com/supergrok)。ChongGrok 不需要 Microsoft 或 Grok 密码、验证码、恢复码，也不能解除公司或学校管理员设置的加载项限制。

## 完成验收清单

- [ ] 安装的是目标 Microsoft 365 应用对应的独立插件；
- [ ] Marketplace 发布者和地址已经核对；
- [ ] Microsoft 与 Grok 均使用了正确账号；
- [ ] 当前账号符合目标插件实时显示的套餐要求；
- [ ] 已阅读 Microsoft 实时显示的权限与隐私说明；
- [ ] 已在不含敏感资料的副本中完成一个小型测试；
- [ ] 修改范围、公式、数字、收件人和附件已经人工核对；
- [ ] 知道如何从当前应用移除插件；
- [ ] 没有向任何人提交密码、验证码或 OAuth 令牌。

以上项目全部确认后，再逐步把插件用于更重要的文件或邮件。

## FAQ

### 安装一次 Grok 后，Word、Excel、PowerPoint 和 Outlook 都能使用吗？

不能按一次安装理解。Microsoft Marketplace 为 Word、Excel、PowerPoint 和 Outlook 分别提供 Grok 插件；需要在哪个应用中使用，就应核对并安装对应的插件。

### Grok Microsoft 365 插件是免费的吗？

Microsoft Marketplace 可以免费安装插件，但免费安装不等于免费获得全部 Grok 权益。Word、Excel、PowerPoint 和 Outlook 的当前适用套餐并不完全相同，应以各自 Marketplace 页面和 Grok 账号实时显示为准。

### X 的付费套餐能使用所有四个 Microsoft 365 插件吗？

不能据此直接推断。xAI 的 Outlook 发布说明写明 Outlook 插件面向付费 X 和 SuperGrok 用户；Word、Excel 和 PowerPoint 的 Marketplace 页面当前列出的是 SuperGrok、Heavy、Business 和 Enterprise 等适用计划。请分别核对目标插件的实时页面。

### 为什么 Microsoft 365 中找不到 Grok 或无法点击添加？

先检查当前 Office 版本是否支持加载项、网络是否在线，以及是否登录了正确的 Microsoft 账号。公司或学校账号还可能由管理员限制 Marketplace、加载项安装或外部 AI 服务，此时应联系管理员，不要反复更换账号安装。

### Grok Microsoft 365 插件和 Grok Connectors 是同一个功能吗？

不是。Microsoft 365 插件在当前打开的 Word 文档、Excel 工作簿、PowerPoint 演示文稿或 Outlook 邮件中工作；Connectors 则从 Grok 对话连接 Outlook、OneDrive、SharePoint、Google Drive 等外部服务。

### Grok for Outlook 会自动发送邮件吗？

xAI 当前产品说明写明，Grok 可以起草回复，但在用户亲自发送前不会发出邮件。发送前仍应人工核对收件人、抄送、正文、附件和敏感信息。

### 不再使用时怎样移除 Grok 插件？

Word、Excel 和 PowerPoint 可在 My Add-ins 或加载项管理中找到 Grok 并移除；Outlook 可在 Add apps 的 Manage your apps 中移除。公司统一部署的插件可能需要管理员处理。

## 官方资料

- [xAI：Grok for Word](https://x.ai/grok/word)
- [xAI：Grok for Excel](https://x.ai/grok/excel)
- [xAI：Grok for PowerPoint](https://x.ai/grok/powerpoint)
- [xAI：Grok for Outlook](https://x.ai/grok/outlook)
- [xAI：Grok for Outlook 发布说明](https://x.ai/news/introducing-outlook-addin)
- [xAI：Grok for Word 发布说明](https://x.ai/news/introducing-word-addin)
- [Microsoft：管理 Word、Excel 与 PowerPoint 加载项](https://support.microsoft.com/en-us/office/add-ins/view-manage-and-install-add-ins-for-excel-powerpoint-and-word)
- [Microsoft：在 Outlook 中使用加载项](https://support.microsoft.com/en-us/outlook/getstarted/use-add-ins-in-outlook)

**事实核验日期：2026-08-15。**插件名称、发布者、安装入口、权限、套餐、地区与组织可用性可能变化，请以 xAI、Microsoft Marketplace、Microsoft 支持页面和当前账号实时显示为准。

{% include faq.html %}
