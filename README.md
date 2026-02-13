# Pure Read 官网

本目录为 Pure Read 的静态官网，介绍扩展与规则仓库，无构建步骤。

## 本地预览

- 直接用浏览器打开 `index.html`，或
- 使用本地静态服务，例如：
  ```bash
  npx serve .
  ```
  然后访问提示的地址（如 http://localhost:3000）。

## 部署

将本目录整体部署到任意静态托管即可，例如：

- **Nginx**：将 `pure-read-site` 目录内容放到站点根或子路径（如 `/` 或 `/pure-read/`）。
- **GitHub Pages**：在仓库设置中指定 Source 为本目录，或使用 GitHub Actions 将本目录发布到 `gh-pages`。
- **Vercel / Netlify**：将本目录设为项目根，发布为静态站点。

无需安装依赖或执行构建命令。
