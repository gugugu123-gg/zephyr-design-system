# Brand DNA — 品牌基因

> ⚠️ **使用前请确认配置：** 下面是默认纸张编辑风色板，可直接使用。如需换成你自己的品牌色，替换色值并同步修改模板 `:root` 变量。头像、气质关键词也请替换成你自己的。

---

## 🎨 默认色板

| 色名 | 色值 | 用途 |
|------|------|------|
| `--paper` | `#ECE7E2` | 页面主背景，默认大面积使用 |
| `--paper-light` | `#F4F1EC` | 局部浅色区块、卡片内层 |
| `--paper-deep` | `#E4DFDA` | Section 交替背景、轻微压暗的纸面 |
| `--surface` | `rgba(255,255,255,0.48)` | 卡片、预览块、浮层 |
| `--ink` | `#171715` | 主标题、正文、主要信息 |
| `--ink-soft` | `#5B5752` | 正文、说明、辅助文字 |
| `--ink-faint` | `#8A857F` | 页码、注释、弱信息 |
| `--yellow` | `#F3D66F` | 荧光笔高亮、关键词底纹、小标签、节点、局部下划线 |
| `--red` | `#B63A3F` | 手绘圈线、箭头、删除线、批注、小编号、极少量警示 |
| `--line` | `rgba(23,23,21,0.10)` | 分割线、卡片边界 |

色彩占比：纸色与中性色约 90%，黄色约 7%，编辑红约 3%。

同一个 section 通常只使用黄色或编辑红中的一种；特殊情况下允许两个同时出现，但二者都不能成为大面积结构背景。

### CSS变量

```css
:root {
  --paper: #ECE7E2;
  --paper-light: #F4F1EC;
  --paper-deep: #E4DFDA;

  --ink: #171715;
  --ink-soft: #5B5752;
  --ink-faint: #8A857F;

  --yellow: #F3D66F;
  --red: #B63A3F;

  --line: rgba(23,23,21,0.10);
  --surface: rgba(255,255,255,0.48);
}
```

---

## 👤 头像/IP形象

请将你的头像文件放入 `assets/avatar.jpg`（建议正方形，至少 400×400px）。

如果你有完整IP形象（全身/半身），放入 `assets/character.png`。

### 使用规则
- 需要头像时优先用 `assets/avatar.jpg`
- 是否在页面中使用IP形象由你决定，不强制

---

## 🔤 字体基因

### 核心原则
- **大标题字体必须让用户选择** — 默认提供黑体、汇文明朝体、霞鹜文楷、思源宋体四个方向，不让浏览器 fallback 自己决定气质
- **展示 HTML 与卡片封面分开选字体** — 如果一个任务同时需要展示 HTML 和卡片封面，必须问两次：展示 HTML 标题字体一次，卡片封面标题字体一次。
- **字体搭配有硬限制** — 黑体必须搭配汇文明朝体作为强调或副标题；霞鹜文楷和汇文明朝体在同一封面或首屏里只能二选一，不能同时作为主要标题字体。
- **正文默认黑体，但可让用户选择霞鹜文楷正文模式** — 科普、教程、功能页默认无衬线黑体；卡片、叙事页、轻松解释页可以选择霞鹜文楷正文
- **中英文搭配** — 英文做装饰/标签，中文承载内容
- **字号对比极端** — 大的要很大，小的要真的小
- **宋体/明朝体克制使用，文楷按用户选择使用** — 思源宋体、汇文明朝体不要大面积铺开；霞鹜文楷可作为标题字体，也可在用户明确选择时作为正文模式

### 推荐字体池

