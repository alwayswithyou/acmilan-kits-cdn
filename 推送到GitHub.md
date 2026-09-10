# 推送到 GitHub（3 步）

仓库已在本地初始化完成：23 个文件（22 张图 + README），已 commit 并打 `v1` tag。你只需建远程仓库并推送。

## 第 1 步：在 GitHub 建仓库

打开 https://github.com/new ，按以下设置：

- **Repository name**：`acmilan-kits-cdn`
- **Public**（必须公开，否则 jsDelivr 读不到）
- **不要**勾选 "Add a README file"、"Add .gitignore"、"Choose a license"（本地已有内容，空仓库最好推）

点 Create repository。

## 第 2 步：本地推送

在 Git Bash 或 PowerShell 里执行（把 `<USER>` 换成你的 GitHub 用户名）：

```bash
cd "C:/Users/ieeen/WorkBuddy/2026-09-08-15-48-49/acmilan-cdn"

git remote add origin https://github.com/<USER>/acmilan-kits-cdn.git
git branch -M main
git push -u origin main
git push origin v1
```

> **认证提示**：GitHub 已停用密码登录。如果弹窗要求输入密码，需要改用 **Personal Access Token**：
> GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic) → Generate new token
> 勾选 `repo` 权限，生成后把 token 当作密码粘贴。

## 第 3 步：验证 CDN

推送完等 1~5 分钟让 jsDelivr 拉取缓存，然后浏览器打开：

```
https://fastly.jsdelivr.net/gh/<USER>/acmilan-kits-cdn@v1/images/02-2122-home.jpg
```

能看到球衣图就成功了。

## 之后生成排版稿

回到 `acmilan-kits` 目录，双击 **`设置用户名.bat`**，输入用户名 + 选 CDN 域名，会自动生成 `公众号排版稿_最终版.md`，里面所有图片链接都已填好。

## 第二次推送（加入交互图鉴）

仓库已新增 `gallery/`（39 张压缩图）和根目录 `index.html`（Pages 版交互图鉴），需要再推一次：

```bash
cd "C:/Users/ieeen/WorkBuddy/2026-09-08-15-48-49/acmilan-cdn"
git push origin main
```

## 开启 GitHub Pages（用于公众号「阅读原文」）

1. 打开 `https://github.com/alwayswithyou/acmilan-kits-cdn/settings/pages`
2. **Source** 选 `Deploy from a branch`
3. **Branch** 选 `main`，目录选 `/ (root)`，点 Save
4. 等约 1 分钟，访问 `https://alwayswithyou.github.io/acmilan-kits-cdn/`

这就是文章末尾「阅读原文」的永久地址，和图片 CDN 同源，不会失效。

## 国内访问速度

jsDelivr 主域名在国内部分地区不稳定。如果粘贴到公众号/头条后图片加载慢或抓取失败，换备用域名即可（路径不变，只需改域名）：

| 域名 | 说明 |
|------|------|
| `fastly.jsdelivr.net` | 推荐，国内节点多 |
| `gcore.jsdelivr.net` | 备用 |
| `testingcf.jsdelivr.net` | Cloudflare 备用 |

改法：重跑 `设置用户名.bat`，第 2 步选对应数字。
