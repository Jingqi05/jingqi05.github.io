---
title: "STM32 ECDH 智能门禁系统"
date: 2025-05-01 00:01:00 +0800
selected: true
description: >-
  基于 STM32F103 + ESP8266 的智能门禁系统，使用国密算法实现全链路安全通信。
  采用 SM2 ECDH 临时密钥协商建立安全通道，SM4-CTR 模式加密通信数据，
  SM3-HMAC 保障消息完整性与防重放。支持 RFID 卡认证、远程开门、
  云端管理服务器，实现了从嵌入式固件到云端的完整安全架构。
cover:
links:
  Code: https://github.com/Jingqi05/door-control-ecdh
---

## 系统架构

- **MCU**: STM32F103C8T6 + FreeRTOS 实时操作系统
- **通信**: ESP8266 WiFi 模块，TCP 协议连接云端
- **加密**: GmSSL 国密算法库（SM2/SM3/SM4）
- **外设**: RC522 RFID 读卡器、OLED 显示屏、舵机门锁、蜂鸣器

## 安全特性

- SM2 双向签名认证 + ECDH 临时密钥交换
- SM4-CTR 模式加密，计数器派生 IV 防止重用
- SM3-HMAC 截断 16 字节完整性校验
- 32 位单调计数器防重放攻击
- 临时密钥提供前向保密

## 安全审计

对系统进行了完整的密码学安全审计，覆盖算法层和实现层共 12 类经典攻击分析，
发现并记录了 8 个实现层安全问题（弱 PRNG、MAC 验证顺序、TOFU 模式等），
制定了分阶段修复计划。
