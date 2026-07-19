# Component: Timeline

- **用途**：呈现一组按时间排序的事件。
- **结构**：`axis`、重复 `time`、`event`、可选 `status/evidence`。
- **状态**：past、current、future；交互式版本可展开详情。
- **内容规则**：明确时间粒度和排序；事件标题使用动作或结果。
- **无障碍**：DOM 顺序与时间顺序一致；当前项有文字说明。
- **Brand 适配**：Warm 像档案年表；AI Lab 像运行记录；Minimal Poster 适合少量大事件。
- **避免**：用 Timeline 表示无时间关系步骤、交错布局导致阅读顺序混乱。
