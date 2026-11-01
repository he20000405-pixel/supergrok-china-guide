# SuperGrok 仓库发布与收录：新手逐步操作指南

这份说明针对下面这个仓库：

- GitHub 仓库：`https://github.com/he20000405-pixel/supergrok-china-guide`
- GitHub Pages：`https://he20000405-pixel.github.io/supergrok-china-guide/`
- 本地文件夹：`C:\Users\37132\Desktop\总chonggrok\grok\supergrok-china-guide`

## 当前维护与首次发布说明

仓库目前已上线。下面保留首次发布时的操作步骤与输出示例，不代表当前仍待首次推送；日常更新请使用文末“以后新增或修改文章时怎么上传”。实际分支、待提交文件和待推送提交以本次 `git status` 为准，本地路径以当前工作目录为准。

当前专题范围以 `/guides/` 和 `sitemap.xml` 为准，不沿用首次发布时的固定文章数量。

---

# 第一阶段：把本地升级内容推送到 GitHub

## 第 1 步：打开 PowerShell

1. 按键盘上的 Windows 键；
2. 输入 `PowerShell`；
3. 点击“Windows PowerShell”；
4. 不需要“以管理员身份运行”。

新窗口通常会显示类似：

```text
PS C:\Users\37132>
```

## 第 2 步：进入 Grok 仓库文件夹

复制下面整行命令，粘贴到 PowerShell，然后按 Enter：

```powershell
Set-Location 'C:\Users\37132\Desktop\总chonggrok\grok\supergrok-china-guide'
```

正常情况下，命令行左侧会变成：

```text
PS C:\Users\37132\Desktop\总chonggrok\grok\supergrok-china-guide>
```

如果仍显示 `C:\Windows\system32` 或其他文件夹，先不要执行后面的 Git 命令，重新复制上面的 `Set-Location` 命令。

## 第 3 步：确认仓库状态

执行：

```powershell
git status
```

首次发布时已有一条待推送提交的输出示例（当前状态以实际结果为准）：

```text
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
nothing to commit, working tree clean
```

解释：

- `On branch main`：当前在正确的主分支；
- `ahead ... by 1 commit`：本地升级已经完成，但还没上传；
- `working tree clean`：没有漏掉未提交文件。

## 第 4 步：推送到 GitHub

执行：

```powershell
git push origin main
```

正常结果最后通常类似：

```text
To https://github.com/he20000405-pixel/supergrok-china-guide.git
   8931d81..新的提交编号  main -> main
```

只要最后出现：

```text
main -> main
```

就表示上传成功。

如果显示：

```text
Everything up-to-date
```

表示内容已经上传过，不需要重复推送。

---

# 第二阶段：如果推送出现 403 权限错误

只有出现下面这种错误时才执行本阶段：

```text
Permission to he20000405-pixel/supergrok-china-guide.git denied to usehe
fatal: unable to access ... 403
```

这表示 Git 误用了旧账号 `usehe` 的登录凭据，不是仓库文件出错。

## 第 1 步：查看 GitHub 凭据账户

执行：

```powershell
git credential-manager github list
```

## 第 2 步：重新登录正确账号

执行：

```powershell
git credential-manager github login --username he20000405-pixel --browser --force
```

随后浏览器会打开 GitHub 授权页面：

1. 确认页面右上角登录的是 `he20000405-pixel`；
2. 如果显示 `usehe`，先退出该账号，再登录 `he20000405-pixel`；
3. 完成 Git Credential Manager 的授权；
4. 回到 PowerShell。

## 第 3 步：重新推送

```powershell
git push origin main
```

不要再执行 `git remote add origin ...`。当前仓库已经有 `origin`，重复添加只会显示：

```text
error: remote origin already exists.
```

---

# 第三阶段：确认 GitHub 仓库已经更新

## 第 1 步：打开仓库

浏览器访问：

`https://github.com/he20000405-pixel/supergrok-china-guide`

## 第 2 步：检查三个位置

1. 仓库首页 README 标题应变为“2026 SuperGrok 国内充值指南”；
2. 文件列表中应出现 `guides`、`_layouts`、`_includes`、`assets` 等目录；
3. 最新提交信息应显示：

```text
Upgrade SuperGrok guide with Grok 4.5 content cluster
```

这三项都正常，说明 GitHub 仓库内容已经更新。

---

# 第四阶段：确认 GitHub Pages 自动部署

原仓库已经启用 GitHub Pages，一般不需要重新创建 Pages。

## 第 1 步：检查 Pages 设置

1. 打开仓库；
2. 点击顶部的 `Settings`；
3. 点击左侧的 `Pages`；
4. 找到 `Build and deployment`。

应当显示：

- Source：`GitHub Actions`；
- 使用仓库内的发布前检查工作流；
- `github-pages` 部署环境仅允许 `main`。

