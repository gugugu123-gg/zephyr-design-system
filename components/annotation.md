# Component: Annotation

- **用途**：解释、纠错、指向界面位置或强调具体内容。
- **结构**：`anchor`、`connector`、`label`，可选 `index`。
- **状态**：default、active、resolved；交互式注释需支持显示/隐藏。
- **内容规则**：每条 Annotation 必须有真实锚点；文字短、动作明确。
- **无障碍**：阅读顺序中注释紧跟锚点；不能只靠空间位置或颜色建立关联。
- **Brand 适配**：Warm 使用手写线与编辑红；AI Lab 使用编号和精确引线；Minimal Poster 使用短线、坐标或色块。
- **避免**：悬空红圈、交叉引线、在移动端指向错误位置。
