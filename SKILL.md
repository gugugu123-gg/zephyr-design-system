---
name: zephyr-design-system
description: 可扩展的个人 AI Design Operating System。用于设计或重构网页、Landing Page、App、教程、文章、社交媒体卡片、演示文稿及其他视觉界面；通过 Brand DNA、Scene、Audience、Layout、Component 五层规范生成可执行设计，并按质量清单验证。用户提出做页面、做图文、设计界面、选择视觉风格、扩展品牌主题或维护本设计系统时使用。
---

# Zephyr Design System

把每个设计任务解析为：

`Brand DNA × Scene × Audience → Layouts + Components → Output`

- **Brand DNA**：视觉身份。控制颜色、字体、图形、图片、动效和禁忌。
- **Scene**：内容类型。控制目标、信息结构和叙事顺序。
- **Audience**：目标受众。控制语言、密度、证据和可访问性。
- **Layout**：信息组织方式。控制槽位、顺序和响应式关系。
- **Component**：语义零件。控制局部结构、状态和交互。

不要让 Brand 决定内容结构，不要让 Scene 写死视觉风格。

## Operating Rules

1. 未确认 Brand、Scene、Audience 前，不生成完整设计或修改实现文件。
2. 用户已明确某个维度时直接采用，不重复询问。
3. 用户提供参考图或现有设计时，先提取可观察规则，再确认映射到现有 Brand 还是新增 Brand。
4. 用户只说“想换风格”时，仅展示 Brand 选项并询问方向，不自行创建风格。
5. 用户授权“你来决定”时可以推断，但在实现前必须声明 Design Contract。
6. 推荐关系是软约束；用户硬约束、内容正确性和可访问性是硬约束。
7. 只读取当前任务需要的文件，避免把所有规范一次装入上下文。

## Workflow

### Step 1: Resolve Brand DNA

读取 `brands/_index.md`。

- 展示可选 Brand 的名称、适用场景和核心气质。
- 用户选择后读取对应 `brands/<id>.md`。
- 用户要新增风格时，先询问定位、关键词、参考、适用与不适用场景；确认后再按 `brands/_schema.md` 创建。

### Step 2: Resolve Scene

读取 `scenes/_index.md`。

- 根据用户明确的交付物映射 Scene；不明确时询问。
- 读取对应 `scenes/<id>.md`，提取目标、必需输入和默认信息结构。
- 一个主交付物只设一个 Primary Scene；可以声明 Secondary Scene 处理混合需求。

### Step 3: Resolve Audience

读取 `audiences/_index.md`。

- 确认主受众；必要时设置一个次受众。
- 读取对应 `audiences/<id>.md`。
- 用 Audience 调整术语、密度、证据、字号和交互复杂度，不覆盖 Brand 身份。

### Step 4: Create Design Contract

实现前输出并确认一份简短契约：

```yaml
brand: warm-editorial
scene: tutorial
audience:
  primary: creators
  secondary: general-readers
delivery: responsive-html
goal: 让创作者理解并复用一个 AI 工作流
content_constraints: []
asset_constraints: []
accessibility: WCAG-AA
```

缺少会改变方向的素材或约束时先询问。不要用完整页面作为风格试错。

### Step 5: Compose Layouts

读取 `layouts/_index.md`，再读取候选 Layout 文件。

1. 按 Scene 的信息结构为每个 section 分配 Layout。
2. 连续 section 避免相同构图，除非重复本身有比较或系列语义。
3. 用 Audience 调整列数、密度、阅读顺序和披露深度。
4. 记录 section map：

```text
Hero -> hero
Concept -> two-column
Process -> step-flow
Example -> comparison
Summary -> hero
```

### Step 6: Select Components

读取 `components/_index.md`，只读取被选中的组件文件。

- 每个组件必须服务于信息或操作，不为填空而添加。
- 使用组件定义的结构、状态与无障碍要求。
- 再应用当前 Brand 的视觉适配。
- 需要旧版 HTML/CSS 实现片段时，可选读 `references/components.md`，但必须按当前 Brand 重绘。

### Step 7: Read Assets and Generate

根据 Scene 从 `scenes/_index.md` 选择起始模板。模板不匹配时可以新建实现，但保留 Design Contract。

生成顺序：

1. 内容骨架
2. 语义 HTML 与交互状态
3. Layout 响应式结构
4. Brand tokens 与组件适配
5. 图片、图标和真实数据
6. 动效与减弱动效

不得使用浏览器默认样式交付引用、列表、表格、代码或交互控件。不得伪造评价、数据、产品状态或素材来源。

### Step 8: Validate

读取 `references/checklist.md`。

- P0 全部通过后才能交付。
- 再执行所选 Brand、Scene、Audience 和 Component 文件中的 Acceptance/Delivery 要求。
- 对 HTML 至少检查桌面和移动端截图、溢出、重叠、键盘焦点、控制台错误和关键资源加载。
- 发现问题后修复并重新检查，不只报告问题。

### Step 9: Deliver

交付最终文件，并简要说明：

- Design Contract
- 使用的 Layout 与 Component
- 验证结果
- 仍存在的真实限制

除非用户明确要求，不自动提交或推送 Git。

## Conflict Priority

发生冲突时按以下优先级处理：

1. 用户明确的内容、媒介和业务约束
2. 正确性、安全性、可访问性
3. Scene 的内容目标和结构
4. Audience 的理解与决策需求
5. Brand 的视觉身份
6. Layout 与 Component 默认建议
7. 模板和旧示例

如果高优先级规则迫使设计偏离 Brand，说明偏离点，不静默破坏内容。

## Extension Protocol

- 新 Brand：复制 `brands/_schema.md`，登记 `brands/_index.md`。
- 新 Scene：复制 `scenes/_schema.md`，登记 `scenes/_index.md`。
- 新 Audience：复制 `audiences/_schema.md`，登记 `audiences/_index.md`。
- 新 Layout：复制 `layouts/_schema.md`，登记 `layouts/_index.md`。
- 新 Component：复制 `components/_schema.md`，登记 `components/_index.md`。

新增项使用小写 kebab-case ID。不得通过复制整套模板来新增风格；视觉差异应优先进入 Brand，内容差异进入 Scene。

## Core Quality Principle

限制低质量随机发挥，不限制有理由的创造：

- 锁定语义 token、排版角色、状态含义和禁忌。
- 允许在网格比例、构图、图像裁切和 section 节奏上变化。
- 每个设计决定都应能追溯到内容目标、受众需求或 Brand 规则。