具体规则见 [发布前检查说明](.github/PUBLISHING-CHECKS.md)。如果已经是这些设置，不要改回分支直接发布。

如果仍使用分支发布，应将 `Source` 切换为 `GitHub Actions`，并确认上述工作流与部署环境规则已配置。

## 第 2 步：查看部署状态

1. 点击仓库顶部的 `Actions`；
2. 找到本次提交对应的发布前检查工作流运行；
3. 确认 `main` 的正常运行依次通过 `verify` → `release-ready` → `deploy`。`release-ready` 是无权限哨兵任务，依赖 `verify` 成功。

PR 和 `ci-check` 测试分支只验收，不发布。只有 `main` 的正常检查通过后才部署同一次运行已检查的产物；检查失败时不执行发布，线上保留上一次成功版本。

状态含义：

- 黄色圆点：正在构建，继续等待；
- 绿色对勾：对应任务成功；只有本次 `deploy` 成功才代表已完成部署；
- 红色叉号：检查或部署失败，查看对应任务日志排查，不要切回分支发布来绕过检查。

## 第 3 步：逐个打开公开页面

先打开主页：

`https://he20000405-pixel.github.io/supergrok-china-guide/`

再检查这些地址：

```text
https://he20000405-pixel.github.io/supergrok-china-guide/guides/
https://he20000405-pixel.github.io/supergrok-china-guide/guides/supergrok-auto-recharge/
https://he20000405-pixel.github.io/supergrok-china-guide/guides/grok-user-id/
https://he20000405-pixel.github.io/supergrok-china-guide/guides/supergrok-plans/
https://he20000405-pixel.github.io/supergrok-china-guide/guides/supergrok-payment-errors/
https://he20000405-pixel.github.io/supergrok-china-guide/guides/supergrok-paid-but-still-free/
https://he20000405-pixel.github.io/supergrok-china-guide/guides/supergrok-vs-x-premium-plus/
https://he20000405-pixel.github.io/supergrok-china-guide/guides/grok-4-5-update/
https://he20000405-pixel.github.io/supergrok-china-guide/en/
https://he20000405-pixel.github.io/supergrok-china-guide/sitemap.xml
https://he20000405-pixel.github.io/supergrok-china-guide/llms.txt
```

判断标准：

- 主页和专题显示正常排版，不是 404；
- `sitemap.xml` 能显示 XML 内容；
- `llms.txt` 显示英文文本列表。

浏览器显示纯文本或 XML 不代表出错，`llms.txt` 和 `sitemap.xml` 本来就不是普通文章页面。

---

# 第五阶段：Google Search Console 收录

这是原来的同一个 GitHub Pages 站点，所以通常不需要重新创建资源，也不需要重新验证所有权。原验证文件 `google3159c3cf58678847.html` 已保留。

## 第 1 步：打开正确的站点资源

进入 Google Search Console，在左上角选择：

```text
https://he20000405-pixel.github.io/supergrok-china-guide/
```

不要误选 ChatGPT 仓库的资源。

## 第 2 步：提交或检查网站地图

1. 点击左侧“站点地图”；
2. 在“添加新的站点地图”输入框中只填写：

```text
sitemap.xml
```

3. 点击“提交”。

如果列表中已经存在 `/sitemap.xml`，不需要反复新增，打开它查看状态即可。

正常状态最终应显示“成功”。如果刚推送后显示“无法抓取”：

1. 先在浏览器确认 `sitemap.xml` 地址能够打开；
2. 确认 GitHub Pages 的 Actions 已经是绿色；
3. 查看地图错误详情，并通过实际网址测试核对 Google 抓取结果；确认问题已修复或需要重试后提交一次，记录状态与读取时间，不反复删除重提。浏览器能打开和 Actions 成功不能单独证明 Google 已读取地图。

## 第 3 步：核对主页索引状态

1. 点击左侧“网址检查”；
2. 粘贴主页完整地址：

```text
https://he20000405-pixel.github.io/supergrok-china-guide/
```

3. 按 Enter；
4. 点击“测试实际网址”或等待检查完成；
5. 仅在未收录且实际测试可抓取、允许索引，或主页有重要更新时，按后台配额请求编入索引；已收录且未变时不重复请求。

## 第 4 步：优先提交六个重要专题

下列地址是历史重点示例。当前按专题目录与站点地图整理完整规范 URL 清单，逐篇检查实际索引状态，优先正文页面；再按需要请求编入索引：

```text
https://he20000405-pixel.github.io/supergrok-china-guide/guides/grok-4-5-update/
https://he20000405-pixel.github.io/supergrok-china-guide/guides/supergrok-auto-recharge/
https://he20000405-pixel.github.io/supergrok-china-guide/guides/supergrok-payment-errors/
https://he20000405-pixel.github.io/supergrok-china-guide/guides/supergrok-paid-but-still-free/
https://he20000405-pixel.github.io/supergrok-china-guide/guides/grok-user-id/
https://he20000405-pixel.github.io/supergrok-china-guide/guides/grok-build-login-403/
```

