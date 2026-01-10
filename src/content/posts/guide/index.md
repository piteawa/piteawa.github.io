---
title: “寻隐轩”
published: 2026-01-10
description: “记录我使用Mizuki主题，从本地配置到部署至GitHub Pages的完整过程与遇到的问题。”
image: “./cover.png”
tags: [“博客搭建”, “Mizuki”, “Astro”, “GitHub Pages”, “个人博客”]
category: 技术实践
draft: false
author: 皮特
---
**系统环境要求**：
- Node.js (我用的 v24.12.0)
- pnpm (包管理器，比 npm 更快)
- Git

**克隆项目**：
打开终端，一行命令即可获得所有源代码：
```bash
git clone https://github.com/matsuzaka-yuki/mizuki.git
cd mizuki
pnpm install