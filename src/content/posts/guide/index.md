---
title: 本地部署
published: 2026-01-30
description: 关于本地部署mizuki
tags: [教程, 代码]
category: 前端
draft: false
pinned: false
lang: zh-CN
---

# 🌸 Mizuki 本地部署教程

本文将详细介绍如何在自己的计算机上本地部署 Mizuki 静态博客系统。

# 📋 系统要求

- **Node.js**: 版本 ≥ 20.x
- **包管理器**: pnpm ≥ 9.x (推荐) 或 npm ≥ 8.x
- **Git**: 最新版本

# 🚀 快速开始

## 1. 克隆项目
```bush
 git clone https://github.com/matsuzaka-yuki/mizuki.git
cd mizuki
```

## 2. 安装依赖
### 安装 pnpm（如果还没有安装）
```bush
 npm install -g pnpm
```

### 安装项目依赖
```bush
pnpm install
```

## 3. 基础配置
### 修改 src/config.ts 文件：
```typescript
export const siteConfig: SiteConfig = {
  title: "您的博客名称",
  subtitle: "博客描述",
  lang: "zh-CN",
  themeColor: {
    hue: 210,
    fixed: false,
  },
  banner: {
    enable: true,
    src: ["assets/banner/1.webp"],
    carousel: {
      enable: true,
      interval: 0.8,
    },
  },
};
```

## 4. 启动开发服务器
```bash
pnpm dev
```

访问 http://localhost:4321 查看效果。

## 📝 内容管理
### 创建新文章
```bash
pnpm new-post "我的第一篇文章"
```
文章将创建在 src/content/posts/ 目录下。

### 文章 Frontmatter 示例
```yaml
---
title: 文章标题
published: 2026-01-30
description: 文章描述
image: ./cover.jpg
tags: [标签1, 标签2]
category: 分类
draft: false
pinned: false
---
```
## 📁 项目结构
```text
mizuki/
├── src/
│   ├── components/     # 组件
│   ├── content/        # 博客内容
│   ├── layouts/        # 布局组件
│   ├── pages/          # 页面
│   └── config.ts       # 配置文件
├── public/             # 静态资源
├── package.json        # 依赖配置
└── README.md           # 说明文档
```
## 🔧 高级配置
## 自定义主题色
### 在 config.ts 中修改 themeColor.hue 值 (0-360)：

```typescript
themeColor: {
  hue: 280,  // 紫色主题
  fixed: false,
}
启用/禁用功能
typescript
// 启用暗色主题切换
themeSwitcher: {
  enable: true,
  defaultTheme: "auto",
}

// 启用搜索功能
search: {
  enable: true,
  provider: "pagefind",
}
```
