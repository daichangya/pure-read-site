# Pure Read 官网

本目录为 Pure Read 的静态官网，介绍扩展与规则仓库，无构建步骤。

## 支持语言

- **中文**、**English**：首页与隐私页支持中英切换，语言选择保存在浏览器 `localStorage`，下次访问会沿用。

## 本地预览

- 直接用浏览器打开 `index.html`，或
- 使用本地静态服务，例如：
  ```bash
  npx serve .
  ```
  然后访问提示的地址（如 http://localhost:3000）。

## 资源说明

- **产品预览图**：`assets/preview-reading.png` 为阅读模式界面截图，来源于主仓库 [assets/store/screenshots/](../assets/store/screenshots/)（如 `screenshot-bbc-640x400.png`），便于官网独立部署时自包含资源。
- **样式与脚本**：`assets/styles.css`、`assets/lang-switcher.js`，无第三方依赖。

## 部署

将本目录整体部署到任意静态托管即可，例如：

- **Nginx**：将 `pure-read-site` 目录内容放到站点根或子路径（如 `/` 或 `/pure-read/`）。
- **GitHub Pages**：在仓库设置中指定 Source 为本目录，或使用 GitHub Actions 将本目录发布到 `gh-pages`。
- **Vercel / Netlify**：将本目录设为项目根，发布为静态站点。

无需安装依赖或执行构建命令。

## 验收与测试建议

- **功能**：语言切换（中文/English）是否生效，主 CTA「添加至 Chrome」、锚点（功能、使用、预览、开发者）、Chrome 商店 / GitHub / 隐私 / 反馈链接是否可点击且目标正确。
- **兼容**：在 Chrome、Firefox、Safari 最新版及移动端竖屏下检查布局与可读性。
- **可访问性**：保留焦点可见（`:focus-visible`）、标题层级、按钮 `aria-pressed`；对比度符合 WCAG AA。
