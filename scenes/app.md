# Scene: App

## Goal

支持用户高频完成任务、监控状态、比较信息并恢复错误。

## Required Input

核心任务、角色权限、数据对象、状态、常用动作、异常与空状态。

## Information Structure

1. **Global Navigation**：范围、身份、主要模块。
2. **Context Header**：当前对象、状态、主要动作。
3. **Primary Workspace**：完成核心任务的主区域。
4. **Supporting Panel**：筛选、详情、历史或上下文。
5. **System Feedback**：加载、成功、警告、错误、空状态。

## Recommendations

- Layout：`dashboard`、`two-column`、`grid`。
- Component：`card`、`badge`、`timeline`、`workflow-node`、`terminal-window`、`annotation`。

## Constraints

- 视觉层级服从任务频率，不按“好看”平均分配空间。
- 所有可操作元素有 hover、focus、disabled、loading 和 error 状态。
- 高密度界面使用稳定尺寸和对齐，动态内容不能造成布局跳动。
- 移动端重排主要任务，不能简单缩小桌面后台。

## Common Errors

- 把 App 做成营销 Landing Page。
- 所有信息都放进同权重卡片。
- 用颜色作为唯一状态信号。
- 只有理想数据，没有空、错、加载和权限状态。

## Delivery Check

用户能快速找到主要任务、理解当前状态、执行动作并从错误恢复。
