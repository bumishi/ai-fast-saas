# Fast SaaS - 一小时上线AI收费应用的全栈脚手架

<div align="center">

![Nuxt Version](https://img.shields.io/badge/Nuxt-4.2-green.svg)
![Nuxt UI Version](https://img.shields.io/badge/Nuxt%20UI-4.1-blue.svg)


**快速构建您的面向全球用户的AI SaaS应用**

[演示站点](https://www.fast-saas.top/) · [AI应用示例](https://www.ai-photos.art/) · [功能文档](#-核心功能)

</div>

<div align="center">

![关注最新更新](https://www.fast-saas.top/wxmp-qr.jpg)

</div>

---

## 🎯 项目简介

**Fast SaaS** 是一个基于 Nuxt 4 构建的全栈 AI SaaS 应用启动模板，专为个人开发者和创业者打造。只需掌握 JavaScript 和 SQL 基础，即可在数小时内上线一个功能完整的 AI 收费应用。

### 为什么选择 Fast SaaS？

- ⚡ **极低上手门槛**：熟悉 Vue.js 和 SQL 即可快速上手，无需全栈经验
- 🚀 **开箱即用**：内置完整的用户中心、订阅计费、积分系统、支付集成
- 🤖 **AI 原生设计**：深度集成 LangChain，支持 OpenAI、OpenRouter、火山引擎等多种大模型
- 💰 **商业化就绪**：订阅 + 积分双计费模式，支持 Creem/Stripe 支付，国内用户支付宝收款
- 🔧 **完善的基础设施**：AI生成历史、异步任务队列、云存储、邮件通知、管理后台(/admin)一应俱全
- 🏗️ **生产级架构**：分层设计、类型安全、事务一致性、完善的错误处理和日志记录

## 🌐 演示站点

- **[Fast SaaS 官网](https://www.fast-saas.top/)** - 项目介绍和功能展示
- **[AI Photos Art](https://www.ai-photos.art/)** - 使用 Fast SaaS 构建的 AI 图片生成应用


## ✨ 核心功能

### 🤖 AI 应用开发能力

#### 多模型支持
- **OpenAI 协议兼容**：支持所有 OpenAI 协议兼容的大模型接入
- **OpenRouter 集成**：访问 100+ AI 模型，包括 GPT-4、Claude、Llama 等
- **火山引擎对接**：国内用户可无缝接入字节跳动 AI 模型
- **LangChain 集成**：强大的 AI 应用开发框架，轻松构建复杂 AI 功能

#### 完整的示例应用
提供开箱即用的 AI 功能示例，几分钟即可开发一个 AI 应用：
- **AI 图片生成**：图片生成、缩略图自动生成、云存储上传
- **通用异步任务处理**：大模型调用、图片处理、文档转换等耗时任务
- **通用ai生成历史**：内置通用的ai生成历史记录和生成结果展示，支持自定义业务分类

### 💳 商业化系统

#### 双积分计费模式
创新的积分管理系统，灵活满足不同用户需求：

**购买积分**（永不过期）
- 用户按需购买积分包
- 积分永久有效，用完为止
- 适合偶尔使用的用户

**订阅积分**（按周期重置）
- 订阅计划包含固定额度积分
- 每月自动重置，周期内用完可叠加购买
- 适合高频用户，最大化价值

**智能消费策略**
- 系统优先消耗订阅积分
- 订阅积分用完后自动切换到购买积分
- 用户体验最优，商家收益最大化

#### 灵活的计费规则
按实际业务操作扣费，简单直观：


### 🔐 完整的用户体系

#### 多种登录方式
- 邮箱密码登录
- Google OAuth
- GitHub OAuth
- 邮箱验证码登录/注册
- 密码重置

#### 安全保障
- JWT 双 Token 认证（Access Token + Refresh Token）
- 密码加密
- 统一的权限控制中间件
- 自动 Token 刷新机制

### 💰 支付与订阅

#### 多平台支付集成
- **Creem 支付**：国内用户通过支付宝实现海外收款
- **Stripe 支付**：全球主流支付平台
- **Webhook 处理**：完整的支付事件处理和幂等保护
- **支付历史**：完整的支付记录查询

#### 订阅管理
- 多种定价计划配置
- 月付/年付灵活切换
- 自动续费
- 订阅取消

### ⚙️ 基础设施

#### 异步任务队列系统
使用 **BullMQ + Redis** 构建的高性能异步任务处理系统：
- 前端提交耗时任务 → 返回任务 ID
- 后端异步处理任务（AI 生成、图片处理等）
- 前端轮询查询任务状态
- 完整的任务状态跟踪（pending、running、completed、failed）
- 支持任务取消和重试
- 后台支持任务失败退还积分

#### 云存储集成
- **默认七牛云**：国内稳定可靠的云存储
- 客户端和服务端双端上传支持
- 图片支持缩略图生成
- 灵活扩展其他云存储服务

#### 邮件通知系统
- 基于 Nodemailer 的邮件服务
- 支持验证码邮件、密码重置邮件
- 可自定义邮件模板
- 易于扩展通知场景

#### 权限控制
- 统一的认证中间件
- Admin 权限保护
- 路由级别权限控制
- 用户上下文自动注入

## 🛠️ 技术架构

### 前端技术栈

| 技术 | 说明 |
|------|------|
| **Nuxt 4** | 现代化全栈框架，支持 SSR、SSG、API 路由 |
| **Vue 3** | 渐进式 JavaScript 框架 |
| **Nuxt UI v4** | 美观现代的 UI 组件库 |
| **TypeScript** | 类型安全的 JavaScript 超集 |
| **Pinia** | 轻量级状态管理 |
| **Tailwind CSS** | 原子化 CSS 框架 |
| **Vue I18n** | 国际化支持 |

### 后端技术栈

| 技术 | 说明 |
|------|------|
| **Nitro** | Nuxt 4 内置服务器，支持多种部署场景 |
| **Drizzle ORM** | 类型安全的数据库 ORM，比 Prisma 更轻量 |
| **MySQL** | 可靠的关系型数据库 |
| **Zod** | Schema 验证库 |
| **jsonwebtoken** | JWT 令牌管理 |
| **BullMQ** | 基于 Redis 的任务队列 |
| **ioredis** | Redis 客户端 |
| **Nodemailer** | 邮件发送服务 |

### AI 集成技术

| 技术 | 说明 |
|------|------|
| **LangChain** | AI 应用开发框架 |
| **OpenAI SDK** | OpenAI API 客户端 |
| **OpenRouter** | 多模型聚合平台 |
| **字节火山引擎** | 国内大模型服务 |

### 架构亮点

#### 🏗️ 严格的分层设计

```
┌─────────────────────────────────┐
│      Client Layer (Vue 3)       │
│  Pages | Components | Stores    │
└────────────┬────────────────────┘
             │ HTTP/API Calls
┌────────────▼────────────────────┐
│      API Routes (Nitro)         │
│  验证输入 | 调用服务层           │
│  返回 ApiResponse<T>           │
└────────────┬────────────────────┘
             │ 业务逻辑
┌────────────▼────────────────────┐
│     Service Layer               │
│  业务逻辑 | 数据库事务           │
│  抛出异常（不捕获）             │
└────────────┬────────────────────┘
             │ 数据访问
┌────────────▼────────────────────┐
│  Database Layer (Drizzle ORM)   │
│  类型安全 | 迁移管理             │
└─────────────────────────────────┘
```

**分层职责清晰：**
- **API 层**：处理 HTTP 请求、验证输入、返回统一格式
- **服务层**：实现业务逻辑、协调组件、返回业务数据
- **数据层**：执行数据库操作、管理连接

#### 🔒 类型安全

- 前后端共享 TypeScript 类型定义
- Drizzle ORM 提供类型安全的数据库操作
- Zod 进行运行时数据验证
- 减少运行时错误，提升代码质量

#### 🚀 现代化开发体验

- 热重载开发
- 自动代码分割
- SSR/SSG 支持
- 优化的生产构建
- TypeScript 完整支持
- 前后端共有接口数据类型、参数验证

## 📦 快速开始

### 环境要求

- Node.js 18+
- MySQL 8.0+
- Redis（用于任务队列）
- PNPM 或 NPM

### 安装步骤

```bash
# 1. 克隆项目
git clone <repository-url>
cd fast-saas

# 2. 安装依赖
pnpm install

# 3. 配置环境变量
cp .env.example .env
# 编辑 .env 文件，填入数据库、支付、AI 等配置

# 4. 创建数据库
CREATE DATABASE IF NOT EXISTS fast_saas CHARACTER SET utf8mb4;

# 5. 生成数据库迁移脚本
pnpm db:generate

# 6. 运行数据库迁移
pnpm db:migrate

# 7. 启动开发服务器
pnpm dev
```

访问 http://localhost:3000 开始体验！

## 💡 常用命令

```bash
# 开发
pnpm dev              # 启动开发服务器
pnpm build            # 构建生产版本

# 数据库
pnpm db:generate      # 生成迁移文件
pnpm db:migrate       # 运行迁移

# 代码质量
pnpm lint             # 代码检查
pnpm typecheck        # 类型检查
```

## 🎓 适合人群

### ✅ 完美适合
- 熟悉 Vue.js 的前端开发者
- 了解基本 SQL 语法的开发者
- 想快速上线 AI 应用的创业者
- 需要完整 SaaS 基础设施的个人开发者


## 📞 联系方式

- **演示站点**：https://www.fast-saas.top/
- **使用fast-saas构建的应用**：https://www.ai-photos.art/

---

<div align="center">

**© 2025 Fast SaaS. All rights reserved.**

用 Fast SaaS，一小时上线您的 AI 应用！

</div>
