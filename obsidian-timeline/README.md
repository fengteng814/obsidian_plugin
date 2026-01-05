# Timeline – Obsidian 插件

一个在 Obsidian 笔记里渲染精美且可配置时间线的插件。

## 功能

- 支持两种时间线格式：
  - `timeline` 代码块：使用简洁的 `+` 前缀三行一组语法。
  - `timeline-labeled` 代码块：使用显式的 `date`、`title`、`content` 字段。
- 允许为单条时间线添加类名，定制线条样式、卡片样式、间距、隐藏标题和激活色。
- 事件标题与描述支持 Markdown。

## 安装

1. 将本仓库内容放入你的仓库目录 `.obsidian/plugins/obsidian-timeline/`。
2. 重启 Obsidian。
3. 打开 **Settings → Community plugins**，启用 **Timeline**。

## 基本用法

创建 `timeline` 代码块，每个事件使用三行 `+` 前缀，分别代表时间、标题和描述。

````markdown
```timeline
+ 2020-01-01
+ 项目启动
+ 定义目标与成功标准。

+ 2020-06-15
+ Beta 发布
+ 将首个 Beta 版本交付早期测试者。
```
````

### 标注式语法

如果想显式写出字段，可使用 `timeline-labeled`。每个事件以 `date:` 开头，可选 `title:`、`content:` 行。

````markdown
```timeline-labeled
date: 2021-03-01
title: 调研阶段
content: 收集用户访谈与早期数据。

date: 2021-04-10
title: 原型
content: 构建首个可交互原型。
```
````

## 使用类名定制样式

在代码块顶部用方括号写入类名（如 `[class-a, class-b]`），这些类会应用到渲染后的时间线元素。

````markdown
```timeline
[line-3, body-2, hide-titles]
+ 2022-01-01
+ 静默上线
+ 面向小范围用户的软发布。
```
````

常用类名（可组合使用）：

- 线条样式：`line-2`、`line-3`、`line-4`、`line-5`
- 卡片样式：`body-2`、`body-3`、`body-4`
- 布局调整：`spaced-lines`、`hide-titles`
- 激活色覆盖：`active-color-background-modifier-success`、`active-color-background-modifier-error`、`active-color-background-modifier-error-hover`、`active-color-text-accent`、`active-color-text-accent-hover`、`active-color-text-error`、`active-color-text-error-hover`、`active-color-text-selection`、`active-color-interactive-accent`、`active-color-interactive-accent-hover`、`active-color-interactive-success`

## 小贴士

- 标题和描述都可使用 Markdown（列表、链接等）。
- 使用 `timeline` 格式时，确保每个事件都有三行 `+` 内容；多余内容会被忽略。
- 类名应放在代码块内容最上方，以便被正确识别。
