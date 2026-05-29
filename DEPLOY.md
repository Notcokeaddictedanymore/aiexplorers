# 🚀 部署到 GitHub Pages · Deployment Guide

完整指南：从本地项目 → GitHub 仓库 → 公开访问 URL，约 5 分钟。

---

## 前提准备 / Prerequisites

1. ✅ GitHub 账号 `Notcokeaddictedanymore` 已登录浏览器
2. ✅ 本机已安装 `git`（macOS 默认装了，命令行输 `git --version` 验证）
3. ✅ 已创建空仓库：[github.com/Notcokeaddictedanymore/aiexplorers](https://github.com/Notcokeaddictedanymore/aiexplorers)
   - 如果还没建：去 https://github.com/new 建一个 **空仓库**，名字 `aiexplorers`，**不要勾** "Add a README"
4. ✅ 准备好 `lingxi-avatar.png` 放在项目根目录（可选 —— 没有也能跑，会显示 🧚‍♀️ fallback）

---

## 步骤 1 · 在 Terminal 进入项目目录

打开 macOS **终端（Terminal）**，运行：

```bash
cd "/Users/jianggu/Documents/Claude/Projects/AI Interactive Learning Experience"
```

---

## 步骤 2 · 初始化 git 仓库 + 首次提交

复制下面整段贴进终端，回车：

```bash
# 初始化 git 仓库
git init

# 配置作者（如果之前没设过）
git config user.name "Gu Yuehan"
git config user.email "jiang.gu@icloud.com"

# 把 main 设为默认分支
git branch -M main

# 加入所有文件（.gitignore 已经过滤掉无关文件）
git add .

# 首次提交
git commit -m "🎓 v1.0 — Initial release: 28 missions across 7 chapters

- Welcome page with AI Quests-inspired cosmic entry
- 28 single-file HTML missions (Chinese K-9 AI literacy)
- Bilingual ZH/EN with localStorage progress
- Game-feel: +100 XP popups, badge animations, confetti
- Navigation: home button, ESC shortcut, step-dot replay
- Mobile-responsive (375px+ tested)
- Aligned with AI4K12 + China MoE 2025 + UNESCO

Co-built by Gu Yuehan (12 yo PM) and Claude."
```

---

## 步骤 3 · 关联 GitHub 远程并推送

```bash
# 添加远程仓库
git remote add origin https://github.com/Notcokeaddictedanymore/aiexplorers.git

# 推送（第一次可能弹出 GitHub 登录授权窗口，按提示完成）
git push -u origin main
```

**如果推送报错 `git@github.com: Permission denied`** 或类似：

- 改用 HTTPS（已经是 HTTPS 了，应该不会有问题）
- 或安装 [GitHub CLI](https://cli.github.com/)：`brew install gh && gh auth login`，然后再推送

---

## 步骤 4 · 开启 GitHub Pages

1. 浏览器打开：https://github.com/Notcokeaddictedanymore/aiexplorers/settings/pages
2. **Build and deployment** 区域：
   - **Source**: 选 `Deploy from a branch`
   - **Branch**: 选 `main`，文件夹选 `/ (root)`
   - 点 **Save**
3. 等 1–2 分钟，刷新页面，顶部会显示绿色 URL：
   ```
   https://notcokeaddictedanymore.github.io/aiexplorers/
   ```

---

## 步骤 5 · 测试公开访问

打开两个链接确认：

- 入口页：`https://notcokeaddictedanymore.github.io/aiexplorers/welcome.html`
- 章节看板：`https://notcokeaddictedanymore.github.io/aiexplorers/index.html`

第一次访问 GitHub Pages 可能需要 1–3 分钟生效。如果访问 404，等一会儿再试。

---

## 步骤 6 · 添加仓库 description + topics（让别人能搜到）

回到 https://github.com/Notcokeaddictedanymore/aiexplorers，点页面右上角 ⚙️ **About** 旁边的齿轮：

**Description（一句话英文介绍）：**
```
A bilingual, no-code AI literacy course for Chinese K-9 students across 28 hands-on missions.
```

**Website:**
```
https://notcokeaddictedanymore.github.io/aiexplorers/welcome.html
```

**Topics（GitHub 搜索标签，按 Enter 添加）：**
```
ai-literacy
education
k12
chinese-education
no-code
interactive-learning
ai4k12
teachable-machine
bilingual
middle-school
primary-school
```

保存。

---

## 🎉 完成

- 仓库公开 URL：https://github.com/Notcokeaddictedanymore/aiexplorers
- 课程入口：https://notcokeaddictedanymore.github.io/aiexplorers/welcome.html

---

## 后续更新 / Updating later

每次改了文件想推到 GitHub：

```bash
cd "/Users/jianggu/Documents/Claude/Projects/AI Interactive Learning Experience"
git add .
git commit -m "描述你这次改了什么"
git push
```

GitHub Pages 通常 30 秒内自动重新部署。

---

## 常见问题 / FAQ

**Q：推送时报错 "fatal: not a git repository"**
A：你没在项目目录里。先 `cd "/Users/jianggu/Documents/Claude/Projects/AI Interactive Learning Experience"`。

**Q：GitHub 让我输入用户名密码，但密码错了**
A：GitHub 2021 年起不接受密码，要用 **Personal Access Token**。最简单：安装 GitHub CLI `brew install gh`，然后 `gh auth login`。

**Q：Pages 上线后中文字体看起来不对**
A：检查浏览器是否有 "PingFang SC" / "Microsoft YaHei" / "Source Han Sans CN"。如果学校电脑没装，可以在 README 后续版本里引入 Google Fonts 的 Noto Sans SC。

**Q：能不能用自定义域名（如 0xAI.fun）？**
A：能。GitHub Pages 设置里有 **Custom domain** 选项，配上 CNAME 记录即可。Cloudflare 免费的二级域名也行。

**Q：lingxi-avatar.png 没准备好，发出去会怎样？**
A：所有页面会显示 🧚‍♀️ emoji + 紫蓝渐变圆 fallback，不会报错。你后续随时补传即可。

---

<sub>从0开始学AI · Deploy Guide v1.0 · 2026</sub>
