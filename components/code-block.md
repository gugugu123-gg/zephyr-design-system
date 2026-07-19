# Component: Code Block

- **用途**：展示可阅读、可复制、可运行或可对照的代码。
- **结构**：`language/file`、`code`、可选 `line-highlight`、`annotation`、copy action。
- **状态**：default、copied、wrapped、expanded、error-example。
- **内容规则**：标明语言和必要版本；省略代码需用明确注释；高亮只指向讲解行。
- **无障碍**：语法颜色对比达标；支持键盘复制；窄屏允许横向滚动或受控换行。
- **Brand 适配**：Warm 使用轻纸面和编辑注释；AI Lab 使用准确语法与执行上下文；Minimal Poster 只展示最关键片段。
- **避免**：用图片代替代码、行号被复制进代码、只靠颜色解释 diff。
