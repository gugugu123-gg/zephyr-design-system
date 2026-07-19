# Component: Prompt Block

- **用途**：展示可复用 Prompt、变量、上下文与预期输出。
- **结构**：`purpose`、`prompt-body`、可选 `variables`、`input-example`、`output-contract`、copy action。
- **状态**：default、editing、copied、invalid。
- **内容规则**：变量使用一致占位符；明确哪些内容由用户替换；Prompt 与示例输出分开。
- **无障碍**：保持可复制文本、键盘可操作 copy、长内容可换行或滚动。
- **Brand 适配**：Warm 使用批注解释变量；AI Lab 使用字段与 schema；Minimal Poster 只摘取核心句，完整 Prompt 放后续页。
- **避免**：把 Prompt 当装饰代码、缺少输入上下文、复制后包含隐藏字符。
