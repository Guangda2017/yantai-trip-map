# 烟台长辈慢节奏 3 日行程地图

一个可直接部署到 GitHub Pages、Vercel 或 Cloudflare Pages 的静态行程地图。

## 文件说明

```text
.
├── index.html       # 网站首页与地图正文
├── .nojekyll        # 告知 GitHub Pages 不使用 Jekyll 处理
├── README.md        # 项目说明
├── DEPLOY.md        # GitHub Pages 发布步骤
└── .gitignore       # 本地系统文件忽略规则
```

## 本地预览

直接双击 `index.html` 可查看页面。若浏览器限制本地定位权限，可在目录内运行：

```bash
python3 -m http.server 8080
```

再访问：<http://localhost:8080>

## 更新地图

编辑 `index.html` 后，推送到 GitHub 的 `main` 分支即可自动更新线上页面。详情见 [DEPLOY.md](./DEPLOY.md)。

## 注意事项

- Leaflet 与 OpenStreetMap 底图通过网络加载；访问地图时需要网络连接。
- 发布公开网站前，请勿写入订单号、身份证件信息、手机号、实时房间号等个人隐私。
- 文中少数酒店点位为区域参考，出发前应以酒店确认地址和导航结果为准。
