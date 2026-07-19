# Style Library — 风格库

这个目录用来存放后续新增的设计风格、设计事例和风格描述。

它不替代现有文件：

- `references/layouts.md` 负责布局结构。
- `references/components.md` 负责可复用组件。
- `references/scene-*.md` 负责不同交付场景。
- `references/style-library/` 负责「这个页面应该长成什么气质」。

## 使用顺序

1. 先看 `styles-index.md`，给用户展示可选设计风格。
2. 用户选定风格后，读取对应 `styles/*.md`。
3. 如果用户给了参考图或案例，登记到 `examples/`。
4. 再回到场景文件、布局文件和组件文件执行。

## 目录结构

```text
style-library/
├── README.md
├── styles-index.md          # 风格总表，给 AI 和用户先看
├── style-template.md        # 新增风格时复制这个模板
├── example-template.md      # 新增设计案例时复制这个模板
├── styles/                  # 单个设计风格说明
│   └── warm-editorial.md
└── examples/                # 你后续放的设计案例说明
    └── README.md
```

## 添加新风格

复制 `style-template.md` 到 `styles/你的风格名.md`，然后补充：

- 风格名称
- 适用场景
- 视觉关键词
- 排版特点
- 可用布局
- 可用组件
- 禁忌
- 参考案例

添加后，在 `styles-index.md` 里登记一行。
