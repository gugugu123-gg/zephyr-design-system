# Brand DNA Index

Brand DNA 只定义视觉身份，不定义内容顺序。选择 Brand 后读取对应文件。

| ID | 名称 | 适用场景 | 核心气质 | 文件 |
|---|---|---|---|---|
| `warm-editorial` | Warm Editorial | 观点、成长、知识分享、长文 | 温暖、克制、有人味 | `brands/warm-editorial.md` |
| `ai-laboratory` | AI Laboratory | AI 工具、Agent、教程、工作流 | 精密、清晰、实验性 | `brands/ai-laboratory.md` |
| `minimal-poster` | Minimal Poster | 社交卡片、观点海报、发布封面 | 直接、强对比、传播性 | `brands/minimal-poster.md` |

## 选择规则

- 用户指定品牌或参考图时，优先服从用户。
- 用户未指定时，展示名称、适用场景和气质，等待选择。
- 用户明确授权 AI 决定时，根据内容语义选择，并在生成前声明选择。
- Brand 的推荐布局和组件是软建议；Scene 决定信息结构。

## 扩展

新增 Brand 时复制 `brands/_schema.md`，使用小写 kebab-case 文件名，并登记到本索引。
