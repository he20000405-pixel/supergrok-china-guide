---
title: "Grok Google Workspace 使用指南：Docs、Sheets 与 Slides"
description: "从 Google Workspace Marketplace 安装 SpaceXAI 官方 Grok 插件，在 Google Docs、Sheets 和 Slides 中打开侧边栏，完成第一次安全测试并排查权限、组织账号与登录问题。"
permalink: /guides/grok-google-workspace/
schema_type: Article
date_published: 2026-08-15
last_modified_at: 2026-08-15
breadcrumbs:
  - name: "首页"
    url: /
  - name: "专题"
    url: /guides/
  - name: "Grok Google Workspace"
    url: /guides/grok-google-workspace/
faq:
  - question: "Grok for Google Workspace 是免费的吗？"
    answer: "Google Workspace Marketplace 当前将这款插件标为 Free of charge，xAI 也称其可以免费安装。免费安装不等于承诺无限使用；实际功能、用量和账号可用性仍应以 Grok 账号与实时页面为准。"
  - question: "安装一次后，Google Docs、Sheets 和 Slides 都能使用吗？"
    answer: "可以。xAI 官方说明，同一个 Google Workspace 插件覆盖 Docs、Sheets 和 Slides。安装后应分别打开一个原生 Google 文件，用侧边栏完成小型测试。"
  - question: "为什么公司或学校 Google 账号不能安装 Grok？"
    answer: "Google Workspace 管理员可以限制、停用或统一部署 Marketplace 应用。页面显示需要管理员批准、应用被阻止或停用时，应停止重复安装，并联系本组织管理员核对政策。"
  - question: "Grok 已经安装，但 Docs 或 Sheets 中看不到入口怎么办？"
    answer: "先刷新当前文件，再打开扩展程序、插件、管理插件，确认 Grok 已安装并允许在该文件中使用。如果文件仍是 Microsoft Office 编辑模式，应先另存或转换为原生 Google Docs、Sheets 或 Slides 文件。"
  - question: "Grok Google Workspace 插件和 Grok Connectors 是同一个功能吗？"
    answer: "不是。Workspace 插件在当前打开的 Docs、Sheets 或 Slides 文件中工作；Connectors 从 Grok 对话连接 Gmail、Drive、Outlook、GitHub 等外部服务。只有任务需要跨服务读取资料时，才需要另外核对连接器权限。"
  - question: "安装 Grok 插件需要授予哪些 Google 权限？"
    answer: "Marketplace 当前列出的权限包括访问和编辑 Docs、Slides、已安装插件的 Sheets，以及插件使用的特定 Drive 文件；还包括运行侧边栏内容、连接外部服务和查看账号邮箱。授权前必须以 Google 同意页面实时显示为准。"
  - question: "怎样卸载 Grok Google Workspace 插件？"
    answer: "在 Google Docs、Sheets 或 Slides 中打开扩展程序、插件、管理插件，找到 Grok 后选择卸载。卸载完成后刷新文件，确认右侧栏和扩展程序菜单中不再出现 Grok。"
---

# Grok 怎么在 Google Docs、Sheets 和 Slides 中使用？安装、权限与排障完整指南

