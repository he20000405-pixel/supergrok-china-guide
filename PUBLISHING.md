# SuperGrok 仓库发布与收录：新手逐步操作指南

这份说明针对下面这个仓库：

- GitHub 仓库：`https://github.com/he20000405-pixel/supergrok-china-guide`
- GitHub Pages：`https://he20000405-pixel.github.io/supergrok-china-guide/`
- 本地文件夹：`C:\Users\37132\Desktop\总chonggrok\grok\supergrok-china-guide`

## 先看你现在处于哪一步

Codex 已经完成：

- 升级 README 和 GitHub Pages 首页；
- 建立 6 篇专题文章；
- 建立 Jekyll、SEO、FAQ 结构化数据、站点地图和 `llms.txt`；
- 完成本地 Git 提交。

因此，**你现在不需要重新执行 `git add .`，也不需要重新提交核心内容。第一步直接从“推送到 GitHub”开始。**

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

正常结果应包含：

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

- Source：`Deploy from a branch`；
- Branch：`main`；
- Folder：`/(root)`。

如果已经是这些设置，不要修改。

如果不是，则选择：

1. Branch 选择 `main`；
2. Folder 选择 `/(root)`；
3. 点击 `Save`。

## 第 2 步：查看部署状态

1. 点击仓库顶部的 `Actions`；
2. 找到最新的 `pages build and deployment`；
3. 等待左侧图标变成绿色对勾。

状态含义：

- 黄色圆点：正在构建，继续等待；
- 绿色对勾：构建成功；
- 红色叉号：构建失败，先不要提交搜索引擎，把错误页面截图交给 Codex 排查。

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
3. 等待一段时间后再重新提交。

## 第 3 步：请求主页重新编入索引

1. 点击左侧“网址检查”；
2. 粘贴主页完整地址：

```text
https://he20000405-pixel.github.io/supergrok-china-guide/
```

3. 按 Enter；
4. 点击“测试实际网址”或等待检查完成；
5. 点击“请求编入索引”。

## 第 4 步：优先提交六个重要专题

按同样方式逐个检查并请求编入索引：

```text
https://he20000405-pixel.github.io/supergrok-china-guide/guides/grok-4-5-update/
https://he20000405-pixel.github.io/supergrok-china-guide/guides/supergrok-auto-recharge/
https://he20000405-pixel.github.io/supergrok-china-guide/guides/supergrok-payment-errors/
https://he20000405-pixel.github.io/supergrok-china-guide/guides/supergrok-paid-but-still-free/
https://he20000405-pixel.github.io/supergrok-china-guide/guides/grok-user-id/
https://he20000405-pixel.github.io/supergrok-china-guide/guides/grok-build-login-403/
```

这六篇分别承接热点、充值转化、付款报错、付款后未生效、User ID 和 Grok Build 403 搜索，优先级最高。其他专题已经包含在网站地图里，可以随后再提交，不必在短时间内反复请求。

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
2. 先检查主页；
3. 如果页面已经编入索引，不需要重复提交；
4. 如果是更新页面，点击“请求编制索引”；
5. 再提交 Grok 4.5、充值流程、付款报错、付款后仍显示 Free、User ID 和 Grok Build 403 六个重点专题。

Bing 显示“已成功编制索引”表示该页面已经进入 Bing 索引。网站地图显示“成功”只代表 Bing 成功读取了 URL 列表，不代表每个页面都已完成收录，这两个状态要分开看。

---

# 第七阶段：发布完成后的最终检查

全部完成后核对：

- [ ] GitHub 仓库显示新 README 和 `guides` 目录；
- [ ] GitHub Actions 的 Pages 部署为绿色；
- [ ] Pages 主页和 7 篇专题都能打开；
- [ ] `sitemap.xml` 能打开；
- [ ] `llms.txt` 能打开；
- [ ] Google Search Console 网站地图状态为成功；
- [ ] Google 已请求主页和 4 个重点页面编入索引；
- [ ] Bing 网站地图状态为成功；
- [ ] Bing 已检查主页和 4 个重点页面；
- [ ] `https://chonggrok.com/supergrok` 和 `https://chonggrok.com/verify` 链接可以正常打开。

---

# 以后新增或修改文章时怎么上传

下面这一节是以后使用的，**不是这次首次推送前必须重复执行的命令**。

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

进入 GitHub 的 `Actions` 页面，等最新部署变成绿色，再到 Google 和 Bing 提交本次新增或明显修改的 URL。

---

# 内容维护底线

- 版本、模型、价格和权益变化前先核实官方来源；
- 不把固定价格写进常青文章，统一链接主站实时页面；
- 不写 API 额度、成品号、接码或批量注册内容；
- 不承诺绝对安全、零风险、100% 不封号或固定到账时间；
- 不删除 `google3159c3cf58678847.html`；
- 截图只使用真实素材或明确标注的虚构数据示意图；
- 新专题放在 `guides/`，并从主 README、专题索引和相关页面添加内链。
