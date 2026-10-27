# 审计报告预览原型 · GitHub Pages 部署包

## 文件说明
- `index.html`  原型本体（单文件，无外链依赖）
- `.nojekyll`   关闭 Jekyll 处理，保证文件按原样发布
- `robots.txt`  禁止搜索引擎收录
- `_headers`    仅 Cloudflare Pages / Netlify 生效，GitHub Pages 会忽略（无害）

## 部署步骤（网页操作，无需命令行）
1. 打开 https://github.com/new ，仓库名填 `audit-report-proto`，可见性选 **Public**，不要勾选任何初始化文件，点 Create repository。
2. 在空仓库页点 **uploading an existing file**。
3. 把本目录下 4 个文件全部拖进去（`.nojekyll` 是隐藏文件，需在资源管理器里开启"显示隐藏项目"才能选中；漏传也能正常访问，只是会走一遍 Jekyll）。
4. Commit changes。
5. 进入 **Settings → Pages**，Source 选 `Deploy from a branch`，Branch 选 `main` + `/ (root)`，Save。
6. 等 1–2 分钟，页面顶部出现 `Your site is live at ...`，地址形如：
   `https://<你的用户名>.github.io/audit-report-proto/`

## 注意事项
- 首次发布有 1–2 分钟延迟，期间访问 404 属正常。
- 该仓库为公开仓库，源码与页面均可被访问；仓库已加 noindex 与 robots 屏蔽，但请勿放真实审计数据。
- 后续更新原型：重新上传覆盖 `index.html`，等 1 分钟左右刷新即可（可能有浏览器缓存，用无痕窗口核对）。
- 墨刀里嵌入时，组件尺寸建议 `1440x900`。