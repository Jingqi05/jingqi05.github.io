# _publications/ — 论文发表

"Publications" 页面和首页 "Selected Publications" 板块的内容源。

## 文件格式

```yaml
---
title: "论文标题"
date: YYYY-MM-DD HH:MM:SS +0800
selected: true
pub_post: "Published in 期刊名"
pub_date: "2025"
authors:
  - 作者1
  - 作者2
links:
  Paper: https://...
---
```

## 显示逻辑

- 首页：筛选 `selected: true`，按 `date` 降序
- 论文页：显示所有论文
- `authors` 中的名字如果在 `_data/authors.yml` 中有对应条目，会自动添加链接
