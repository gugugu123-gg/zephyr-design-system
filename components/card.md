# Component: Card

- **用途**：承载一个完整对象、案例、功能或摘要。
- **结构**：可选 `media`；必需 `title` 与 `body`；可选 `metadata`、`status`、`actions`。
- **状态**：default、hover、focus-within、selected、disabled、loading、empty。
- **内容规则**：整张卡只表达一个对象；动作不超过两个；不要在 Card 内再堆同层级 Card。
- **无障碍**：可点击卡片需要明确交互元素和键盘焦点，不能只监听容器点击。
- **Brand 适配**：Warm 使用纸面与细分隔；AI Lab 使用结构线和状态；Minimal Poster 使用硬边、低圆角和强比例。
- **避免**：所有 section 都用卡片、重阴影、固定高度截断关键内容。