这六个地址是首次发布时的重点专题示例，不代表当前全部文章或固定提交优先级。对未收录且实际测试可抓取、允许索引的页面，以及本次新增或重要更新的页面，按后台配额请求；技术阻碍先修复，已收录且未变或已请求待处理的 URL 不作无意义重复提交。

逐篇记录 Google 选择的规范地址、最后抓取时间、索引状态、核查时间、证据和请求结果。受限、配额不足、等待处理的页面保留待办；地图提交成功、地图读取成功与文章已索引分别验收。

“已请求编入索引”不等于马上能在 Google 搜到。Google 仍会自行决定抓取和收录时间。

---

# 第六阶段：Bing Webmaster Tools 收录

如果这个 Grok 站点之前已经从 Google Search Console 导入，**不需要再填写 Bing 验证码**。

## 第 1 步：确认选对站点

进入 Bing Webmaster Tools，在左上角选择：

```text
https://he20000405-pixel.github.io/supergrok-china-guide/
```

## 第 2 步：检查网站地图

1. 点击左侧“网站地图”；
2. 如果没有网站地图，提交完整地址：

```text
https://he20000405-pixel.github.io/supergrok-china-guide/sitemap.xml
```

3. 如果已经存在，查看“状态”和“已发现的 URL”。

正常结果：

- 状态显示“成功”；
- 已发现的 URL 不为 0。

## 第 3 步：提交重点 URL

1. 点击左侧“URL 检查”；
2. 按当前专题清单逐篇检查实际索引与抓取状态，优先正文，再检查主页等入口；
3. 如果页面已经编入索引且没有重要更新，不重复提交；
4. 对未收录且实际测试可抓取、允许索引，或本次新增、重要更新的页面，按后台配额请求编制索引；
5. 记录逐篇核查时间、证据与请求结果；已提交待处理的 URL 不作无意义重复请求，受限、配额不足、等待处理保留待办，不照搬首次发布时的固定列表。

Bing 显示“已成功编制索引”表示该页面已经进入 Bing 索引。网站地图显示“成功”只代表 Bing 成功读取了 URL 列表，不代表每个页面都已完成收录，这两个状态要分开看。

---

# 第七阶段：发布完成后的最终检查

全部完成后核对：

- [ ] GitHub 仓库显示新 README 和 `guides` 目录；
- [ ] 本次 `main` 的 `verify`、`release-ready` 和 `deploy` 均成功；
- [ ] Pages 主页及当前 `/guides/`、`sitemap.xml` 中的全部专题都能打开；
- [ ] `sitemap.xml` 能打开；
- [ ] `llms.txt` 能打开；
- [ ] Google Search Console 网站地图状态为成功；
- [ ] Google 已核对本次重点页面的索引状态，并按需请求编入索引；
- [ ] Bing 网站地图状态为成功；
- [ ] Bing 已检查本次重点页面；
- [ ] `https://chonggrok.com/supergrok` 和 `https://chonggrok.com/verify-grok` 链接可以正常打开。

---

# 以后新增或修改文章时怎么上传

下面这一节用于已上线仓库的日常更新；先检查实际修改，再提交和推送。

## 第 1 步：进入仓库

```powershell
Set-Location 'C:\Users\37132\Desktop\总chonggrok\grok\supergrok-china-guide'
```

## 第 2 步：查看修改

```powershell
git status
```

## 第 3 步：把修改加入待提交列表

```powershell
git add .
```

如果这里出现 `LF will be replaced by CRLF` 或 `CRLF will be replaced by LF`，通常是换行格式提示，不是上传失败。继续执行 `git status`，确认文件已经出现在 `Changes to be committed` 下。

## 第 4 步：创建提交

把引号里的文字换成本次修改内容，例如：

```powershell
git commit -m "Update Grok payment error guide"
```

## 第 5 步：推送

```powershell
git push origin main
```

## 第 6 步：等待 Pages 自动更新

进入 GitHub 的 `Actions` 页面，确认本次 `main` 的 `verify`、`release-ready` 和 `deploy` 均成功并检查公开页面，再到 Google 和 Bing 提交本次新增或明显修改的 URL。

---

# 内容维护底线

- 版本、模型、价格和权益变化前先核实官方来源；
- 不把固定价格写进常青文章，统一链接主站实时页面；
- 不写 API 额度、成品号、接码或批量注册内容；
- 不承诺绝对安全、零风险、100% 不封号或固定到账时间；
- 不删除 `google3159c3cf58678847.html`；
- 截图只使用真实素材或明确标注的虚构数据示意图；
- 新专题放在 `guides/`，并从主 README、专题索引和相关页面添加内链。
