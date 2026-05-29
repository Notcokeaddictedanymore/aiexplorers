# 从0开始学AI · AI Literacy Courses for Beginners

> A bilingual, no-code AI literacy course for Chinese K-9 students across 28 hands-on missions.
>
> 为中国中小学生（4–9 年级 · 10–15 岁）打造的 AI 素养课程 —— 完全零代码、中英双语、7 章 28 关，在情景中学习。

🌐 **在线体验 / Try it live**: [aiexplorers.github.io](https://notcokeaddictedanymore.github.io/aiexplorers/welcome.html)

---

## ✨ 为什么做这个 / Why this exists

国家《中小学人工智能通识教育指南（2025 年版）》要求把 AI 素养纳入义务教育，但市面上能让 12 岁孩子真正"动手玩 AI"、又不需要任何编程基础的教材几乎没有。这门课的目标是补这个洞 —— 7 章 28 关，每关 20–40 分钟，从"AI 怎么看见熊猫"一路玩到"训练一个你自己的 AI 并办发布会"。

China's MoE 2025 AI literacy guideline mandates AI in K-9 curriculum, but few materials let a 12-year-old actually *play with AI* without any coding background. This course fills that gap — 7 chapters, 28 missions, 20–40 minutes each, from "how AI recognizes a panda" to "train your own AI and host a launch event."

---

## 🗺 课程地图 / Course map

| Ch | 主题 / Theme | 关卡 / Missions | 锚点情景 / Anchor scenario |
|----|---|---|---|
| 1 | AI 怎么看见世界 · Perception | M1-1 ~ M1-4 | 卧龙保护区 · 大熊猫识别 |
| 2 | AI 怎么思考 · Reasoning | M2-1 ~ M2-4 | 故宫文物 · 知识图谱与决策树 |
| 3 | AI 怎么学习 · Learning | M3-1 ~ M3-4 | 山西果园 · 智慧农业害虫检测 |
| 4 | AI 怎么对话 · Interaction | M4-1 ~ M4-4 | 诗仙 GPT · 方言救援 |
| 5 | AI 与人类社会 · Society | M5-1 ~ M5-4 | 信息茧房 · 深度伪造识别 |
| 6 | 暴雨中的 AI · Real-world city AI | M6-1 ~ M6-4 | 北京 2023·7·31 内涝预测与防汛 |
| 7 | 训练我的第一个 AI · Capstone | M7-1 ~ M7-4 | 选问题 → 收数据 → 训练 → 发布 |

每一章遵循 **热身 → 探索 → 挑战 → 反思** 节奏，全部任务结束后颁发 *"AI 少年研究员"* 结业证书。

---

## 🚀 快速开始 / Quick start

**给学生 / For students:**
1. 打开 `welcome.html`
2. 按「接受任务」进入课程地图
3. 从 M1-1 开始 —— 进度自动保存在浏览器，下次接着玩

**给老师 / For teachers:**
课程不需要安装、不需要服务器、不需要账号 —— 任何一台能开浏览器的设备就能用。把 `welcome.html` 通过 USB / 学校内网 / GitHub Pages 分发给学生即可。

**本地运行 / Run locally:**
```bash
git clone https://github.com/Notcokeaddictedanymore/aiexplorers.git
cd aiexplorers
# 直接双击 welcome.html，或开 8000 端口（推荐，避免 localStorage 跨文件问题）
python3 -m http.server 8000
# 浏览器访问 http://localhost:8000/welcome.html
```

---

## 🛠 技术栈 / Tech stack

完全前端单文件 HTML，零构建步骤 / Pure single-file HTML, zero build step:

- **样式 / Styling**: Tailwind CSS（CDN 引入）+ 自定义 CSS
- **交互 / Interactivity**: 原生 JavaScript（无框架）
- **状态保存 / State**: `localStorage`（每关进度独立 key，无后端）
- **训练真实 AI / Real AI training**: Google Teachable Machine（M7-3 推荐）
- **多语言 / i18n**: `data-zh` / `data-en` 双 span + CSS 切换
- **导师角色 / Mentor**: 小京灵 (Jingling) —— 蓝色全息精灵，苏格拉底式提问

---

## 📚 课程对齐 / Aligned with

- **AI4K12 Five Big Ideas** (USA, AAAI + CSTA)
- **中国教育部《中小学人工智能通识教育指南（2025 年版）》** —— 知识 / 技能 / 思维 / 价值观 4 维
- **UNESCO K-12 AI Curricula Framework**

---

## 📂 文件结构 / File structure

```
aiexplorers/
├── welcome.html              # 影院级入口页（深空 + 地球 + 接受任务）
├── index.html                # 章节看板（7 章卡片 + 进度条 + 徽章）
├── lingxi-avatar.png         # 小京灵头像（吉祥物）
│
├── m1-1-intro.html ~ m1-4-cost.html        # Ch.1 感知（大熊猫）
├── m2-1-graph.html ~ m2-4-labels.html       # Ch.2 推理（故宫）
├── m3-1-data.html ~ m3-4-owner.html         # Ch.3 学习（果园）
├── m4-1-poet.html ~ m4-4-dialect.html       # Ch.4 对话（诗仙 GPT）
├── m5-1-recsys.html ~ m5-4-citizen.html     # Ch.5 社会（信息茧房）
├── m6-1-rainstorm.html ~ m6-4-warning.html  # Ch.6 城市 AI（北京暴雨）
├── m7-1-pick.html ~ m7-4-launch.html        # Ch.7 毕业作品
│
├── 00-README-从这里开始.md
├── PRD-AI互动学习课程-完整产品规划.md         # 完整产品规划文档
└── 01-课程地图-Course-Map.html               # 一页式视觉地图
```

每个任务页面都是单一 HTML 文件，包含全部 CSS + JS + SVG，不依赖任何外部资源（除了 Tailwind CDN）。

---

## 🎯 设计理念 / Design philosophy

1. **零代码** —— 12 岁的孩子打开浏览器就能开始，不需要 Python / Jupyter / 任何安装
2. **场景驱动** —— 每个 AI 概念都锚定在真实情景（保护区、博物馆、果园、城市防汛），不是抽象公式
3. **批判性思维** —— 小京灵故意会"幻觉"，让学生学会质疑 AI；每章都有反思关，谈伦理 + 局限
4. **本土化** —— 大熊猫不是猫，故宫不是 Louvre，方言救援针对中国少数民族语言，防汛针对北京真实事件
5. **自由探索** —— 任何时候按 ESC 退出回地图，已完成的关卡可点回看复习，没有线性强制

---

## 🤝 贡献 / Contributing

欢迎老师、家长、同龄学生提 issue 或 PR：

- 发现某关卡逻辑 bug？开 issue 描述复现步骤
- 想加新章节 / 新关卡？先开 issue 讨论思路
- 想翻译成其他语言（粤语、英语强化、繁体）？欢迎 PR
- 想做真人测试？欢迎在 Discussions 里贴反馈

**请不要 PR：** 把单文件拆成多文件（违背项目"零部署"哲学）、引入 React/Vue 等框架（违背"零构建"哲学）。

---

## 🙋 关于作者 / About the author

**开发者 · Developer:** 辜月晗 / Gu Yuehan —— 12 岁北京中学生，零编程基础的产品经理。课程由 12 岁学生 + Claude 共同设计共建。

This course was designed and built collaboratively by **Gu Yuehan** (12-year-old middle schooler in Beijing) and **Claude** (Anthropic's AI assistant). The 12-year-old chose every scenario, vetted every interaction, and tested every mission with peers.

---

## 📜 许可证 / License

[MIT License](LICENSE) —— 你可以自由使用、修改、传播、商用。只需保留版权声明。

教学使用、改编成本地化版本、纳入学校课程都欢迎。如果你做了有趣的衍生版，请在 Discussions 里贴个链接给我看看 🎓

---

## 🌟 致谢 / Credits

- **Google AI Quests** —— 课程结构和单关时长（45 min）的灵感来源
- **Anthropic Claude** —— 课程内容设计协作伙伴
- **Google Teachable Machine** —— M7-3 真实训练 AI 的零代码工具
- **AI4K12 Initiative** —— Five Big Ideas 框架
- **中国教育部 2025 AI 通识指南** —— 课程对齐基准
- 所有最早愿意测试 alpha 版的 12 岁同学和老师们 🙇

---

<sub>从0开始学AI · v1.0 · 2026 · Made with ❤️ in Beijing</sub>
