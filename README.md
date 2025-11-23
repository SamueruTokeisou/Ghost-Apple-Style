# 🍎 Ghost-Apple-Style

**为 Ghost 博客打造的苹果风格增强包 / Apple-style Enhancement Package for Ghost Blog**

一个轻量级、零依赖的 Ghost 博客美化方案，让你的博客拥有 macOS/iOS 般的优雅设计。

*A lightweight, zero-dependency enhancement package that brings macOS/iOS elegance to your Ghost blog.*

---

## ✨ 特性 Features

### 🖥️ Mac 风格代码块 / Mac-style Code Blocks
- 经典的红黄绿三色窗口控制按钮 / Classic red-yellow-green window control buttons
- 动态语言标题识别 / Dynamic language title detection
- 一键复制代码功能 / One-click code copy button
- 毛玻璃质感 / Frosted glass effect
- 完美适配亮色/暗色模式 / Perfect light/dark mode support

### 📑 智能文章目录 / Smart Table of Contents
- 自动提取 H2/H3 标题 / Auto-extract H2/H3 headings
- iOS 风格的圆点指示器 / iOS-style dot indicators
- 流畅的悬停动画 / Smooth hover animations
- 响应式隐藏（小屏幕自动隐藏）/ Responsive hiding on small screens
- 毛玻璃半透明卡片 / Frosted glass translucent card

### ⬆️ 返回顶部按钮 / Back to Top Button
- 纯 CSS 绘制的箭头图标 / Pure CSS arrow icon
- 毛玻璃背景效果 / Frosted glass background
- 平滑滚动动画 / Smooth scroll animation
- 悬停上浮交互 / Hover lift interaction

### 🌓 完整暗色模式支持 / Full Dark Mode Support
- 自动跟随系统主题 / Auto follow system theme
- 所有组件完美适配 / All components perfectly adapted

---

## 🚀 快速开始 Quick Start

### 安装方法 Installation

1. **登录 Ghost 后台 / Login to Ghost Admin**
   ```
   https://your-blog.com/ghost
   ```

2. **进入代码注入设置 / Navigate to Code Injection**
   ```
   设置 Settings → 代码注入 Code Injection → 站点页脚 Site Footer
   ```

3. **复制粘贴代码 / Copy and Paste Code**
   
   将 `ghost-apple-style.html` 中的完整代码粘贴到 **Site Footer** 区域
   
   *Paste the complete code from `ghost-apple-style.html` into the **Site Footer** section*

4. **保存并刷新 / Save and Refresh**
   
   点击保存，然后刷新你的博客页面即可看到效果！
   
   *Click Save, then refresh your blog page to see the magic!*

---

## 📁 文件说明 File Description

```
Ghost-Apple-Style/
├── ghost-apple-style.html    # 完整的代码包（CSS + JS）/ Complete package (CSS + JS)
├── README.md                  # 项目说明文档 / Project documentation
├── preview/                   # 预览截图 / Preview screenshots
│   ├── light-mode.png        # 亮色模式预览 / Light mode preview
│   └── dark-mode.png         # 暗色模式预览 / Dark mode preview
└── LICENSE                    # MIT 许可证 / MIT License
```

---

## 🎨 效果预览 Preview

### 亮色模式 Light Mode
![Light Mode Preview](preview/light-mode.png)

### 暗色模式 Dark Mode
![Dark Mode Preview](preview/dark-mode.png)

---

## ⚙️ 自定义配置 Customization

### 修改文章目录位置 / Change TOC Position

在 CSS 中修改以下代码：

*Modify the following code in CSS:*

```css
#toc-sidebar-container {
    top: 120px;        /* 距离顶部距离 / Distance from top */
    right: 30px;       /* 距离右侧距离 / Distance from right */
    width: 280px;      /* 宽度 / Width */
}
```

### 修改返回顶部按钮位置 / Change Back-to-Top Position

```css
#back-to-top {
    bottom: 30px;      /* 距离底部距离 / Distance from bottom */
    right: 30px;       /* 距离右侧距离 / Distance from right */
}
```

### 修改代码块圆角 / Change Code Block Border Radius

```css
.mac-window-code {
    border-radius: 8px;  /* 修改这个数值 / Change this value */
}
```

---

## 🔧 兼容性 Compatibility

### 支持的浏览器 Supported Browsers
- ✅ Chrome 90+
- ✅ Safari 14+
- ✅ Firefox 88+
- ✅ Edge 90+

### 支持的 Ghost 版本 Supported Ghost Versions
- ✅ Ghost 4.x
- ✅ Ghost 5.x

