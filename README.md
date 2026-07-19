# Personal Design Skill

一套给 AI 看的个人品牌设计系统。

把审美写成操作手册，AI 每次帮你做页面时必须翻这本手册，不能自由发挥。**限制 AI 的自由度 = 保证输出质量。**

> ⚠️ **使用前请先完成 `brand-dna.md` 的配置：** 默认品牌色可直接使用，如需替换成你自己的请同步修改模板变量；并放入你自己的头像。

---

## Demo

用这套系统生成的真实页面：

### 📖 教程型 - 分享会页面

信息清晰、步骤明确、有节奏的单页科普/教程。

🔗 [在线预览](https://esthersjw.github.io/cola-ob-sharing/cola-ob-sharing.html)

---

### 📖 教程型 - Design Skill 拆解

把审美写成操作手册——从纠正AI到做出自己的Design Skill的完整过程。

🔗 [在线预览](https://esthersjw.github.io/esther-design-system/demo-readme-tutorial.html)

---

### 🎪 活动页 / Landing

视觉冲击、深浅面板交替、强节奏感的活动邀请页。

🔗 [在线预览](https://esthersjw.github.io/esther-design-system/demo-landing.html)

---

### 📱 App 型 / 功能型

功能优先、交互感、信息密度高的应用型页面。

🔗 [在线预览](https://esthersjw.github.io/esther-design-system/demo-app.html)

---

### 📕 小红书图文卡片

3:4 比例、字大、手机可读、一键导出 PNG 的图文卡片。

🔗 [在线预览](https://esthersjw.github.io/esther-design-system/demo-cards.html)

---

### 📱 公众号排版

杂志编号风：全内联样式 + section 标签，复制粘贴进微信公众号编辑器即可。

🔗 [在线预览](https://esthersjw.github.io/esther-design-system/assets/demo-wechat.html)

---

### 📜 布局 Playground

16种经过验证的布局模式一览。

🔗 [在线预览](https://esthersjw.github.io/esther-design-system/demo-layouts.html)

---

### 🧩 组件库全览

51个经过验证的可复用组件。

🔗 [组件库预览](https://esthersjw.github.io/esther-design-system/components-preview.html)

---

## 核心逻辑

```
SKILL.md(流程 - AI 按什么步骤干活)
    ↓
brand-dna.md + references/*(规范 - 能用什么不能用什么)
    ↓
assets/template-*.html(起点 - 从模板改,不从零写)
```

- AI 不能随便发明布局 → 只能从 16 种里选
- AI 不能随便用颜色 → 只能用你定义的品牌色 + 扩展规则
- AI 不能随便写样式 → 必须从组件库里选
- AI 做完要自检 → 对照 checklist 逐条过，P0 不过就打回

---

## 文件结构

```
zephyr-design-system/
├── SKILL.md                    ← 7步工作流(大脑)
├── brand-dna.md                ← 品牌基因:颜色/字体/气质/禁忌(需配置)
├── assets/                     ← 模板骨架(起点)
│   ├── template-tutorial.html      教程页模板
│   ├── template-landing.html       活动页模板
│   ├── template-app.html           App型模板
│   ├── template-cards.html         小红书卡片模板
│   ├── html2canvas.min.js          卡片导出依赖
│   ├── avatar-placeholder.svg      占位头像(可替换为你自己的 avatar.jpg)
│   └── avatar.jpg                  ← 你的头像(需自行放入,仓库未附带)
└── references/                 ← 规则和零件(知识库)
    ├── layouts.md                  16种布局模式(附完整代码)
    ├── components.md               组件库(51组件,完整HTML+CSS)
    ├── style-library/              风格库(设计风格/案例/描述)
    ├── checklist.md                质量检查清单(P0/P1/P2)
    ├── scene-tutorial.md           教程场景规范
    ├── scene-landing.md            活动页场景规范
    ├── scene-app.md                App型场景规范
    ├── scene-cards.md              小红书卡片场景规范
    └── scene-wechat.md             公众号排版场景规范
```

---

## 8 步工作流

AI 每次做设计必须按这个顺序走：

| # | 做什么 | 为什么 |
|---|--------|--------|
| 1 | 先展示设计风格、交付类型、排版方向、字体气质菜单 | 让用户先选，不自作主张，减少无效试错 |
| 2 | 问 5 个问题(类型/风格/用途/页数/素材约束) | 明确范围 |
| 3 | 读 brand-dna + style-library + 对应场景文件 | 先学规矩再动手 |
| 4 | 从 assets/ 复制对应模板 | 从半成品开始，不从零写 |
| 5 | 从 layouts.md 选 3-5 种布局 | 每个 section 不能一样 |
| 6 | 从 components.md 选组件 | 禁止用 HTML 默认样式 |
| 7 | 对照 checklist 自检 | P0 不过就打回 |
| 8 | 交付 HTML 文件 | 浏览器打开就能看 |

---

## 风格库扩展

后续新增设计风格、参考案例和风格描述，统一放在：

```text
references/style-library/
├── styles-index.md          # 风格总表
├── style-template.md        # 新风格模板
├── example-template.md      # 设计案例模板
├── styles/                  # 单个风格说明
└── examples/                # 设计案例说明
```

当前默认风格：

- **暖纸编辑感**：亚麻米白背景、黑色排版、黄色局部高亮、少量编辑红批注、大标题、非对称、杂志式节奏。
- **极简竖版观点卡**：巨大中文标题、强留白、顶部小标签、底部短说明，适合抖音/小红书图文卡片。

---

## 品牌基因速览

### 色板（默认配色，可在brand-dna.md中替换为你自己的）

| 颜色 | 色值 | 用途 |
|------|------|------|
| 纸张底色 | `#ECE7E2` | 默认大面积背景 |
| 柔纸色 | `#F4F1EC` | 局部浅区块 |
| 深纸色 | `#E4DFDA` | Section 交替背景 |
| 半透明纸面 | `rgba(255,255,255,0.48)` | 卡片、预览块、浮层 |
| 墨色 | `#171715` | 主文字 |
| 柔墨色 | `#5B5752` | 正文、说明、辅助文字 |
| 淡墨色 | `#8A857F` | 页码、注释、弱信息 |
| 黄色 | `#F3D66F` | 荧光笔、关键词底纹、小标签、节点、局部下划线 |
| 编辑红 | `#B63A3F` | 手绘圈线、箭头、删除线、批注、小编号 |

默认逻辑：纸张底色 + 黑色排版 + 黄色局部高亮 + 少量编辑红批注。色彩占比约为纸色/中性色 90%、黄色 7%、编辑红 3%。禁止黄色整块底、整屏编辑红、粗黄色外框和多色渐变。

### 字体

| 用途 | 字体 |
|------|------|
| 大标题 | 用户选择：黑体 / 汇文明朝体 / 霞鹜文楷 / 思源宋体 |
| 副标题 | 思源宋体 / Noto Serif SC |
| 中文正文 | 用户选择：默认黑体 / 霞鹜文楷正文 |
| 英文大标题：无衬线 | Arial Narrow / Helvetica Neue / Aptos Display |
| 英文大标题：低反差衬线 | Source Serif 4 / Libre Baskerville |
| 手写/注释 | Caveat |
| 代码/终端 | Fira Code |

大标题必须让用户在黑体、汇文明朝体、霞鹜文楷、思源宋体里选择；如果同时需要展示 HTML 和卡片封面，必须分别询问展示 HTML 标题字体和卡片封面标题字体。黑体必须搭配汇文明朝体；霞鹜文楷和汇文明朝体二选一。正文默认黑体，也可以按用户要求切到霞鹜文楷正文模式。英文大标题默认用稳定无衬线，低反差衬线只作为明确选择；禁止 Didot、Bodoni、Cormorant、高反差 Fraunces 和夸张 italic。手写/批注统一 Caveat，代码、终端、API Key、命令统一 Fira Code。不同预览环境如果缺字体会 fallback，想完全一致需要安装同一字体或使用授权明确的 Web Font。

### 气质关键词（请根据你的品牌调性修改）

可爱但有品质 · 手绘蜡笔感 · 有温度 · **不像 AI** · 一看就是你的

### 禁忌

蓝紫渐变 · glassmorphism · neon · bounce 动画 · Inter/Roboto · 所有 section 居中 · 黄色整块底 · 整屏编辑红 · 粗黄色外框 · HTML 默认样式 · 看起来像 AI 生成的通用模板

---

## 质量检查

**P0(必须全过)**

纸色/中性色约90% · 黄色约7% · 编辑红约3% · 无禁忌元素 · 无 HTML 默认样式 · 灰暖纸张背景和轻微颗粒 · 衬线+无衬线混搭 · 响应式 · 每 section 布局不同 · clamp() fluid sizing · 截图发社交媒体不会被说"又是 AI 做的"

**P1(应过)**

字号对比极端 · Scroll Reveal 动效 · 非封面内容区可使用大装饰数字/英文 · 少量编辑红批注/圈线/箭头（必须指向具体内容） · 封面页禁止装饰性数字、水印数字和重复编号图形

**P2(加分)**

图片溢出容器 · 纸张质感稳定 · 装饰元素克制 · prefers-reduced-motion

---

## 怎么用

1. Fork 或克隆本仓库
2. 放入你的头像 `assets/avatar.jpg`
3. （可选）打开 `brand-dna.md`，把默认品牌色替换成你自己的，并同步修改 `assets/template-*.html` 里 `:root` 的变量。注意：公众号模板（`template-wechat.html`）全部是内联样式，没有 CSS 变量，需要手动搜索替换色值。快捷方法：在所有模板文件中搜索 `#B63A3F` 替换为你的编辑红色，`#F3D66F` 替换为你的黄色
4. 把 `assets/template-cards.html` 中的作者名替换成你自己的
5. 把仓库链接发给你的 AI Agent，跟它说：

> 帮我读这个设计系统，以后做页面按这个规范来。

核心不是这些文件本身，是**你的审美判断力**。文件只是把你的判断写成了 AI 能执行的规则。

---

## Credits

- 方法论灵感来源于 [归藏](https://github.com/guizang) 的 PPT Skill——“限制AI的自由度 = 保证输出质量”这个核心思路参考了他的设计
- Built with [Cola](https://colaos.ai) — the first OS with a soul

---

## License

[![CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

本仓库采用 [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) 协议。

- ✅ 可自由使用、修改、分享
- ✅ 必须署名：ESTHER不二 (esthersjw)
- ❌ 禁止商用
- 🔄 修改后必须以相同协议分享
