---
title: "ESP32 门禁控制端"
date: 2025-04-15 00:01:00 +0800
selected: true
description: >-
  基于 ESP32 + PlatformIO 的门禁控制端固件，通过 WiFi 连接云端服务器，
  集成 CryptoSession 安全会话库实现加密通信。
  支持 RFID 卡读取、OLED 状态显示、蜂鸣器提示、舵机门锁控制，
  与 STM32 端配合构成完整的分布式门禁系统。
cover: /assets/images/covers/esp-doorcontrol.png
links:
  Code: https://github.com/Jingqi05/esp-doorcontrol
---

## 功能特性

- ESP32 WiFi 联网，TCP 长连接云端服务器
- CryptoSession 库实现 SM4 加密通信
- RC522 RFID 卡读取与认证
- OLED 中文显示（门禁状态、卡号信息）
- 舵机门锁控制 + 蜂鸣器状态提示
- PlatformIO 构建，模块化库设计（crypto、network、gmsslib）

## 技术栈

- **MCU**: ESP32 + ESP-IDF
- **加密**: GmSSL 移植版（SM2/SM3/SM4）
- **构建**: PlatformIO + CMake
- **库**: CryptoSession（安全会话）、gmsslib（国密算法）、network（WiFi/TCP）
