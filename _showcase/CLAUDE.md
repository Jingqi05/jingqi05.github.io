# _showcase/ — 个人展示

"Showcase" 页面和首页 "Not Just Research" 板块的内容源。

## 目录结构

- `default/` — 模板自带展示项（大部分 `show: false`）
- `self/` — 用户自定义展示项

## 文件格式

```yaml
---
title: "展示项标题"
show: true
width: 4                      # 列宽（1-12）
date: YYYY-MM-DD HH:MM:SS +0800
group: "Not Just Research"    # 首页只显示此组
---
```

## 显示逻辑

- 首页：`show: true` 且 `group: "Not Just Research"`，瀑布流布局
- 展示页：所有 `show: true` 的项目，按 `group` 分组
