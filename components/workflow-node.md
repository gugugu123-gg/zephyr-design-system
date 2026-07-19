# Component: Workflow Node

- **用途**：表示流程中的输入、处理、决策、工具或输出。
- **结构**：`type`、`label`、可选 `input-port`、`output-port`、`status`、`metadata`。
- **状态**：idle、queued、running、success、warning、error、disabled。
- **内容规则**：节点类型可识别；连接有方向；决策分支带条件；错误显示原因或恢复入口。
- **无障碍**：提供流程的线性文本等价物；节点可聚焦，状态不只靠颜色。
- **Brand 适配**：Warm 可弱化为步骤卡和手绘连接；AI Lab 使用精确端口与状态；Minimal Poster 只保留 3-5 个关键节点。
- **避免**：装饰性连接线、无限画布没有导航、缩放后文字不可读。
