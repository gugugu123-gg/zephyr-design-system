---
name: zephyr-design-system
description: 基于 ESTHER 不二设计系统改造的个人 Design Skill。做HTML页面、个人网站、教程页面、介绍页面、landing page、图文卡片等前端设计时自动触发。包含品牌DNA、风格库和多个场景子规范。
---

> © 2026 ESTHER不二 (esthersjw) | CC BY-NC-SA 4.0
> 使用本 Skill 需署名原作者，禁止商用，修改后须以相同协议分享。
> Repo: https://github.com/gugugu123-gg/zephyr-design-system

触发条件：当用户要求制作HTML网页、个人页面、教程页面、介绍型页面、landing page、活动页面、App型页面、作品集等任何前端设计相关任务时触发。也在用户说"做图文"、"图文卡片"、"小红书图文"、"文章转卡片"、"转成图文"、"做卡片"时触发。

## 使用方式（8步工作流）

### Step 1: 先给用户选择菜单
在动手前，先告诉用户本 Skill 当前支持哪些设计方式和排版方式，不要直接开始写页面。

目的：先引导用户做选择，避免直接产出造成 token 浪费，也避免用户因为审美疲劳不喜欢最终方向。

硬规则：

- 用户没有明确指定风格/排版时，不得直接开始写完整 HTML。
- 必须先给用户一个简短菜单，让用户选择或确认。
- 菜单只展示主要方向，不要把所有组件细节一次性倒给用户。
- 用户选择后，再进入模板、布局、组件组合。

必须展示：

1. **设计风格** — 读取 `references/style-library/styles-index.md`，展示可选风格。默认风格是「暖纸编辑感」。
2. **交付类型** — 教程/介绍/科普、活动页/Landing、App型/功能型、图文卡片、公众号排版。
3. **主要排版方向** — 从 `references/layouts.md` 中概括 5-8 个主要布局方向给用户选，例如大标题海报型、左右双栏型、编辑式错位排版、编号章节型、卡片组合型、Sticky滚动叙事型、深浅纸面交替型、时间轴/流程型。若是图文卡片，必须额外让用户在「封面型 / 信息型 / 图文型 / 混合组卡」中选择。
4. **字体气质** — 必须让用户选择展示 HTML 的标题字体；如果任务还包含卡片封面，必须再单独让用户选择一次卡片封面字体，不能用一次选择同时覆盖两种产物。字体选项固定为：黑体 / 汇文明朝体 / 霞鹜文楷 / 思源宋体。搭配规则：黑体必须搭配汇文明朝体作为强调或副标题；霞鹜文楷和汇文明朝体只能二选一，不能在同一封面或首屏里同时作为主要标题字体。正文模式仍需确认：默认黑体无衬线 / 霞鹜文楷正文。英文大标题默认使用稳定无衬线（Arial Narrow / Helvetica Neue / Aptos Display），低反差衬线（Source Serif 4 / Libre Baskerville）只作为明确选择；禁止 Didot、Bodoni、Cormorant、高反差 Fraunces 和夸张 italic。手写/批注统一使用 Caveat，代码/终端/API Key/命令统一使用 Fira Code。

如果用户已经明确给了参考图或指定“照这个模子”，优先按用户给的模子，不再自由发挥。

### Step 2: 澄清需求
向用户确认5个问题：
1. **类型** — 教程/介绍/科普？活动页/Landing？App型/功能型？**图文卡片？** **公众号排版？**
2. **设计风格** — 使用哪个 `style-library` 风格？是否有参考案例？如果是抖音/小红书竖版卡片，优先展示「极简竖版观点卡」。
3. **受众和用途** — 给谁看的？发在哪里？阅读还是传播？
4. **Section数/页数** — 大概几屏、几页或几张卡片？
5. **素材与硬约束** — 有哪些文案/图片/数据？必须包含什么？
6. **字体选择** — 展示 HTML 标题字体从黑体 / 汇文明朝体 / 霞鹜文楷 / 思源宋体中选；正文用默认黑体还是霞鹜文楷？如果还需要卡片封面，必须再问一次“卡片封面字体”，同样从黑体 / 汇文明朝体 / 霞鹜文楷 / 思源宋体中选。

### Step 3: 读规范
1. **必读** `brand-dna.md` — 确认品牌底层规范
2. **必读** `references/style-library/styles-index.md` — 确认风格库
3. 根据用户选择读取对应风格文件，例如 `references/style-library/styles/warm-editorial.md`
4. 根据类型选读场景文件：
   - 教程型/介绍型/科普型 → `references/scene-tutorial.md`
   - 活动页/分享会/Landing → `references/scene-landing.md`
   - App型/功能型（看板/书架/Canvas） → `references/scene-app.md`
   - **图文卡片/小红书图文/文章转卡片** → `references/scene-cards.md`
   - **公众号排版/做分发** → `references/scene-wechat.md`

