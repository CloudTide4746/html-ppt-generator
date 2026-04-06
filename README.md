# HTML PPT Generator

<p align="center">
  <img src="https://img.shields.io/badge/reveal.js-5.0-brightgreen?style=for-the-badge" alt="reveal.js">
  <img src="https://img.shields.io/badge/Tailwind%20CSS-3.x-38b2ac?style=for-the-badge" alt="Tailwind CSS">
  <img src="https://img.shields.io/badge/License-MIT-blue?style=for-the-badge" alt="License">
</p>

---

<p align="center">
  🎨 将纯文本内容转换为精美的交互式 HTML 演示文稿
</p>

<p align="center">
  基于 <strong>reveal.js</strong> + <strong>Tailwind CSS</strong> + <strong>Font Awesome</strong>
</p>

---

## 📖 简介

HTML PPT Generator 是一个 Claude Code 技能，可将纯文本内容快速转换为专业的、交互式的 HTML 演示文稿。无需安装任何软件，直接在浏览器中打开即可使用。

适用于创建技术分享、教学演示、会议演讲、产品介绍等多种场景。

---

## ✨ 功能特性

| 特性 | 说明 |
|------|------|
| 🎯 **Reveal.js 驱动** | 全功能演示框架，支持幻灯片过渡、键盘导航、进度指示 |
| 🎨 **Tailwind CSS 样式** | 实用优先的样式设计，代码简洁、风格统一 |
| ⚡ **交互式组件** | 多种交互元素，让演示更生动 |
| 📱 **响应式设计** | 自适应桌面、平板、手机等不同设备 |
| 🌈 **渐变背景** | 多种配色主题自由切换 |
| 🔣 **丰富图标** | Font Awesome 图标库支持 |

---

## 🚀 快速开始

### 输入示例

向 Claude 提供你的内容，例如：

```
请帮我创建一个关于"Git 入门教程"的演示文稿，内容包括：
1. Git 简介
2. 基本命令（init, add, commit, push）
3. 分支管理
4. 常见问题
```

### Claude 会自动

```
1. 🔍 深入分析内容结构和逻辑
2. 📐 规划每个幻灯片的布局和样式
3. 💻 生成完整的 HTML 代码
4. ✅ 审核并优化视觉效果
5. 🔄 迭代直到达到高质量标准
```

### 输出结果

生成包含以下功能的 HTML 文件：

- 全屏演示模式
- 键盘/鼠标导航
- 进度条显示
- 所有交互组件正常工作

---

## 🎯 交互组件详解

### 1. 点击展开卡片 `📋`

点击卡片标题展开更多详情，适合展示补充信息。

```
点击前：图标 + 标题
点击后：展开显示详细描述
```

> 💡 **使用场景**：功能介绍、详细说明、附加资源

---

### 2. 标签页导航 `📑`

在多个内容面板之间切换，同一区域展示不同内容。

```
┌─────────┬─────────┬─────────┐
│  标签1  │  标签2  │  标签3  │
├─────────┼─────────┼─────────┤
│         │         │         │
│  内容1  │  内容2  │  内容3  │
│         │         │         │
└─────────┴─────────┴─────────┘
```

> 💡 **使用场景**：对比分析、分类展示、步骤说明

---

### 3. 交互式流程图 `🔄`

可点击的步骤流程图，展示线性流程或步骤序列。

```
[步骤1] ──▶ [步骤2] ──▶ [步骤3] ──▶ [步骤4]
```

> 💡 **使用场景**：流程说明、算法演示、操作步骤

---

### 4. 可展开列表 `📚`

手风琴式列表，适合 FAQ 或多层级内容。

```
▼ 问题1
   答案内容...

▼ 问题2
   答案内容...
```

> 💡 **使用场景**：问答环节、详细解释、列表展示

---

### 5. 交互式测验 `❓`

多选题，点击后立即显示对错反馈。

```
❓ 问题：Git 的基本工作区域包括？

   ○ Working Directory
   ○ Staging Area
   ○ Remote Repository
   ○ Local Database

   ✓ 正确！已选择所有正确答案
```

> 💡 **使用场景**：知识巩固、互动问答、学习测验

---

### 6. 可拖拽元素 `🖱️`

支持拖拽排序的交互元素。

> 💡 **使用场景**：排序练习、分类任务、组合游戏

---

## 🎨 配色主题

每个幻灯片支持独立的渐变背景主题：

| 主题 | 渐变效果 | 适用场景 |
|------|----------|----------|
| 🟣 **紫色 (Purple)** | 靛蓝 → 紫色 → 石板灰 | 技术分享、创意展示 |
| 🔵 **青色 (Cyan)** | 青色 → 蓝色 → 靛蓝 | 数据分析、流程说明 |
| 🟢 **翡翠 (Emerald)** | 翡翠绿 → 青色 → 蓝绿 | 环保主题、成功案例 |
| 🟠 **橙色 (Orange)** | 橙色 → 红色 → 玫瑰红 | 促销活动、活力展示 |
| ⬛ **石板灰 (Slate)** | 石板灰 → 靛蓝 → 紫色 | 商务演示、专业汇报 |

---

## 📂 项目结构

```
html-ppt-generator/
├── SKILL.md       # 🔧 完整技能文档（面向开发者）
└── README.md      # 📄 项目说明文档（面向用户）
```

---

## 🛠️ 技术栈

### CDN 依赖

| 库 | 版本 | 用途 |
|----|------|------|
| [Tailwind CSS](https://tailwindcss.com/) | v3.x | 样式框架 |
| [Reveal.js](https://revealjs.com/) | v5.0 | 演示框架 |
| [Font Awesome](https://fontawesome.com/) | v6 | 图标库 |
| [Google Fonts](https://fonts.google.com/) | - | 字体（Inter + Noto Sans SC） |

---

## 📐 设计原则

### ✅ 应该这样做

```
1. Tailwind 优先 - 使用工具类替代自定义 CSS
2. 内容居中 - 使用 max-width + auto margin 居中
3. 全屏展示 - 幻灯片填满整个视口
4. 适度交互 - 交互组件服务内容，而非喧宾夺主
```

### ❌ 避免这样做

```
1. 避免过度使用 padding - 会破坏居中效果
2. 避免固定高度 - 使用相对尺寸
3. 避免冲突 CSS - reveal.js 管理的属性不要覆盖
4. 避免 rush 输出 - 按规定流程执行每个阶段
```

---

## 📝 使用示例

### 示例 1：技术分享

```
输入：关于 React Hooks 的技术分享
输出：20+ 页交互式幻灯片，包含代码演示、原理动画
```

### 示例 2：产品介绍

```
输入：新产品发布会演示
输出：包含特性卡片、对比表格、CTA 按钮的演示文稿
```

### 示例 3：教学课件

```
输入：Python 入门教程
输出：含代码示例、交互测验、流程图的完整课件
```

---

## 🔧 本地使用

1. 克隆仓库
   ```bash
   git clone https://github.com/CloudTide4746/html-ppt-generator.git
   ```

2. 在 Claude Code 中使用此技能
   ```bash
   /skill html-ppt-generator
   ```

3. 提供你的内容，等待生成完成

---

## 📄 License

MIT License - 欢迎使用、修改和分享！

---

<p align="center">
  Made with ❤️ by CloudTide4746
</p>
