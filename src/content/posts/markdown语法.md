---
title: Markdown 书写指南/示例链接
published: 2026-05-18
description: Markdown 书写指南/示例链接
tags: [utility tools, markdown]
category: utility tools
slug: md
draft: false
---

# **Markdown 书写指南/示例链接**：

[flyfire博客文章示例](https://firefly.cuteleaf.cn/archive/?category=%E6%96%87%E7%AB%A0%E7%A4%BA%E4%BE%8B)

### 主流平台
- **GitHub (GFM - GitHub Flavored Markdown)**  
  官方基础语法指南：**[官方基础语法指南](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)**  
  完整 GFM 规范：**[完整 GFM 规范](https://github.github.com/gfm/)**

- **GitLab (GLFM)**  
  官方文档：**[官方文档](https://docs.gitlab.com/user/markdown/)**

- **Stack Overflow / Stack Exchange**  
  Markdown 编辑帮助：**[Markdown 编辑帮助](https://stackoverflow.com/editing-help)**  
  格式化帮助：**[格式化帮助](https://stackoverflow.com/help/formatting)**

- **Reddit**  
  官方格式化指南：**[官方格式化指南](https://support.reddithelp.com/hc/en-us/articles/360043033952-Formatting-Guide)**

### 本地/笔记类工具
- **Obsidian**  
  基础语法：**[https://obsidian.md/help/syntax](https://obsidian.md/help/syntax)**  
  Obsidian 扩展语法：**[https://obsidian.md/help/obsidian-flavored-markdown](https://obsidian.md/help/obsidian-flavored-markdown)**

- **Notion**  
  Markdown 快捷键与支持（帮助中心）：**[https://www.notion.com/help/writing-and-editing-basics](https://www.notion.com/help/writing-and-editing-basics)**（搜索 “Markdown” 部分）  
  开发者增强 Markdown 参考（API）：**[https://developers.notion.com/guides/data-apis/enhanced-markdown](https://developers.notion.com/guides/data-apis/enhanced-markdown)**

### 中文主流平台
- **语雀 (Yuque)**  
  语雀高度兼容 GFM，可直接参考 GitHub 语法，平台内编辑器也支持快捷输入

### 通用标准参考
- 原始 Markdown 语法（John Gruber）：http://daringfireball.net/projects/markdown/syntax
- CommonMark 规范（最接近现代标准的）：https://commonmark.org/

**TIPS**：  
大多数平台都**高度兼容 GitHub Flavored Markdown (GFM)**，所以先掌握 GitHub 的官方指南，就能覆盖 80% 的使用场景。遇到平台特定差异时，再查对应平台的文档。

<br>
<br>
<br>
<br>

# markdown的各平台差异

虽然 Markdown 的**核心语法**（如标题 `#`、列表、粗体`**`**、链接等）基本通用，但不同平台会基于 **CommonMark** 标准进行扩展、修改或限制，导致**具体写法和支持的功能不同**。这被称为 “Markdown Flavors”（Markdown 风味/方言）。

### 常见差异例子

以下是几个典型平台的对比（2026 年当前情况）：

| 功能 | GitHub / GitLab (GFM) | Reddit | Stack Overflow | 语雀 / 知乎 | Typora / Obsidian（本地） |
|------|-----------------------|--------|----------------|-------------|-------------------------|
| **表格** | 支持<br>`\| 列1 \| 列2 \|`<br>`\| --- \| --- \|` | 不支持原生表格 | 支持（有限） | 支持 | 完全支持 |
| **任务列表** | 支持<br>`- [x] 已完成` | 支持（但显示不同） | 支持 | 支持 | 支持 |
| **删除线** | `~~删除~~` | `~~删除~~` | `~~删除~~` | `~~删除~~` | 支持 |
| **代码高亮** | ```` ```python ``` ````（支持语言） | ```` ```python ``` ```` | 支持 | 支持 | 支持 |
| **脚注** | 支持 `[^1]` | 不支持 | 支持 | 部分支持 | 支持 |
| **自动链接** | `https://...` 会自动变链接 | 类似 | 类似 | 类似 | 取决于设置 |
| **表情符号** | `:smile:` → 😄 | `:smile:` | 不支持 | 支持部分 | 支持 |
| **标题最大层级** | 6 级 | 6 级 | 6 级 | 通常 6 级 | 无限制 |
| **HTML 嵌入** | 有限支持 | 严格限制 | 严格限制 | 基本不支持 | 完全支持 |

### 更具体的书写差异举例

1. **表格写法**（最常见差异）
   - **GitHub / 语雀**：可以这样写（推荐）
     ```markdown
     | 姓名 | 年龄 | 城市 |
     |------|------|------|
     | 张三 | 25   | 香港 |
     ```
   - **Reddit**：不支持原生表格，通常要用图片或 ASCII 艺术代替。

2. **任务清单**
   - **GitHub**：
     ```markdown
     - [x] 完成的事
     - [ ] 未完成
     ```
   - 部分老平台可能只支持 `- [x]` 但渲染效果不同。

3. **数学公式（LaTeX）**
   - **GitHub**：不支持原生，需要用 `$` 但渲染较差。
   - **语雀、Notion、Obsidian**：强烈支持 `$$` 或 `$`。
   - **知乎**：支持但需要特定包裹。

4. **引用块嵌套**
   - 大部分平台支持多级 `>`，但渲染样式差异很大。

5. **扩展语法**
   - **GitHub**：支持 `![]()` 图片 + `alt` 文字 + title。
   - **部分平台**：不支持图片 title 属性。
   - **微信公众号**：几乎不支持标准 Markdown，要用它的专有格式。

### TIPS：
- **写博客/文档** → 用 **GFM**（GitHub Flavored Markdown），兼容性最广。
- **跨平台** → 尽量只用**核心语法**（#、**、[]()、-、1. 等），避免高级扩展。
- **测试** → 在对应平台直接预览，很多人会因为“在 Typora 里好看，上传后全乱”而踩坑。