| 场景 | 推荐 | 备注 |
|------|------|------|
| 英文大标题：无衬线 | `Arial Narrow` / `Helvetica Neue` / `Aptos Display` | 默认选择，适合 Agent、API、AI 等英文概念词，不抢中文标题 |
| 英文大标题：低反差衬线 | `Source Serif 4` / `Libre Baskerville` | 只在需要更安静的编辑感时使用 |
| 手写/注释 | `Caveat` | 手绘感、标注、批注、提示语 |
| 代码/终端 | `Fira Code` | 代码块、终端、API Key、文件名、命令 |
| 大标题：黑体 | `Source Han Sans SC` / `Noto Sans SC` / 系统黑体 | 强观点、教程封面、行动型内容；必须搭配汇文明朝体做副标题或局部强调 |
| 大标题：文楷 | `LXGW WenKai`（霞鹜文楷） | 亲近、手写、适合科普解释和图文卡片 |
| 大标题：明朝 | `Huiwen Mincho`（汇文明朝体） | 更复古、文学、档案感；只在需要这个语气时使用 |
| 大标题：思源宋体 | `Source Han Serif SC` / `Noto Serif SC` | 干净、编辑感、较稳 |
| 副标题 | `Source Han Serif SC`（思源宋体）/ `Noto Serif SC` | 用于短副标题、引语、解释性短句 |
| 正文/UI 默认 | `Source Han Sans SC` / `Noto Sans SC` / 系统黑体 | 默认无衬线，长正文、按钮、导航、标签优先用这一类 |
| 正文：文楷模式 | `LXGW WenKai`（霞鹜文楷） | 用户明确选择时可用于正文，适合轻松解释、图文卡片、叙事内容；不用于高密度后台和复杂表格 |
| 情绪短句/卡片封面 | `LXGW WenKai`（霞鹜文楷）/ `Caveat` | 用于卡片封面、旁白、签名、轻松批注，不承担长正文 |

### 全局字体变量

所有模板和新页面都应优先使用这组变量，不要在页面里临时发明英文、手写或代码字体。

```css
:root {
  --font-cn-title-sans: "Source Han Sans SC", "思源黑体", "Noto Sans SC", "Microsoft YaHei", sans-serif;
  --font-cn-title-wenkai: "LXGW WenKai", "霞鹜文楷", "Noto Serif SC", serif;
  --font-cn-title-mincho: "Huiwen Mincho", "汇文明朝体", "Noto Serif SC", serif;
  --font-cn-title-serif: "Source Han Serif SC", "思源宋体", "Noto Serif SC", "Songti SC", serif;
  --font-cn-body-sans: "Source Han Sans SC", "思源黑体", "Noto Sans SC", "Microsoft YaHei", sans-serif;
  --font-cn-body-wenkai: "LXGW WenKai", "霞鹜文楷", "Source Han Sans SC", "Noto Sans SC", sans-serif;

  /* 默认模式：大标题文楷，正文黑体。用户可按场景覆盖这两个变量。 */
  --font-title: var(--font-cn-title-wenkai);
  --font-body: var(--font-cn-body-sans);

  --font-en-title-sans: "Arial Narrow", "Helvetica Neue", "Aptos Display", Arial, sans-serif;
  --font-en-title-serif: "Source Serif 4", "Libre Baskerville", Georgia, serif;
  --font-en-display: var(--font-en-title-sans);
  --font-hand: "Caveat", "Comic Sans MS", cursive;
  --font-code: "Fira Code", "Cascadia Code", "Consolas", monospace;
}

.en-display {
  font-family: var(--font-en-display);
  font-style: normal;
  font-weight: 700;
  letter-spacing: -0.04em;
}

.hand-note {
  font-family: var(--font-hand);
}

code,
pre,
kbd,
.mono {
  font-family: var(--font-code);
}
```

### 字体模式选择

生成页面前必须让用户选择，或根据内容明确默认：

| 变量 | 可选值 | 适合 |
|------|--------|------|
| `--font-title` | `var(--font-cn-title-sans)` | 强观点、教程封面、行动型标题；必须搭配汇文明朝体作为强调或副标题 |
| `--font-title` | `var(--font-cn-title-wenkai)` | 默认推荐。亲近、解释感、图文卡片感 |
| `--font-title` | `var(--font-cn-title-mincho)` | 复古、档案、文学、时间感 |
| `--font-title` | `var(--font-cn-title-serif)` | 现代编辑感、正式说明、杂志标题 |
| `--font-body` | `var(--font-cn-body-sans)` | 默认推荐。教程、功能页、长正文、导航按钮 |
| `--font-body` | `var(--font-cn-body-wenkai)` | 用户明确选择时使用。轻松科普、叙事、图文卡片、口播稿展示 |

如果用户说“标题用霞鹜文楷，正文也用霞鹜文楷”，应设置：

```css
:root {
  --font-title: var(--font-cn-title-wenkai);
  --font-body: var(--font-cn-body-wenkai);
}
```

### 字体渲染差异说明

同一个 HTML 在不同浏览器或预览环境里可能显示成不同字体，原因通常是本机字体可用性不同。CSS 会按 `font-family` 顺序查找：第一个字体找不到，就使用后面的 fallback。要让不同环境完全一致，必须确保目标字体已安装，或使用授权明确的 Web Font / 本地字体文件；不要提交来源不明或授权不清的字体文件。

