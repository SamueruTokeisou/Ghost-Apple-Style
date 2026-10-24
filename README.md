# Ghost-Apple-Style · Reading v3

为 Ghost / Casper 文章页提供 Apple 风格的阅读界面：磨砂玻璃目录、清晰排版、代码复制与深浅色切换。

Apple-inspired reading enhancements for Ghost / Casper, built with vanilla CSS and JavaScript. No jQuery or external libraries required.

[在线示例](https://www.286163668.xyz/ghost-blog/)

## 本版功能

- 桌面右侧磨砂玻璃目录，带 SVG 线条图标、章节数量、当前章节高亮和阅读进度。
- 自动提取正文 H2–H4；至少 3 个符合条件的标题才生成目录。Ghost 卡片内的标题不计入。
- 目录不折叠。宽度 ≥1200px 时在右侧显示；阅读正文时出现，离开正文后隐藏。较窄屏幕在正文前完整展开。
- 保留文章已有标题 ID 与链接；仅在目录中省略 emoji，正文内容不变。
- Mac 风格代码栏、语言识别、一键复制；长代码单独横向滚动。
- 表格滚动容器、引用块、行内代码和图片样式。
- 跟随系统／浅色／深色三种外观，偏好保存在本机浏览器。
- 返回文章开头、顶部阅读进度条、键盘焦点提示与打印样式。
- 对部分原生页头／页脚链接文字做中文替换，保留链接目标。

## 安装（推荐：与当前线上部署一致）

1. 先备份 Ghost 后台 **Settings → Code injection** 中已有的内容。
2. 移除以前安装的本项目代码，避免旧版目录、复制按钮和样式重复；保留其他用途的注入代码。
3. 将 [ghost-reading-v3-header.html](ghost-reading-v3-header.html) 的完整内容（含 `<style>`）粘贴到 **Site header**。
4. 将 [ghost-reading-v3-footer.html](ghost-reading-v3-footer.html) 的完整内容（含 `<script>`）粘贴到 **Site footer**。
5. 保存并刷新文章页面。

Ghost 的页头注入放入页面 head，页脚注入放在页面底部。参见 [Ghost 官方 Code injection 文档](https://ghost.org/help/code-injection-styles/)。

### 单文件安装

根目录 [Ghost-Apple-Style](Ghost-Apple-Style) 保留旧入口，内容已更新为 v3 样式和脚本的合并包，可整体放入 **Site footer**。推荐使用上述分开安装方式，以便样式更早加载。**两种安装方式只能选一种。**

## 文件说明

| 文件 | 用途 |
| --- | --- |
| `ghost-reading-v3-header.html` | 当前线上使用的页头样式 |
| `ghost-reading-v3-footer.html` | 当前线上使用的页脚交互脚本 |
| `Ghost-Apple-Style` | v3 合并安装包，兼容原项目入口 |
| `CHANGELOG.md` | 本次更新及验证记录 |
| `legacy/Ghost-Apple-Style-v1.html` | 更新前原版代码备份，不要与 v3 同时安装 |
| `legacy/README-v1.md` | 更新前原说明存档，其中描述不适用于 v3 |

## 兼容范围与边界

本版针对当前站点的 **Casper 5.12.5** 页面结构适配。脚本的文章入口为：

```css
body.post-template article.article .gh-content
```

桌面布局还依赖 Casper 的 `.gh-canvas` 与命名网格。更换主题时需重新核对选择器与布局，不承诺兼容所有第三方主题或 Ghost 历史版本。

本版增强 Ghost 已渲染的文章 HTML，不替换 Markdown 解析器；不包含 Mermaid、数学公式、自动语法高亮或 Wiki.js 的全部扩展功能。不会修改 Ghost 主题文件或后台设置页面。

使用现代浏览器特性，包括 `backdrop-filter`、`color-mix()`、`dvh` 与 Unicode 正则表达式。已在当前 Edge 环境验证，未完成所有浏览器版本的兼容测试。复制优先使用 Clipboard API，失败时尝试选中并复制，最后提示手动复制。

## 自定义与排查

- 配色：调整页头 CSS 中的 `--read-ink`、`--read-muted`、`--read-panel`、`--read-blue` 等变量。
- 玻璃效果：调整 `.tr-toc` 的透明背景、模糊、边框和阴影。
- 目录位置：桌面目录横向位置由正文边界计算；不要仅修改固定的 right 值。
- 断点：如修改 1200px，需同步修改页头 CSS 和页脚脚本中的媒体查询。
- 目录未出现：确认文章结构匹配、符合条件的标题不少于 3 个，并已滚动到正文区域。
- 首页没有阅读工具属于预期行为；本版工具主要作用于文章页。
- 重复目录／按钮：移除旧版或其他目录插件，确保只安装一份本项目。
- 卸载：移除页头和页脚中本项目的注入块并刷新。文章内容和原有标题 ID 不会被写回修改。

## 作者与致谢

作者：[SamueruTokeisou](https://github.com/SamueruTokeisou) · [X / Twitter](https://x.com/TokeisouSamueru)

感谢 [Ghost](https://ghost.org/) 与 [Apple 设计资源](https://developer.apple.com/design/resources/) 带来的启发。本项目并非 Apple 官方产品。

原版 README 声明采用 MIT，但仓库此前未包含 LICENSE 文件；原说明已完整保存在 legacy 中，本次同步未新增或更改许可条款。
