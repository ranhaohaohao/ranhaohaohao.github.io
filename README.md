# 刘淏冉 · 个人学术主页

静态中文个人学术主页，用于在社团协会等场景中介绍个人教育背景、科研经历与项目经历，并支持在线预览、单独查看与下载简历。

## 文件结构

```text
liu-haoran-homepage/
├── index.html          # 主页（单页）
├── style.css           # 样式
├── script.js           # 导航菜单 / 当前年份等少量交互
├── 404.html            # 404 页面
├── favicon.svg         # 站点图标
├── README.md
├── .gitignore
└── assets/
    └── my-resume-v2.pdf  # 简历副本（原文为只读输入）
```

## 本地预览

在 `liu-haoran-homepage` 目录内运行：

```powershell
python -m http.server 8000
```

然后访问 <http://localhost:8000/>。

## 修改主页文字

所有内容都在 `index.html` 中，直接编辑对应板块的 HTML 文本即可；样式在 `style.css`，少量交互在 `script.js`。页面不依赖任何构建工具。

## 替换简历 PDF

1. 将新简历文件命名为 `my-resume-v2.pdf`；
2. 替换 `assets/my-resume-v2.pdf`；
3. 其余文件无需改动，预览与下载链接均指向该文件。

请保持文件名 `my-resume-v2.pdf` 不变。

## GitHub Pages 部署

1. 新建 GitHub 仓库（公开），例如 `<用户名>.github.io`；
2. 在 `liu-haoran-homepage` 目录内：
   ```powershell
   git init
   git add .
   git commit -m "init homepage"
   git branch -M main
   git remote add origin https://github.com/<用户名>/<仓库名>.git
   git push -u origin main
   ```
3. 在仓库 Settings → Pages 中选择 `main` 分支根目录发布。

## 如何更新网站

直接修改 `index.html` / `style.css`，提交并推送即可：

```powershell
git add .
git commit -m "update homepage"
git push
```
