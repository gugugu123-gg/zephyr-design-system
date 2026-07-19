# Zephyr Design System

一个面向 AI Agent 的可扩展 Design Operating System。它不再把审美压缩成单一 `brand-dna.md`，而是用五个独立维度组合设计：

```text
Brand DNA（视觉身份）
        ×
Scene（内容结构）
        ×
Audience（理解与决策方式）
        ↓
Layouts（信息组织）+ Components（语义零件）
        ↓
可验证的设计输出
```

核心目标：不限制有理由的创造，但限制无依据的随机发挥。

## Architecture

```text
zephyr-design-system/
├── SKILL.md                       AI 执行流程、选择门槛、冲突优先级
├── agents/
│   └── openai.yaml               Skill 的 UI 元数据
├── brands/
│   ├── _index.md                 Brand 选择索引
│   ├── _schema.md                新 Brand 的必填契约
│   ├── warm-editorial.md          温暖编辑主题
│   ├── ai-laboratory.md           AI 工具与技术主题
│   └── minimal-poster.md          极简传播海报主题
├── scenes/
│   ├── _index.md                 Scene 与模板映射
│   ├── _schema.md                新 Scene 契约
│   ├── tutorial.md               教程与概念解释
│   ├── landing.md                产品、活动与项目介绍
│   ├── app.md                    工具、后台与工作台
│   ├── social-card.md            社交卡片与组图
│   ├── article.md                长文与公众号
│   └── presentation.md           演示、分享与提案
├── audiences/
│   ├── _index.md                 Audience 选择索引
│   ├── _schema.md                新 Audience 契约
│   ├── general-readers.md         大众读者
│   ├── creators.md               内容创作者
│   ├── technical-practitioners.md 技术实践者
│   └── decision-makers.md         决策者
├── layouts/
│   ├── _index.md                 Layout 索引
│   ├── _schema.md                新 Layout 契约
│   └── *.md                      7 个无品牌布局骨架
├── components/
│   ├── _index.md                 Component 索引
│   ├── _schema.md                新 Component 契约
│   └── *.md                      9 个独立语义组件
├── assets/
│   ├── template-tutorial.html     教程起始模板
│   ├── template-landing.html      Landing 起始模板
│   ├── template-app.html          App 起始模板
│   ├── template-cards.html        社交卡片起始模板
│   └── template-wechat.html       长文起始模板
└── references/
    ├── design-contract.md         生成前的任务契约
    ├── checklist.md               P0/P1/P2 质量门槛
    ├── legacy-map.md              旧文件到新架构的迁移关系
    ├── components.md              旧版 HTML/CSS 实现配方
    ├── layouts.md                 旧版布局实现配方
    └── style-library/             旧风格记录与案例
```

`brand-dna.md` 仅作为旧链接的兼容入口。Warm Editorial 的规则已迁移到 `brands/warm-editorial.md`，不再是全局默认。

## Responsibility Model

| Layer | 回答的问题 | 不负责 |
|---|---|---|
| Brand DNA | 看起来和感觉像谁？ | section 顺序 |
| Scene | 为了完成什么内容目标？ | 品牌色和字体 |
| Audience | 给谁看、需要多深？ | 固定视觉主题 |
| Layout | 信息如何排列和响应？ | 内容真实性 |
| Component | 局部结构和状态是什么？ | 整页叙事 |

冲突时依次服从：用户硬约束 → 正确性与可访问性 → Scene → Audience → Brand → Layout/Component 默认值 → 模板。

## AI Workflow

1. 选择 Brand DNA。
2. 确认主 Scene。
3. 确认 Primary Audience。
4. 建立 Design Contract。
5. 根据 Scene 组合 Layout。
6. 选择必要 Component，并应用 Brand 适配。
7. 从模板或语义骨架生成设计。
8. 按 Checklist 和各层验收规则检查。
9. 交付文件与验证结果。

如果用户只说“想换一个风格”，AI 必须停在 Brand 选择阶段，不得自行新增主题或修改文件。

## Built-in Brands

### Warm Editorial

适合个人观点、成长文章和知识分享。纸面、中性色、克制批注与编辑排版构成辨识度。

### AI Laboratory

适合 AI 工具、Agent、教程和工作流。技术感来自真实状态、数据、节点和精确结构，不使用蓝紫霓虹或通用机器人图。

### Minimal Poster

适合社交媒体卡片、观点海报和演示章节页。使用严格网格、巨大文字、强裁切和单一传播焦点。

## Extension

- 新视觉身份：复制 `brands/_schema.md`。
- 新内容类型：复制 `scenes/_schema.md`。
- 新受众模型：复制 `audiences/_schema.md`。
- 新信息骨架：复制 `layouts/_schema.md`。
- 新语义零件：复制 `components/_schema.md`。

新增文件使用小写 kebab-case ID，并登记到对应 `_index.md`。不要通过复制整套 HTML 模板来创建 Brand。

## Existing Demos

- `demo-readme-tutorial.html`：教程页面
- `demo-landing.html`：Landing
- `demo-app.html`：App
- `demo-cards.html`：社交卡片
- `assets/demo-wechat.html`：公众号排版
- `demo-layouts.html`：旧布局 Playground
- `components-preview.html`：旧组件预览

这些 Demo 是历史实现样本，不代表所有 Brand 的默认视觉。

## License

本仓库采用 [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)：

- 可使用、修改和分享。
- 必须署名 ESTHER不二（esthersjw）。
- 禁止商用。
- 修改后需以相同协议分享。
