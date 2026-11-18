# MyST 使用注意事项

## URL 与目录结构

**问题：** `connect/index.md` 部署后无法通过 `/connect/` 访问，返回 404。

**原因：** MyST book-theme 默认展平目录结构。`connect/index.md` 的 slug 被解析为根路径 `/`，与项目根 `index.md` 冲突，内容合并到主页面中，不生成独立页面。

**解决：** 在 `myst.yml` 的 `site` 段添加：

```yaml
site:
  template: book-theme
  options:
    folders: true
```

设置后 `connect/index.md` 会生成在 `/connect/` URL，`connect/memo.md` 会生成在 `/connect/memo/`。

## 模板下载

**问题：** `myst build --html` 卡在 "Fetching template" 步骤，超时后构建失败。

**原因：** MyST 首次构建时会从 GitHub 下载 book-theme 模板（`https://github.com/myst-templates/book-theme/archive/refs/heads/main.zip`）。在网络受限的环境中，下载请求可能被阻断或超时。

**解决：** 
- 设置 HTTP 代理：`HTTPS_PROXY=http://127.0.0.1:7890 myst build --html`
- 或从已构建的项目复制 `_build/templates/site/myst/book-theme/` 目录到新项目

## Node 版本要求

**问题：** CI 在 "Build HTML Assets" 步骤快速失败（10–25 秒），构建日志提示 `Please update your Node or NPM versions.`

**原因：** `npm install -g mystmd` 安装的是最新版 mystmd，从 1.13.0 起要求 Node >= 22。myst 启动时会做版本校验，workflow 里若固定 `node-version: 18.x`，校验失败即中止构建，跟文档内容无关。这个坑随 2026-11-12 发布的 mystmd 1.13.0 出现——此前 1.12.0 支持 Node 18，同样的配置可以构建成功。

**解决：** 把 workflow 中 `setup-node` 的版本改为 22：

```yaml
- uses: actions/setup-node@v4
  with:
    node-version: 22
```

**排查提示：** 若同一组织内内容相近的 workflow 仍在成功，先对照它的 Node 版本——大概率就是版本差异。

## 构建输出

`myst build --html` 输出到 `_build/html/` 目录。book-theme 是 SPA，所有页面的 HTML 内容通过 JSON 文件加载，主 `index.html` 是壳页面。非 `index.md` 文件（如 `memo.md`）会生成独立目录（如 `/memo/`）和对应的 JSON 数据文件。

## GitHub Pages 部署

部署工作流由 `myst init --gh-pages` 自动生成，包含以下关键配置：

```yaml
env:
  BASE_URL: /${{ github.event.repository.name }}
```

`BASE_URL` 必须设置为仓库名，否则页面资源路径错误。三个工作手册仓库的配置：

- `quanttide-handbook-of-business-entity`
- `quanttide-tutorial-of-business-entity`
- `quanttide-bylaw-of-business-entity`

部署后页面地址格式为 `https://quanttide.github.io/{仓库名}/{路径}/`。
