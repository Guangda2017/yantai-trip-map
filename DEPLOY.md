# GitHub Pages 发布指南

本目录已经是一个可直接发布的静态网站：`index.html` 位于项目根目录，不需要安装 Node.js 或执行构建命令。

git init
git add .
git commit -m "发布烟台行程地图"
gh repo create yantai-trip-map --public --source=. --remote=origin --push
```

然后到新建的 GitHub 仓库网页中开启 Pages：

1. 打开仓库的 **Settings** → **Pages**。
2. 在 **Build and deployment** 中选择 **Deploy from a branch**。
3. Branch 选择 `main`，Folder 选择 `/ (root)`。
4. 点击 **Save**。
5. 等待约 1–3 分钟，页面会显示线上地址，通常为：

```text
https://<GitHub用户名>.github.io/yantai-trip-map/
```

## 改成私有分享

GitHub Pages 的公开仓库最简单。若不希望页面公开，可选择：

- 使用 Vercel 的访问保护；或
- 使用 Cloudflare Pages Access；或
- 在发布前删除所有酒店电话、具体住宿信息等不适合公开的内容。

## 常见问题

### 页面打开了但地图是空白

页面本身已部署，但 Leaflet 和 OpenStreetMap 底图需联网加载。请检查当前网络能否访问 `unpkg.com` 与 `tile.openstreetmap.org`。

### 为什么加了 `.nojekyll`

它会让 GitHub Pages 原样提供静态文件，避免 Jekyll 对文件路径作额外处理。