**直接答案：**打开 [Google Workspace Marketplace 的 Grok 官方页面](https://workspace.google.com/marketplace/app/grok/660927092109)，确认开发者显示为 **SpaceXAI**，阅读权限后再安装。一个插件可以在 Google Docs、Sheets 和 Slides 中使用；第一次应在不含敏感资料的副本中打开右侧 Grok 面板，只执行一项容易核对的小任务。

Google Marketplace 当前将插件标为免费，xAI 也说明可以免费安装。**免费安装不等于无限使用，也不保证每个地区、组织账号或 Grok 账号立即具备相同功能。**如果公司或学校账号要求管理员批准，应先联系管理员，不要反复切换账号安装。

**English summary:** The official Grok add-on works inside Google Docs, Sheets and Slides. Verify the SpaceXAI Marketplace listing, review the requested permissions, and test it in a non-sensitive copy before using real work files.

**关键词：** `Grok Google Workspace` · `Grok Docs` · `Grok Sheets` · `Grok Slides` · `Grok Workspace 插件` · `Grok add-on`

## 先分清：Workspace 插件、Connectors 和上传文件

这三个入口都会让 Grok 处理文件，但工作位置和授权范围不同。先选对入口，后面的安装与排障才不会混在一起。

| 你要完成的任务 | 应使用的入口 | 数据从哪里来 |
|---|---|---|
| 在当前文档中改写段落、在当前表格中写公式、在当前演示文稿中增加页面 | **Grok for Google Workspace** | 当前打开的 Docs、Sheets 或 Slides 文件 |
| 从 Grok 对话中查找 Gmail、Google Drive、Outlook 或 GitHub 内容 | **Grok Connectors** | 你单独授权的外部服务 |
| 只分析一份临时文件，不需要后续继续访问 | **手动上传文件** | 本次对话中选择的文件 |

Workspace 插件可以配合 Connectors 使用。例如，xAI 说明 Docs 中的 Grok 在启用连接器后可以引用近期邮件或 Drive 文件。但这会增加授权范围。第一次使用插件时，先不要连接其他服务，只验证当前文件。

需要跨服务读取资料时，再单独阅读 [Grok Connectors 连接器使用指南]({{ '/guides/grok-connectors/' | relative_url }})。

## 安装前准备

开始安装前，先完成下面四项准备：

1. **确认 Google 账号。**浏览器同时登录多个账号时，记住应该把插件安装到哪一个账号。
2. **判断账号类型。**个人 Google 账号通常可以自行安装；公司或学校账号可能受管理员政策限制。
3. **准备测试文件。**复制一份不含客户资料、订单、密码或个人隐私的文档、表格或演示文稿。
4. **保存原始内容。**第一次允许 Grok 修改文件前，先建立副本或确认版本记录可用。

如果无法确认当前 Google 账号，或者测试文件仍含敏感资料，应先停止安装。

## 第一步：确认是 SpaceXAI 官方插件

不要只根据搜索结果中的名称安装。请打开 [Grok - Google Workspace Marketplace](https://workspace.google.com/marketplace/app/grok/660927092109)，依次核对：

- 应用名称为 `Grok`；
- 开发者显示为 `SpaceXAI`，并链接到 `x.ai`；
- `Works with` 包含 Google Docs、Google Sheets 和 Google Slides；
- 页面当前显示 `Free of charge`；
- 地址栏域名为 `workspace.google.com`。

任意一项不一致，都不要继续安装。第三方可能使用相似名称，但名称相同不能证明开发者相同。

## 第二步：阅读权限，再完成安装

### 路径 A：从 Marketplace 直接安装

1. 在官方 Marketplace 页面点击 **Install / 安装**。
2. Google 要求确认时，选择准备使用的 Google 账号。
3. 阅读 OAuth 同意页面列出的每一项权限。
4. 只有账号和权限都符合预期时，才点击 **Allow / 允许**。
5. 等待页面显示安装完成，然后打开一份测试用的 Docs、Sheets 或 Slides 文件。

### 路径 B：从 Google 编辑器安装

1. 在电脑浏览器中打开一份 Google Docs、Sheets 或 Slides 文件。
2. 点击 **扩展程序 → 插件 → 获取插件**。
3. 搜索 `Grok`，打开开发者为 SpaceXAI 的结果。
4. 点击 **安装 → 继续**，再按上一条路径核对账号和权限。

Google Marketplace 当前列出的权限比较广，包括编辑 Docs 和 Slides、管理安装了插件的 Sheets、访问插件实际使用的特定 Drive 文件、在侧边栏运行内容、连接外部服务以及查看账号邮箱。权限文字可能调整，**最终以安装时 Google 同意页面的实时内容为准**。

如果权限超出你的工作需要，或者组织政策不允许把文件交给外部 AI，应取消安装。

## 第三步：在当前文件中打开 Grok

安装完成后，按下面的顺序检查：

1. 刷新当前 Docs、Sheets 或 Slides 页面。
2. 打开 **扩展程序 → 插件**，查找 Grok；部分界面也会在右侧边栏显示插件图标。
3. 选择 Grok，打开右侧面板。
4. 如果面板要求登录 Grok，使用准备处理当前文件的 Grok 账号完成登录。
5. 确认右侧面板已经加载，再执行下一节的小型测试。

**预期结果：**Grok 出现在当前文件旁边的侧边栏中，不需要把整个文件下载后上传到另一个网页。

**停止条件：**如果页面跳转到陌生域名、要求把 Google 或 Grok 密码发送给他人，或者当前打开的是错误账号，应立即关闭授权或登录页面。

## 第四步：按文件类型完成第一次安全测试

第一次不要直接处理正式文件。下面三种测试只需选择一种，完成并核对结果后，再逐步扩大任务范围。

### Google Docs：先改写一小段测试文字

1. 打开测试文档，并复制一段不含敏感信息的文字。
2. 在右侧 Grok 面板输入：`把第二段改写得更简洁，保留日期和数字，不要修改其他段落。`
3. 执行前确认任务范围只涉及第二段。
4. 完成后逐句比较原文和修改结果，并检查标题、列表与日期是否保持正确。
5. 结果不符合要求时使用 Google Docs 的撤销或版本记录恢复，不要继续让 Grok批量修改整篇文档。

**预期结果：**修改出现在正常的 Google Docs 内容中，仍可人工编辑、撤销和查看版本。

### Google Sheets：先解释小范围数据并写一个公式

1. 在测试表格中准备 3 至 5 行简单数据，例如月份、收入和支出。
2. 只选择这段测试区域。
3. 在 Grok 面板输入：`解释所选区域，并在空白列写出收入减支出的公式。先说明将使用哪些单元格。`
4. 检查回答是否引用了正确单元格，再查看公式栏中的实际公式。
5. 手工计算一行结果，确认公式没有引用错误列后，才考虑向下填充。

**预期结果：**Grok 的解释能够对应所选单元格，写入的内容是可查看、可修改的普通表格公式。

**停止条件：**如果 Grok引用了未选择的敏感区域、公式指向错误单元格或准备覆盖原始数据，应撤销修改并缩小选择范围。

### Google Slides：先生成一页测试幻灯片

1. 复制一份测试演示文稿，保留一个简单主题。
2. 在 Grok 面板输入：`根据这三条提纲新增一页总结，不改其他页面，不补充未经提供的数字。`
3. 完成后检查标题、正文、图表或图片来源，以及新页面是否延续现有主题。
4. 逐项核对事实；涉及网页或 X 搜索的内容，应打开原始来源确认。
5. 确认一页结果可靠后，再分批生成更多页面。

**预期结果：**新内容仍是可编辑的 Google Slides 页面，而不是只能查看的图片或导出文件。

## 第五步：根据测试结果决定下一步

| 测试结果 | 说明 | 下一步 |
|---|---|---|
| 侧边栏正常，结果只涉及选定内容 | 安装、账号和基本权限可用 | 继续使用副本，小批量扩大任务范围 |
| 插件已安装，但菜单或侧边栏中没有 Grok | 文件模式、插件状态或页面缓存可能有问题 | 按下一节的“看不到入口”流程检查 |
| 右侧面板反复要求登录 | Grok 登录、Cookie 或账号选择可能失败 | 停止重复登录，检查正确账号和浏览器设置 |
| 工作或学校账号显示管理员限制 | 组织政策阻止个人安装或使用 | 联系管理员，不要改用私人账号搬运公司资料 |
| Grok 修改了错误区域或生成了错误事实 | 任务范围不清或结果需要人工审核 | 撤销修改，缩小范围并重写指令 |

只有第一种结果适合继续处理真实工作文件。其他情况应先完成对应排障。

## 常见问题排查

### 页面显示“所在地区不可用”

Google Marketplace 应用可能受地区限制。确认当前 Google 账号和 Marketplace 页面后，仍显示不可用时，应停止重复安装。不要通过注册批量账号或伪造地区资料绕过限制。

### 页面要求管理员批准，或显示应用被阻止、停用

这是 Google Workspace 组织政策问题。保存页面提示，联系公司或学校管理员，并提供官方 Marketplace 链接。只有管理员允许或统一部署后，组织账号才能继续使用。

### 已安装，但找不到“插件”或 Grok 入口

按顺序执行：

1. 刷新当前文件；
2. 打开 **扩展程序 → 插件 → 管理插件**，确认 Grok 已安装；
3. 在 Grok 的选项中确认允许在当前文件中使用；
4. 检查当前文件是不是仍处于 Microsoft Office 编辑模式；
5. 如果看不到“插件”，将文件转换或另存为原生 Google Docs、Sheets 或 Slides 格式，再重新打开。

Google 官方说明，Office 编辑模式下可能不显示插件入口。

### Grok 侧边栏空白或登录循环

1. 确认浏览器允许当前 Google 文件正常打开；
2. 检查是否选择了错误的 Google 或 Grok 账号；
3. 暂时允许该站点所需的第三方 Cookie，再刷新一次；
4. 仍然循环时停止操作，记录浏览器版本、账号类型、发生时间和页面提示。

Google 官方提醒，部分编辑器插件在浏览器阻止第三方 Cookie 时可能无法正常工作。不要为了排障关闭整个浏览器的所有安全设置。

### 安装成功，但某个文件无法使用

先确认该文件是原生 Google 文件，并且你对文件拥有编辑权限。再打开 **管理插件**，检查 Grok 是否被关闭。如果只有一个文件异常，应在它的副本中测试；不要直接更改整个组织的权限。

## 不再使用时怎样卸载

1. 打开任意 Google Docs、Sheets 或 Slides 文件。
2. 点击 **扩展程序 → 插件 → 管理插件**。
3. 找到 Grok，打开选项并选择 **卸载**。
4. 刷新文件，确认菜单和右侧栏中不再出现 Grok。

如果使用的是公司或学校账号，管理员统一部署的插件可能无法由个人卸载。此时应联系管理员，不要删除工作文件来解决插件问题。

## 插件、Grok 账号与 SuperGrok 的边界

Marketplace 显示免费，指的是**插件可以免费安装**。它不等于承诺 Grok 功能没有用量限制，也不代表安装插件会自动升级 Grok 账号。

先在当前账号中测试实际可用功能。如果账号已经存在有效订阅、成功扣款或待处理订单，不要因为插件暂时不可用而再次购买。应先检查组织政策、登录账号和插件权限。

只有确认当前账号没有有效或待处理订阅，并且确实需要更高的 Grok 消费端使用额度时，才可以查看 [ChongGrok SuperGrok 实时方案](https://chonggrok.com/supergrok)。ChongGrok 只协助会员订阅，不需要 Google 密码、验证码、恢复码或 Workspace OAuth 令牌，也不能解除 Google 管理员设置的组织限制。

## 隐私与安全边界

- 第一次使用时只处理测试文件或正式文件的副本。
- 授权前阅读 Google 实时显示的权限，不根据教程截图直接点击允许。
- 不把 Google 或 Grok 密码、验证码、恢复码、Cookie、OAuth 令牌发给任何客服。
- 不在提示词中加入与任务无关的客户信息、订单、财务数据或私人通信。
- Sheets 公式、Slides 中的事实和 Docs 中的数字都必须人工核对。
- 公司和学校资料必须遵守组织的 AI、隐私与数据处理政策。
- 任何线上插件和第三方授权都不是零风险；不再使用时应及时卸载并检查授权。
- 本文只讨论 Grok 消费端 Google Workspace 插件，不提供 API、批量账号或地区限制规避教程。
- ChongGrok 与 SpaceXAI、xAI、X 或 Google 没有隶属、授权或官方合作关系。

## 完成验收清单

- [ ] Marketplace 页面中的开发者确认为 SpaceXAI；
- [ ] 安装时选择了正确的 Google 账号；
- [ ] 已阅读并接受实际需要的权限；
- [ ] Grok 侧边栏能在原生 Google 文件中打开；
- [ ] Grok 使用的是预期账号；
- [ ] 已在不含敏感资料的副本中完成一项小型测试；
- [ ] 已人工核对修改范围、公式和事实；
- [ ] 知道如何管理或卸载插件；
- [ ] 没有向任何人提交密码、验证码或 OAuth 令牌。

以上项目全部确认后，再把插件用于更重要的文件。

## FAQ

### Grok for Google Workspace 是免费的吗？

Google Workspace Marketplace 当前将插件标为 `Free of charge`，xAI 也称其可以免费安装。免费安装不等于承诺无限使用；实际功能、用量和账号可用性仍应以 Grok 账号与实时页面为准。

### 安装一次后，Google Docs、Sheets 和 Slides 都能使用吗？

可以。xAI 官方说明，同一个 Google Workspace 插件覆盖 Docs、Sheets 和 Slides。安装后应分别打开一个原生 Google 文件，用侧边栏完成小型测试。

### 为什么公司或学校 Google 账号不能安装 Grok？

Google Workspace 管理员可以限制、停用或统一部署 Marketplace 应用。页面显示需要管理员批准、应用被阻止或停用时，应停止重复安装，并联系本组织管理员核对政策。

### Grok 已经安装，但 Docs 或 Sheets 中看不到入口怎么办？

先刷新当前文件，再打开 **扩展程序 → 插件 → 管理插件**，确认 Grok 已安装并允许在该文件中使用。如果文件仍是 Microsoft Office 编辑模式，应先另存或转换为原生 Google Docs、Sheets 或 Slides 文件。

### Grok Google Workspace 插件和 Grok Connectors 是同一个功能吗？

不是。Workspace 插件在当前打开的 Docs、Sheets 或 Slides 文件中工作；Connectors 从 Grok 对话连接 Gmail、Drive、Outlook、GitHub 等外部服务。只有任务需要跨服务读取资料时，才需要另外核对连接器权限。

### 安装 Grok 插件需要授予哪些 Google 权限？

Marketplace 当前列出的权限包括访问和编辑 Docs、Slides、已安装插件的 Sheets，以及插件使用的特定 Drive 文件；还包括运行侧边栏内容、连接外部服务和查看账号邮箱。授权前必须以 Google 同意页面实时显示为准。

### 怎样卸载 Grok Google Workspace 插件？

在 Google Docs、Sheets 或 Slides 中打开 **扩展程序 → 插件 → 管理插件**，找到 Grok 后选择卸载。卸载完成后刷新文件，确认右侧栏和扩展程序菜单中不再出现 Grok。

## 官方资料

- [xAI：Grok in Google Workspace 发布说明](https://x.ai/news/introducing-google-workspace-addon)
- [xAI：Grok for Google Workspace 产品页](https://x.ai/grok/workspace)
- [Google Workspace Marketplace：Grok by SpaceXAI](https://workspace.google.com/marketplace/app/grok/660927092109)
- [Google：查找、安装和使用 Marketplace 应用](https://support.google.com/marketplace/answer/6067029?hl=en)
- [Google：在 Docs、Sheets 与 Slides 中安装、管理和卸载插件](https://support.google.com/docs/answer/2942256?hl=en)
- [Google：Marketplace 应用安装提示说明](https://support.google.com/marketplace/answer/12408485?hl=en)

**事实核验日期：2026-08-15。**插件名称、权限、按钮位置、地区与组织可用性可能变化，请以 SpaceXAI、xAI、Google Workspace Marketplace 和当前账号页面为准。

{% include faq.html %}
