# VoiceFlow 产品设计文档 | Product Design Document

[English](#english) | [中文](#中文)

---

## English

# VoiceFlow - Voice-First Productivity Mini Program

<p align="center">
  <strong>Voice-First Productivity Tool for Mobile Scenarios</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Platform-WeChat%20Mini%20Program-brightgreen?style=flat-square" alt="Platform">
  <img src="https://img.shields.io/badge/Status-In%20Development-blue?style=flat-square" alt="Status">
  <img src="https://img.shields.io/badge/Language-40%2B-orange?style=flat-square" alt="Languages">
</p>

## Overview

VoiceFlow is a voice-first productivity tool designed specifically for mobile scenarios. By deeply integrating AI capabilities with daily workflows, it enables users to complete meeting recording, content creation, and information organization with just one tap—without complex operations.

### Key Features

| Feature | Description |
|---------|-------------|
| **Meeting Elf** | Floating button design, one-tap start/stop recording, real-time speech-to-text with bilingual support (Chinese/English), auto-generated meeting summaries and to-dos |
| **Voice Dictation** | Global shortcut activation from any app, offline-first local speech recognition, 40+ language support, intelligent punctuation with 98% accuracy |
| **Voice Notes** | AI-powered organization, automatic transcription, smart tagging (#work #meeting #ideas #todo), semantic search |
| **AI Agent** | Voice-controlled scheduling, research assistance, content creation, translation support |

## Technical Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                    Presentation Layer                        │
│         WeChat Mini Program  │  iOS App  │  Android App     │
├─────────────────────────────────────────────────────────────┤
│                     Service Layer                            │
│    Speech Recognition API  │  AI Model  │  Business Logic  │
├─────────────────────────────────────────────────────────────┤
│                      Data Layer                              │
│       User Data  │  Note Storage  │  Model Training Data    │
└─────────────────────────────────────────────────────────────┘
```

**Privacy First**: Local speech recognition + edge AI models protect user data security.

## Development Roadmap

| Phase | Timeline | Features |
|-------|----------|----------|
| **MVP** | Month 1-2 | Basic voice recording, text transcription, note storage |
| **V1.0** | Month 3-4 | AI summarization, multilingual support |
| **V2.0** | Month 5-6 | AI Agent, calendar integration, third-party apps |
| **V3.0** | Month 7-8 | Enterprise features, team collaboration, advanced analytics |

## Pricing Plans

| Plan | Price | Features |
|------|-------|----------|
| **Free** | ¥0 | 100 voice sessions/day, basic transcription, 100 notes storage |
| **Pro** | ¥30/month | Unlimited voice, AI summarization, unlimited notes, multilingual |
| **Enterprise** | ¥99/month | Team collaboration, API access, dedicated support, data analytics |

## Competitive Advantages

| Feature | VoiceFlow | Competitors |
|---------|-----------|--------------|
| No meeting required | ✅ | ❌ |
| Global shortcut activation | ✅ | ❌ |
| 40+ language support | ✅ | ✅ |
| Offline local recognition | ✅ | ❌ |
| AI Agent integration | ✅ | ❌ |

## Performance Metrics

- < 0.5s response latency
- 98% recognition accuracy
- 40+ supported languages

## Quick Start

```bash
# Clone the repository
git clone https://github.com/cnshanrengo/voiceflow.git

# Install dependencies
npm install

# Start development server
npm run dev
```

## Tech Stack

- **Frontend**: WeChat Mini Program, iOS, Android
- **Backend**: FastAPI, Python
- **AI**: Speech Recognition, NLP, LLM

## Contact

- **WeChat**: xmcdws
- GitHub Issues: [https://github.com/cnshanrengo/voiceflow/issues](https://github.com/cnshanrengo/voiceflow/issues)

## License

MIT License

Copyright (c) 2026 VoiceFlow

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

---

## 中文

# VoiceFlow 语音优先生产力小程序

<p align="center">
  <strong>专为移动场景设计的语音优先生产力工具</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/平台-微信小程序-brightgreen?style=flat-square" alt="平台">
  <img src="https://img.shields.io/badge/状态-开发中-blue?style=flat-square" alt="状态">
  <img src="https://img.shields.io/badge/语言支持-40%2B-orange?style=flat-square" alt="语言">
</p>

## 产品概述

VoiceFlow 是一款专为移动场景设计的语音优先生产力工具，将 AI 能力与日常工作流深度融合。无需复杂操作，一键语音即可完成会议记录、内容创作、信息整理等任务。

### 核心价值

| 特点 | 说明 |
|------|------|
| **零门槛** | 按键即说，无需加入会议 |
| **全场景** | 任何应用内随时呼出 |
| **智能化** | AI 自动分类整理 |

## 核心功能

### 🤖 会议精灵 (Meeting Elf)
悬浮球设计，一键开始/结束录制
- 实时语音转文字，支持中英双语
- 自动生成会议摘要和待办事项
- 自动识别发言人
- 会议内容云端同步，多端查看
- 支持插入图片、文档标注

### 🎤 语音听写 (Voice Dictation)
- **全局快捷键**：任何应用内，通过悬浮球或快捷指令呼出听写
- **离线优先**：本地语音识别引擎，无网也能快速转写
- **40+语言支持**：普通话、粤语、英语、日语等主流语言
- **标点智能**：AI 自动添加标点，语义理解准确率 98%

### 📝 语音笔记 (Voice Notes)
AI 驱动的智能整理
1. 语音输入 - 随时随地语音记录
2. AI 转写 - 自动转为文字笔记
3. 智能分类 - AI 自动打标签归类
4. 检索回顾 - 语义搜索快速找到

### 🧠 AI 智能体 (AI Agent)
用语音控制一切，让 AI 成为你的私人助理

| 助手 | 示例 |
|------|------|
| 日程助手 | "帮我安排下周三下午3点开会" |
| 研究助理 | "帮我整理这份报告的核心观点" |
| 内容创作 | "写一封感谢客户的邮件" |
| 翻译官 | "把这段话翻译成英文" |

## 技术架构

```
┌─────────────────────────────────────────────────────────────┐
│                        表现层                                │
│              微信小程序  │  iOS App  │  Android App        │
├─────────────────────────────────────────────────────────────┤
│                        服务层                                │
│         语音识别 API  │  AI 模型服务  │  业务逻辑服务        │
├─────────────────────────────────────────────────────────────┤
│                        数据层                                │
│         用户数据  │  笔记存储  │  模型训练数据              │
└─────────────────────────────────────────────────────────────┘
```

**隐私优先**：本地语音识别 + 端侧 AI 模型，保护用户数据安全。

## 开发路线图

| 阶段 | 时间 | 功能 |
|------|------|------|
| **MVP** | 第 1-2 月 | 基础语音录制、文字转写、基础笔记存储 |
| **V1.0** | 第 3-4 月 | AI 摘要生成、语音听写、多语言支持 |
| **V2.0** | 第 5-6 月 | AI 智能体、日程集成、第三方应用对接 |
| **V3.0** | 第 7-8 月 | 企业版功能、团队协作、高级分析报表 |

## 商业模式

| 版本 | 价格 | 功能 |
|------|------|------|
| **免费版** | ¥0 | 每日 100 次语音、基础转写、100 条笔记存储 |
| **专业版** | ¥30/月 | 无限语音、AI 摘要、无限笔记、多语言 |
| **企业版** | ¥99/月 | 团队协作、API 接入、专属客服、数据报表 |

## 竞争优势

| 功能 | VoiceFlow | 竞品 |
|------|-----------|------|
| 无需加入会议 | ✅ | ❌ |
| 全局快捷呼出 | ✅ | ❌ |
| 40+ 语言支持 | ✅ | ✅ |
| 本地离线识别 | ✅ | ❌ |
| AI 智能体集成 | ✅ | ❌ |

## 性能指标

- < 0.5s 响应延迟
- 98% 识别准确率
- 40+ 支持语言

## 快速开始

```bash
# 克隆仓库
git clone https://github.com/cnshanrengo/voiceflow.git

# 安装依赖
npm install

# 启动开发服务器
npm run dev
```

## 技术栈

- **前端**：微信小程序、iOS、Android
- **后端**：FastAPI、Python
- **AI**：语音识别、自然语言处理、大语言模型

## 联系方式

- **微信**：xmcdws
- GitHub Issues: [https://github.com/cnshanrengo/voiceflow/issues](https://github.com/cnshanrengo/voiceflow/issues)

## 许可证

MIT License

版权所有 (c) 2026 VoiceFlow

特此向任何获得本软件及相关文档文件（"软件"）副本的人免费授予无限制使用、复制、修改、合并、发布、分发、再许可和/或销售本软件副本的权利，并允许向提供本软件的人这样做，但须遵守以下条件：

上述版权声明和本许可声明应包含在本软件的所有副本或主要部分中。

本软件按"原样"提供，不提供任何明示或暗示的保证，包括但不限于对适销性、特定用途适用性和非侵权性的保证。在任何情况下，作者或版权持有人均不对因本软件或使用或其他与本软件相关的交易而产生的任何索赔、损害或其他责任负责，无论是在合同、侵权或其他诉讼中。

---

*让每一次语音，都成为高效工作的起点。*