### Step 4: 拷模板
从 `assets/` 选择对应模板作为起点：
- 教程型 → `assets/template-tutorial.html`
- 活动页/Landing → `assets/template-landing.html`
- App型/功能型 → `assets/template-app.html`
- **图文卡片** → `assets/template-cards.html`

**从模板开始改，不从零写。**

### Step 5: 选布局组合
从 `references/layouts.md` 中选取 3~5 种布局模式，为每个 section 分配不同布局。

**每个 section 布局必须不同。**

（图文卡片模式：先确定封面型、信息型、图文型或混合组卡，再参考 `scene-cards.md` 中的推荐排版手法，为每页选择不同手法。）

### Step 6: 选组件填充
从 `references/components.md` 中选取组件填入各 section。

**硬规则：禁止使用任何HTML默认样式。** 所有引用块、列表、表格、卡片必须从 components.md 里选用对应组件的代码。不允许用默认 `<blockquote>`、默认 `border-left` 引用、无样式 `<ul>/<ol>`、默认 `<table>`。如果在 components.md 里找不到合适的，自己设计一个符合 brand-dna 规范的，但绝不能用浏览器默认样式。

### Step 7: 自检
对照 `references/checklist.md` 逐条检查：
- **P0 必须全过** — 任何一条不过就要改
- P1 应过 — 尽量满足
- P2 加分 — 锦上添花

（图文卡片模式：额外对照 `scene-cards.md` 底部的 Checklist。）

### Step 8: 交付
输出最终 HTML 文件，确保可直接在浏览器打开。

## 场景类型速查

| 类型 | 场景文件 | 模板 |
|------|----------|------|
| 教程型/介绍型/科普型 | `references/scene-tutorial.md` | `assets/template-tutorial.html` |
| 活动页/分享会/Landing | `references/scene-landing.md` | `assets/template-landing.html` |
| App型/功能型 | `references/scene-app.md` | `assets/template-app.html` |
| 图文卡片/小红书图文 | `references/scene-cards.md` | `assets/template-cards.html` |
| 公众号排版 | `references/scene-wechat.md` | `assets/template-wechat.html` |

## 关键原则
- **从模板开始改，不从零写** — 模板已内置品牌变量和基础结构
- **先给用户选择菜单** — 先展示风格、交付类型、排版方向，再动手
- **主动引导用户** — 用户没选清楚时先收敛方向，不用完整页面试错
- **风格库可扩展** — 新风格、新案例、新描述统一放入 `references/style-library/`
- **默认纸张编辑风** — 使用亚麻米白纸张背景、轻微颗粒、黑色排版、黄色局部高亮和少量编辑红批注，视觉效果主要靠排版、字号、字重和留白
- **中文字体必须分别选择** — 展示 HTML 标题和卡片封面标题是两个不同选择，不能只问一次；选项固定为黑体 / 汇文明朝体 / 霞鹜文楷 / 思源宋体；正文通过 `--font-body` 在默认黑体和霞鹜文楷之间选择
- **中文字体搭配限制** — 黑体必须搭配汇文明朝体；霞鹜文楷和汇文明朝体在同一封面/首屏里只能二选一，不能都作为主要标题字体
- **全局英文字体规则** — 英文大标题默认用 Arial Narrow / Helvetica Neue / Aptos Display；低反差衬线只用 Source Serif 4 / Libre Baskerville；禁止 Didot、Bodoni、Cormorant、高反差 Fraunces 和夸张 italic；手写/批注用 Caveat，代码/终端/API Key/命令用 Fira Code
- **红色批注必须有语义** — 红圈只能圈具体词、短语、数字、按钮或核心句，不能悬空圈空白；没有明确对象时改用短下划线、小箭头或直接删除
- **封面页禁止装饰编号** — 封面页/首屏只保留必要小标签文本，禁止装饰性数字、水印数字和重复编号图形；不要在封面卡片或首屏右上角放淡色编号当装饰
- **卡片必须整体化** — 图文卡片使用整体式信息卡，不堆多层小框；主卡片圆角约 22px，图片/顶部视觉区约 20px，小标签约 14px；边框用低对比 1px 细线，阴影很弱或不用；层级靠留白、分区、细分隔线和局部批注建立
- **禁止大面积彩色结构** — 不使用粗黄色外框、整屏编辑红背景、大面积黄色卡片底；黄色和编辑红只能做局部强调
- **每个 section 布局必须不同** — 避免单调重复，从 layouts.md 选不同模式
- **做完必须跑 checklist** — P0 全过才能交付

## 禁忌
严格遵守 `brand-dna.md` 的禁忌清单，不在此重复。核心底线：截图发 Twitter 不会被说"又是AI做的"。
