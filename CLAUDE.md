# 李景奇个人主页 — Jekyll GitHub Pages

基于 [academic-homepage](https://github.com/luost26/academic-homepage) 模板的个人学术主页。

## 构建与预览

```bash
bundle install                # 安装依赖
bundle exec jekyll serve      # 本地预览 → http://127.0.0.1:4000/
```

## 部署

推送到 GitHub 仓库 `Jingqi05/jingqi05.github.io` 的 `master` 分支，
GitHub Actions 自动构建部署到 https://jingqi05.github.io/。

需要代理推送时：
```bash
git config http.proxy http://127.0.0.1:10808
git config https.proxy http://127.0.0.1:10808
git push
```

## 目录结构

```
├── _data/              站点数据（profile.yml 等）
├── _includes/          HTML 模板片段（导航栏、页脚、各 widget）
├── _layouts/           页面布局模板（default.html）
├── _news/              新闻动态条目
├── _projects/          项目展示条目
├── _publications/      论文发表条目
├── _showcase/          个人展示内容
├── assets/             静态资源（图片、CSS、JS、简历）
├── .github/workflows/  GitHub Actions 部署配置
├── _config.yml         Jekyll 全局配置
├── index.html          首页模板
├── projects.html       项目页模板
├── publications.html   论文页模板
└── showcase.html       展示页模板
```

## 站点运作流程

### 1. 数据驱动

所有内容通过 `_data/` 中的 YAML 文件和各集合（`_news/`、`_projects/`、`_publications/`、`_showcase/`）中的 Markdown 文件提供。

### 2. 模板渲染

```
index.html → 引用 _includes/widgets/*.html → 读取 _data/*.md 和集合数据 → 生成 HTML
```

首页渲染顺序：
1. `profile_card.html` — 读取 `profile.yml`（头像、简介、邮箱、GitHub）
2. `experience_card.html` — 读取 `profile.yml`（教育、经历、奖项）
3. `news_card.html` — 读取 `_news/*.md`（新闻动态）
4. `publication_card.html` — 读取 `_publications/` 中 `selected: true` 的论文
5. 项目卡片 — 读取 `_projects/` 中 `selected: true` 的项目
6. Showcase 卡片 — 读取 `_showcase/` 中 `show: true` 且 `group: "Not Just Research"` 的项目

### 3. 构建部署

```
git push → GitHub Actions → Ruby + Jekyll build → _site/ → GitHub Pages
```

## 常用编辑操作

| 操作 | 修改文件 |
|------|----------|
| 修改个人信息/简介/头像 | `_data/profile.yml` |
| 添加/修改获奖 | `_data/profile.yml` 的 `awards` 部分 |
| 添加/修改经历 | `_data/profile.yml` 的 `experience` 部分 |
| 添加新闻 | 在 `_news/` 创建 `.md` 文件 |
| 添加项目 | 在 `_projects/YEAR/` 创建 `.md` 文件 |
| 添加论文 | 在 `_publications/YEAR/` 创建 `.md` 文件 |
| 显示/隐藏首页板块 | `_data/display.yml` |
| 修改导航栏 | `_data/navigation.yml` |
| 修改样式 | `assets/css/global.css` |
| 替换头像 | `assets/images/photos/profile.jpg` |
| 替换简历 | `assets/CV/cv.pdf` |

## 注意事项

- `_showcase/default/` 下大部分文件是模板演示内容（`show: false`），不要随意启用
- `assets/images/badges/TAMU.svg` 是占位 logo，可替换为学校 logo
- favicon 在 `_layouts/default.html` 中设置，当前为 `profile.jpg`
- `display.yml` 中 `show_visitor_statistics: false` 已关闭访客统计
