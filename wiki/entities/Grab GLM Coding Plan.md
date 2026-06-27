---
title: "Grab GLM Coding Plan"
type: entity
category: project
tags:
  - entity
  - project
  - automation
  - glm
  - captcha
updated: 2026-06-27
---

# Grab GLM Coding Plan

智谱GLM Coding Plan套餐自动抢购助手，支持自动点选验证码。

## 基本信息

- **类型**：自动化工具
- **本地路径**：`D:\php_code\ai_project\grab-GLM-coding-plan-master`
- **功能**：GLM Coding Plan套餐准点自动抢购
- **验证码识别**：本地完成，不上传第三方
- **支持平台**：Windows, Linux, macOS
- **许可证**：仅供学习交流使用

## 核心功能

### 抢购功能
- 自动打开抢购页面
- 自动检测登录状态
- 倒计时到点自动选周期、点购买
- 遇到验证码自动识别并点选
- 抢到后停止点击，停在支付弹窗

### 验证码识别
- 本地OCR识别，无需第三方服务
- 自动处理多种验证码类型
- 识别失败自动"换一张"

### 反限流机制
- 系统繁忙（接口555/无套餐卡）时自动刷新重拉
- 指数退避重试，避免被单独限流
- 改写售罄数据、绕过限流

## 使用方式

### 方式一：Playwright（推荐）
- 一条命令启动，全程自动
- 新手推荐
- 需要在带桌面的环境运行

### 方式二：油猴脚本
- 浏览器里有可视化面板
- 需要手动把脚本粘进油猴扩展
- 需要单独开识别服务

## 技术栈

- **Python**：3.8+
- **Playwright**：浏览器自动化
- **验证码识别**：本地OCR

## 配置选项

| 配置项 | 说明 | 可选值 |
|--------|------|--------|
| targetPlan | 目标套餐 | Lite / Pro / Max |
| billingCycle | 计费周期 | month / quarter / year |
| targetHour | 目标时 | 0-23 |
| targetMinute | 目标分 | 0-59 |
| targetSecond | 目标秒 | 0-59 |

## 依赖项目

- **验证码识别核心**：MgArcher/Text_select_captcha
- **原始油猴脚本**：Linux Do社区@ballen

## 应用场景

- 抢智谱GLM Coding Plan套餐
- 自动化网页抢购流程
- 学习自动化测试

## 关联连接
- [[智谱GLM]] — 抢购的目标产品
- [[自动化工具]] — 项目类型
- [[本地项目汇总]] — 所属项目集合