### 字体使用限制

- 生成展示 HTML 前必须确认展示 HTML 标题字体；同时生成卡片封面时必须再确认卡片封面标题字体，两者不能默认共用一次选择。
- 字体选项固定为黑体、汇文明朝体、霞鹜文楷、思源宋体。
- 黑体必须搭配汇文明朝体作为强调或副标题；霞鹜文楷和汇文明朝体在同一封面或首屏里只能二选一，不能同时作为主要标题字体。
- 普通网页中，汇文明朝体最多用于一页中的一个主要大标题；霞鹜文楷可用于大标题，也可在用户明确选择时用于正文。
- 竖版观点卡中，霞鹜文楷可以连续用于多个封面标题、情绪短句或核心观点句，但不承担长正文。
- 思源宋体适合副标题、短引语和少量强调，不用于大段正文。
- 霞鹜文楷适合卡片封面、情绪标题、旁白批注和签名；用户明确选择时可作为正文模式，但要检查长段落可读性。
- 正文、列表、说明文字、按钮、导航、表格默认使用黑体无衬线；若用户选择文楷正文，按钮、导航和表格仍优先保留黑体。
- 英文大标题默认使用稳定无衬线：`Arial Narrow`、`Helvetica Neue`、`Aptos Display`；`Agent`、`API`、`AI` 这类概念词优先用无衬线，避免抢中文标题。
- 英文低反差衬线只使用 `Source Serif 4` 或 `Libre Baskerville`，用于更安静的编辑标题或引文。
- 禁止使用 Didot、Bodoni、Cormorant、高反差 Fraunces、夸张 italic 作为英文大标题或全局英文装饰。
- 手写批注一律用 Caveat，不把 Caveat 用作正文或大段解释。
- 代码、终端、API Key、文件名和命令一律用 Fira Code，不用普通正文黑体。
- 如果一个页面已经大量使用文楷或手写字体，就不要再叠加太多明朝体/宋体。
- 字体的作用是建立层级，不是为了堆“设计感”。

### 字号系统（fluid sizing）
- Hero大标题: `clamp(2.8rem, 7vw, 5.5rem)`
- Section标题: `clamp(1.6rem, 4vw, 2.6rem)`
- 卡片标题: `1.15rem ~ 1.4rem`
- 正文: `16px`
- 辅助文字: `0.78rem ~ 0.85rem`
- 大装饰数字: 只允许用于非封面内容区或章节页；封面页/首屏禁止使用装饰性数字、水印数字和重复编号图形。

---

## ✨ 气质关键词

设计出来的东西应该让人觉得：

- **可爱但有品质** — 不是幼儿风也不是奢侈风
- **手绘蜡笔感** — 有温度、有人味
- **不像AI** — 这是最高优先级的约束
- **有设计师眼光** — 细节讲究、间距精确、色彩克制
- **温暖但不幼稚** — 有内容有深度
- **个人品牌感** — 一看就知道是"你的"

> 💡 请根据你自己的品牌调性修改上面的关键词。

---

## 🎨 配色扩展原则

配色扩展时：

- 所有页面默认使用灰暖纸张背景，不使用纯白或明显偏黄的奶油底。
- 背景必须有非常轻微的纸张颗粒或纤维质感，但纹理不得抢眼。
- 视觉效果优先依赖排版、字号、字重、对齐和留白，不依赖大面积色块。
- 黄色只用于荧光笔高亮、关键词底纹、小标签、节点和局部下划线。
- 编辑红只用于手绘圈线、箭头、删除线、批注、小编号和极少量警示。
- 红色批注元素只用于指出信息，不用于纯装饰。红圈必须圈住真实内容，不能悬空圈空白；如果没有明确对象可圈，改用短下划线、小箭头或直接删除。
- 封面页/首屏只保留必要小标签文本，禁止使用装饰性数字、水印数字和重复编号图形；不要在封面卡片或首屏背景放淡色编号当装饰。
- 黄色与编辑红不得同时大面积出现；红色永远只是点缀，不做主背景。
- 绝不用纯黑 `#000` 或纯白 `#fff` 作为大面积底色。
- 不提交来源不明或授权不明确的纸纹图片；需要更真实纸感时可使用授权明确的透明纸纹 PNG。

### 已删除的颜色方向

