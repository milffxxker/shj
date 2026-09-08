# 施汉杰个人作品集

React + Vite 多页面感作品集。主页包含全屏首页、个人简介、作品目录和整屏联系方式；作品目录使用独立 URL 展示详情页。

## 本地运行

```bash
pnpm install
pnpm dev
```

构建生产版本：

```bash
pnpm build
```

## GitHub Pages 部署\n\n网站通过 `.github/workflows/deploy-pages.yml` 自动构建并发布到：\n\n<https://shjpersonal.github.io/shj/>\n\n推送到 `main` 分支后会自动重新部署。仓库的 **Settings → Pages → Source** 应设置为 **GitHub Actions**。工作流使用 `/shj/` 作为基础路径，确保 JavaScript、CSS、图片、视频和作品详情页在项目站点子目录下都能正确访问。\n\n## 素材替换

- 将个人照片替换到 `public/assets/`，并修改 `src/App.jsx` 中人物图路径。
- 将首页视频命名为 `hero-loop.mp4` 放入 `public/assets/`；当前会自动使用 `hero.png` 作为回退海报。
- 作品标题、类型、封面和路由集中在 `src/App.jsx` 顶部的 `projects` 数组中。
- 点击作品封面进入 `/work/项目名称`；详情页已预留封面首屏、项目介绍和四个作品图片区域。
