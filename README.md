# HTML PPT Generator

将纯文本内容转换为精美的、交互式的 HTML 演示文稿，基于 reveal.js 和 Tailwind CSS。

## 简介

本技能可将纯文本内容转换为专业的交互式 HTML 演示文稿。使用 [reveal.js](https://revealjs.com/) 作为演示框架，[Tailwind CSS](https://tailwindcss.com/) 进行样式美化。

## 功能特性

- **Reveal.js 驱动** - 全功能演示框架，支持幻灯片过渡、导航控制和进度指示
- **Tailwind CSS 样式** - 实用优先的样式设计，代码简洁易维护
- **交互式组件** - 点击展开卡片、标签页导航、可展开列表、交互式流程图、拖拽元素和问答测验
- **响应式设计** - 演示文稿自适应不同屏幕尺寸
- **渐变背景** - 多种配色主题（紫色、青色、翡翠、橙色、石板灰）
- **图标支持** - 全程使用 Font Awesome 图标

## 交互组件

| 组件 | 说明 |
|------|------|
| 点击展开卡片 | 点击展开显示更多详情 |
| 标签页导航 | 在内容面板之间切换 |
| 交互式流程图 | 可点击的步骤流程 |
| 可展开列表 | 手风琴式问答 |
| 交互式测验 | 带反馈的多选题 |
| 可拖拽元素 | 拖拽排序 |

## 使用方式

本技能适用于 Claude Code。当你提供演示内容时，技能会：

1. 深入分析内容
2. 规划幻灯片结构
3. 生成 HTML 和 Tailwind CSS 样式
4. 审核并优化输出
5. 迭代直到演示文稿达到质量标准

## 项目结构

```
html-ppt-generator/
├── SKILL.md    # 技能主文档
└── README.md   # 说明文件
```

## 技术细节

### 外部依赖（CDN）

- Tailwind CSS
- Reveal.js（CSS + JS）
- Font Awesome
- Google Fonts（Inter、Noto Sans SC）

## 设计原则

1. **Tailwind 优先** - 所有样式使用工具类，仅在动画关键帧定义时使用自定义 CSS
2. **Reveal.js 兼容** - 避免与 reveal.js 冲突的 CSS 属性
3. **内容居中** - 每个幻灯片使用适当的 max-width 约束居中内容
4. **全屏展示** - 演示文稿填满整个浏览器视口

## License

MIT
