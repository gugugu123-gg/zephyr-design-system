# Component: Terminal Window

- **用途**：展示命令、日志、运行状态和可复现结果。
- **结构**：`title/path`、可选窗口控制、`command`、`output`、`status`、copy action。
- **状态**：idle、running、success、warning、error。
- **内容规则**：命令与输出视觉区分；保留关键上下文，长日志折叠或截断并说明。
- **无障碍**：代码可选择和复制；状态带文本，不只用颜色；动画光标可关闭。
- **Brand 适配**：Warm 像编辑过的代码纸；AI Lab 像真实控制台；Minimal Poster 只用于一条关键命令或结果。
- **避免**：假的窗口按钮、整页等宽体、无法复制的截图代码。
