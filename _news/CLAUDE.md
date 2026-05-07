# _news/ — 新闻动态

首页 "News" 板块的内容源。每个 `.md` 文件是一条新闻。

## 文件格式

```yaml
---
title: >-
  新闻标题
date: YYYY-MM-DD HH:MM:SS +0800
---
```

- 文件名建议格式：`YYYY-MM-DD-简短描述.md`
- `date` 决定排序（新的在前）和显示的年份/日期

## 显示逻辑

`index.html` 按 `date` 降序排列，最多显示 `display.yml` 中 `num_news` 条。
