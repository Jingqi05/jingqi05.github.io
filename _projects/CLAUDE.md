# _projects/ — 项目展示

"Projects" 页面和首页 "Selected Projects" 板块的内容源。按年份分子目录存放。

## 文件格式

```yaml
---
title: "项目名称"
date: YYYY-MM-DD HH:MM:SS +0800
selected: true                    # true = 显示在首页
description: >-
  项目简介
cover:                            # 封面图路径，留空则自动生成 SVG 占位图
links:
  Code: https://github.com/...
---
```

## 显示逻辑

- 首页：筛选 `selected: true`，按 `date` 降序
- 项目页：显示所有项目
