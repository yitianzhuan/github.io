# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 项目概述

这是一个使用 Hexo 的 GitHub Pages 技术博客，部署于 `yitianzhuan.github.io`。

## 常用命令

```bash
# 创建新文章
hexo new "文章标题"

# 启动本地开发服务器（端口 4000）
hexo server

# 生成静态文件到 public/ 目录
hexo generate

# 清除缓存和生成的文件
hexo clean

# 完整部署流程（清理、生成、部署）
npm run deploy:build
```

## 核心目录结构

```
.
├── _config.yml              # 主站点配置文件
├── source/
│   └── _posts/             # 博客文章目录
├── themes/                 # 主题文件夹
├── public/                 # 生成的静态文件（不提交到 Git）
└── .github/workflows/
    └── deploy.yml          # GitHub Actions 部署配置
```

## 开发工作流

1. 使用 `hexo server` 进行本地预览
2. 提交到 main 分支后，GitHub Actions 自动构建并部署
3. 根配置文件（`_config.yml`）修改后需要重启服务器

## 重要注意事项

- 主题配置文件位于 `themes/[theme-name]/_config.yml`
- `public/` 目录应加入 `.gitignore`
- 使用 GitHub Actions 实现自动部署，无需本地执行 `hexo deploy`
- 主题配置文件修改后自动更新，无需重启服务器
