---
title: "门禁云端服务器"
date: 2025-04-10 00:01:00 +0800
selected: false
description: >-
  基于 Python + FastAPI 的门禁系统云端服务器，提供 TCP 加密通信接口和 HTTP REST API。
  支持设备认证、卡管理、开门记录查询，前端使用 Vue 3 + Tailwind CSS 构建管理界面。
cover: /assets/images/covers/door-server.png
links:
  Code: https://github.com/Jingqi05/door-server
---

## 功能

- TCP 服务器处理 STM32/ESP32 设备的加密通信
- SM2 密钥协商 + SM4-CTR 加密会话
- HTTP REST API：设备管理、卡号管理、开门记录
- Vue 3 前端管理界面
- SQLite 数据库存储