不再使用蓝色、青蓝色、冷绿色、粉色、橙色、紫色和多色渐变。代码中不要保留 `--blue`、`--blue-deep`、`--cyan`、`--spruce`、`--marker-blue`、`--marker-green`、`--marker-pink`、`--marker-orange`、`--marker-amber` 这类变量；如旧模板需要迁移，统一改为 `--yellow` 或 `--red`。

---

## 🚫 通用禁忌清单

| 类型 | 禁止 |
|------|------|
| 配色 | 蓝紫渐变、neon、纯黑白、AI常用的冷灰蓝调、橙色、多套辅助色同时出现、任何多色渐变背景、黄色整块底、整屏编辑红色背景 |
| 深色版面 | 默认不用深色大底；需要节奏变化时优先用墨色，且只做少数特殊 section |
| 字体 | Inter/Roboto/Arial等overused字体（除非明确是终端风格辅助字体）、monospace充当"技术感" |
| 布局 | 所有section居中、千篇一律卡片网格、cards嵌套cards |
| 动效 | bounce/elastic、animate width/height、无限循环动画 |
| 装饰 | glassmorphism、圆角矩形+阴影千篇一律、渐变文字、AI光效、border-left 竖线引用块（类似 Notion/飞书的左侧竖条引用样式） |
| 整体 | 看起来像AI生成的通用模板、generic Landing Page模板感 |
| 边框 | 粗黄色外框、四边彩色包围、依靠彩色边框强行制造设计感 |
| 排版 | 行间距/字间距必须肉眼检查，不允许出现过松或过紧的异常节奏 |
| 图片 | AI生成的stock photo风、过度滤镜、无意义装饰图 |
| 默认样式 | HTML默认blockquote、默认border-left引用块、无样式ul/ol列表、默认table——所有组件必须从components.md选用，绝不允许浏览器默认渲染 |

### 自检问题
做完设计后问自己：
1. 这个页面截图发到社交媒体，会不会被人评论"又是AI做的"？
2. 能不能一眼认出这是你的品牌？
3. 有没有哪个部分让你觉得"见过很多次了"？

---

## 📐 通用间距原则

- Section之间: `clamp(80px, 12vh, 160px)`
- 内容块之间: `clamp(40px, 6vw, 100px)`
- 卡片内padding: `clamp(28px, 3vw, 44px)`
- 元素间gap: `clamp(24px, 3vw, 48px)`
- 全部用 `clamp()` 做fluid sizing
- `max-width: 1300px` + `margin: 0 auto` 约束内容宽度

---

## 🧾 卡片风格原则

使用整体式信息卡，而不是多层嵌套小框。卡片允许中等圆角，但必须克制，避免过圆、过软、过可爱。主要依靠留白、分区、细分隔线和局部批注建立层级，而不是依赖大量边框。

推荐变量：

```css
:root {
  --card-radius: 22px;
  --card-visual-radius: 20px;
  --card-tag-radius: 14px;
  --card-border: 1px solid rgba(23, 23, 21, 0.08);
  --card-shadow: none;
  --card-padding: clamp(32px, 3vw, 40px);
  --card-row-gap: clamp(24px, 2.5vw, 28px);
}
```

- 主卡片圆角用 `22px`。
- 图片或顶部视觉区圆角用 `20px`。
- 小标签圆角用 `14px`，不要使用过软的胶囊形，除非它是很小的功能标签。
- 边框用 `1px solid rgba(23,23,21,0.08)`。
- 阴影很弱或不用，禁止重漂浮感。
- 卡片内边距控制在 `32px ~ 40px`，行与行之间控制在 `24px ~ 28px`。
- 内部层级优先用分区、细分隔线、字号和留白，不堆小卡片，不用大量边框。
- 一句话标准：一个整体卡片，轻微圆角，克制边框，大留白，内部用分区而不是小卡片堆叠；有一点亲和感，但整体仍偏编辑感和信息感。

---

## 📱 响应式通用规则

- 断点: 900px（两栏→单栏）、600px（字号微缩）
- 移动端是"重新排列"不是"缩小"
- 尊重 `prefers-reduced-motion`
- 移动端不隐藏内容——adapt不amputate

---

## 🔍 细节规范

- **选中文本高亮**: `::selection { background: 你的强调色; color: #1a1a1a; }`
- **链接悬停**: 用强调色底色块或下划线，不用变色

---

*This is the foundation. Every scene file builds on top of this.*