### 支持的主题 Supported Themes
- ✅ Casper (官方主题 / Official theme)
- ✅ Casper Legacy
- ✅ 大多数第三方主题 / Most third-party themes

---

## 💡 常见问题 FAQ

### Q: 代码不生效怎么办？/ Code doesn't work?
**A:** 
1. 确保代码粘贴在 **Site Footer** 而不是 Site Header
   
   *Make sure code is pasted in **Site Footer**, not Site Header*

2. 清除浏览器缓存后刷新页面
   
   *Clear browser cache and refresh the page*

3. 检查是否有其他 CSS/JS 冲突
   
   *Check for CSS/JS conflicts with other code*

### Q: 文章目录不显示？/ TOC not showing?
**A:** 
文章目录需要文章中至少有一个 H2 或 H3 标题才会显示。

*TOC requires at least one H2 or H3 heading in your post to appear.*

### Q: 暗色模式不工作？/ Dark mode not working?
**A:** 
确保你的系统或浏览器设置了暗色模式偏好设置。

*Make sure your system or browser has dark mode preference enabled.*

### Q: 可以只使用部分功能吗？/ Can I use only certain features?
**A:** 
可以！在代码中找到对应的 CSS/JS 部分删除即可。

*Yes! Simply remove the corresponding CSS/JS sections in the code.*

---

## 🛠️ 技术栈 Tech Stack

- **纯 CSS3** - 无需任何 CSS 框架 / Pure CSS3, no frameworks needed
- **原生 JavaScript** - 依赖 jQuery（Ghost 自带）/ Native JS with jQuery (included in Ghost)
- **响应式设计** - 完美适配移动端 / Responsive design for mobile
- **性能优化** - 零额外 HTTP 请求 / Zero additional HTTP requests

---

## 📄 开源协议 License

本项目采用 [MIT License](LICENSE) 开源协议。

*This project is licensed under the [MIT License](LICENSE).*

你可以自由地：
- ✅ 商业使用 / Commercial use
- ✅ 修改代码 / Modify
- ✅ 分发代码 / Distribute
- ✅ 私人使用 / Private use

唯一要求：保留原作者版权声明。

*The only requirement: Keep the original copyright notice.*

---

## 🤝 贡献 Contributing

欢迎提交 Issue 和 Pull Request！

*Issues and Pull Requests are welcome!*

### 贡献指南 Contributing Guidelines

1. Fork 本项目 / Fork this repository
2. 创建特性分支 / Create your feature branch
   ```bash
   git checkout -b feature/AmazingFeature
   ```
3. 提交更改 / Commit your changes
   ```bash
   git commit -m 'Add some AmazingFeature'
   ```
4. 推送到分支 / Push to the branch
   ```bash
   git push origin feature/AmazingFeature
   ```
5. 创建 Pull Request / Open a Pull Request

---

## 🌟 Star History

如果这个项目对你有帮助，请给它一个 ⭐️ 星标！

*If this project helps you, please give it a ⭐️ star!*

---

## 📧 联系方式 Contact

- **作者 Author:** SamueruTokeisou
- **X (Twitter):** [@TokeisouSamueru](https://x.com/TokeisouSamueru)
- **GitHub:** [@SamueruTokeisou](https://github.com/SamueruTokeisou)

---

## 🙏 致谢 Acknowledgments

感谢以下项目和资源的启发：

*Thanks to the following projects and resources for inspiration:*

- [Ghost](https://ghost.org/) - 优秀的开源博客平台 / Excellent open-source blogging platform
- [Apple Design Resources](https://developer.apple.com/design/resources/) - 苹果设计指南 / Apple design guidelines
- [Clipboard.js](https://clipboardjs.com/) - 代码复制功能灵感 / Code copy inspiration

---

## 📝 更新日志 Changelog

### v1.0.0 (2025-01-xx)
- 🎉 初始版本发布 / Initial release
- ✨ Mac 风格代码块 / Mac-style code blocks
- ✨ 智能文章目录 / Smart table of contents
- ✨ 返回顶部按钮 / Back to top button
- 🌓 完整暗色模式支持 / Full dark mode support

---

<div align="center">

**用 ❤️ 和 ☕️ 制作 / Made with ❤️ and ☕️**

如果你喜欢这个项目，不妨请我喝杯咖啡？

*If you like this project, buy me a coffee?*

[![Buy Me A Coffee](https://img.shields.io/badge/Buy%20Me%20A%20Coffee-支持作者-orange?style=for-the-badge&logo=buy-me-a-coffee)](https://www.buymeacoffee.com/yourusername)

</div>
