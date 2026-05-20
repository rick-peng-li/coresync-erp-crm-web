# CoreSync ERP/CRM

CoreSync 是一个基于现代技术栈构建的企业资源计划 (ERP) 和客户关系管理 (CRM) 系统。它旨在为中小企业提供一个功能齐全、易于定制和扩展的管理平台。

## 🌟 项目介绍

本项目基于 [IDURAR](https://github.com/idurar/idurar-erp-crm) 开源项目进行开发，集成了进销存、财务管理、客户管理、销售管理等核心业务功能。

### 核心功能
- **CRM 管理**: 线索 (Leads)、客户 (Clients)、联系人 (People) 管理。
- **销售管理**: 报价单 (Quotes)、优惠 (Offers)、订单 (Orders) 流程。
- **财务管理**: 发票 (Invoices)、支付 (Payments)、税收 (Taxes)、支出 (Expenses) 管理。
- **库存管理**: 产品 (Products)、品类管理。
- **自动化**: 自动生成 PDF 发票、邮件通知集成。
- **AI 集成**: 支持 OpenAI 接口（可选）。

## 🏗️ 系统架构

本项目采用前后端分离的架构：

### 后端 (Backend)
- **核心框架**: [Node.js](https://nodejs.org/) & [Express](https://expressjs.com/)
- **数据库**: [MongoDB](https://www.mongodb.com/) (使用 [Mongoose](https://mongoosejs.com/) 作为 ODM)
- **认证**: JSON Web Token (JWT) & Bcrypt 密码加密
- **模板引擎**: Pug (用于生成 PDF)
- **存储**: 支持本地存储及 AWS S3
- **代码组织**: 经典的 Controller-Model-Route 模式，并按功能模块 (app/core) 进行划分。

### 前端 (Frontend)
- **核心框架**: [React 18](https://reactjs.org/)
- **构建工具**: [Vite](https://vitejs.dev/)
- **UI 组件库**: [Ant Design (antd)](https://ant.design/) & [Ant Design Pro Components](https://procomponents.ant.design/)
- **状态管理**: [Redux Toolkit](https://redux-toolkit.js.org/)
- **路由**: [React Router 6](https://reactrouter.com/)

## 🚀 启动方式

### 环境要求
- **Node.js**: v20.9.0 或更高版本
- **npm**: v10.2.4 或更高版本
- **MongoDB**: 本地运行或云端实例 (MongoDB Atlas)

### 1. 后端配置与启动

进入后端目录：
```bash
cd backend
```

安装依赖：
```bash
npm install
```

配置环境变量：
复制 `.env` 模板并根据实际情况修改：
```bash
# 修改 DATABASE 链接、JWT_SECRET 等
```

初始化数据库（首次运行必做）：
```bash
npm run setup
```

启动开发服务器：
```bash
npm run dev
```

### 2. 前端配置与启动

进入前端目录：
```bash
cd frontend
```

安装依赖：
```bash
npm install
```

配置环境变量：
修改 `.env` 文件，确保 `VITE_BACKEND_SERVER` 指向正确的后端地址：
```env
VITE_BACKEND_SERVER="http://localhost:8888/api/"
```

启动开发服务器：
```bash
npm run dev
```

访问 `http://localhost:3000` (或 Vite 提示的其他端口) 即可开始使用。

## 📄 许可证

本项目遵循 [Fair-code License](https://faircode.io/)。
