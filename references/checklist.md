# Quality Checklist

## P0: 必须通过

### Contract

- [ ] Brand、Scene、Primary Audience 已明确并与 Design Contract 一致。
- [ ] 用户硬约束、真实素材和交付格式已落实。
- [ ] 没有在用户只表达换风格意向时擅自新增或修改 Brand。

### Content

- [ ] Scene 的目标和必需信息结构完整。
- [ ] 标题、数据、引用、评价和来源真实且可核查。
- [ ] Audience 能理解术语、行动、状态和证据。
- [ ] 没有用占位文案冒充成品内容。

### Visual Identity

- [ ] 颜色、字体、图形、图片、动效符合所选 Brand。
- [ ] 状态色和强调色语义一致。
- [ ] 不存在 Brand 明确禁止的元素。
- [ ] 风格来自系统规则，不是随机装饰叠加。

### Layout and Components

- [ ] 每个 Layout 与信息关系匹配，阅读顺序明确。
- [ ] Component 结构和状态完整，没有同层级 Card 嵌套。
- [ ] 页面无文本溢出、遮挡、错位和无意布局跳动。
- [ ] 引用、列表、表格、代码和控件不是浏览器默认样式。

### Responsive and Accessibility

- [ ] 桌面与移动端均检查；移动端是重排，不是机械缩小。
- [ ] 键盘可达、焦点可见、语义结构正确。
- [ ] 颜色不是唯一信息载体，正文与控件对比度合格。
- [ ] 图片有替代文本；交互控件有可理解名称。
- [ ] 支持 `prefers-reduced-motion`，关键内容不依赖动画或 hover。

### Technical

- [ ] 控制台无阻断错误，关键资源加载成功。
- [ ] 真实交互可用，loading、empty、error 等必要状态存在。
- [ ] 外部素材许可明确，不提交来源不明的字体或图片。

## P1: 应当通过

- [ ] 第一视口能识别对象、价值或主要任务。
- [ ] 连续 section 有节奏变化，但整体网格和视觉语言一致。
- [ ] 组件数量克制，每个组件都有内容或操作理由。
- [ ] 关键主张紧邻证据，CTA 层级明确。
- [ ] 目标导出尺寸下检查了缩略图、投影或长文阅读效果。

## P2: 加分项

- [ ] 有真实且相关的主视觉、截图、数据或案例。
- [ ] 微交互帮助理解状态或因果，而非纯装饰。
- [ ] 系列产物有稳定母版与可控变化。
- [ ] 设计决策能追溯到 Brand、Scene 或 Audience 规则。

## Required Final Checks

再执行所选 Brand 的 `Acceptance`、Scene 的 `Delivery Check`、Audience 的成功标准，以及所有选中 Component 的状态和无障碍要求。
