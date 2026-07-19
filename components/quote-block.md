# Component: Quote Block

- **用途**：呈现有来源的引用或作者明确标记的核心观点。
- **结构**：`quote`、`source/author`、可选 `context` 与 `link`。
- **状态**：静态；交互仅用于查看来源或复制。
- **内容规则**：外部引用必须署名；自有观点不能伪装成名人引用。
- **无障碍**：使用语义化 `blockquote` 与 `cite`，但必须提供完整自定义样式。
- **Brand 适配**：Warm 强调编辑排版；AI Lab 适合研究结论；Minimal Poster 可让引用成为唯一主视觉。
- **避免**：默认 `border-left` 引用样式、巨大装饰引号压住正文、无来源数据。
