# Layout: Step Flow

- **适合**：教程步骤、工作流、方法、审批或状态转换。
- **槽位**：`flow-title`、重复的 `step-index`、`step-action`、`step-detail`、`step-output`，可选连接关系。
- **信息顺序**：严格按依赖顺序；分支必须有条件标签，循环必须标出返回点。
- **视觉特点**：方向、当前状态和完成状态清晰；连接线不是装饰。
- **响应式**：桌面可横向或纵向，移动端默认纵向；连接关系不能在重排后丢失。
- **不适用**：没有先后关系的同类特征。
- **可用 Scene**：`tutorial`、`landing`、`app`、`social-card`、`presentation`。
