# Design Contract

生成前使用以下字段固定任务边界：

```yaml
brand: <brand-id>
scene: <scene-id>
audience:
  primary: <audience-id>
  secondary: <optional-audience-id>
delivery: <responsive-html|static-cards|presentation|other>
goal: <one measurable sentence>
primary_action: <optional>
content_constraints:
  - <required content, claims, order>
asset_constraints:
  - <provided or required assets>
technical_constraints:
  - <framework, size, browser, export>
accessibility: WCAG-AA
```

## Resolution Notes

在契约下附 3-8 行即可：

- Scene 提供哪些 section。
- Audience 如何改变密度、术语和证据。
- Brand 如何渲染视觉。
- 选择哪些 Layout 和 Component。
- 有哪些用户约束覆盖默认规则。

契约是实现依据，不是长篇提案。用户已给出的信息不得重复询问。
