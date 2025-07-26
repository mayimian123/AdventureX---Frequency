# Hz 赫兹 - 社交网络平台 | Hz - Social Networking Platform
#AdventureX2025

一个专为年轻人（16-26岁）设计的现代社交网络平台，通过基于频率的匹配算法和Coffee Chat活动连接志同道合的人。

A modern social networking platform designed for young adults (16-26 years old) to connect with like-minded individuals through frequency-based matching algorithms and Coffee Chat activities.

## 🌟 功能特性 | Features

### 核心社交功能 | Core Social Features
- **Hz匹配算法** | **Hz Matching Algorithm**: 基于兴趣、位置、专业领域和互动潜力的兼容性评分连接用户 | Connect users based on compatibility scores using interests, location, professional fields, and interaction potential
- **实时聊天系统** | **Real-time Chat System**: 匹配用户之间的即时消息 | Instant messaging between matched users
- **用户资料管理** | **User Profile Management**: 包含头像上传、兴趣和个人信息的综合资料设置 | Comprehensive profile setup with avatar upload, interests, and personal information
- **Coffee Chat活动** | **Coffee Chat Activities**: 组织和参与线下聚会活动 | Organize and participate in offline meetup events

### 主要功能 | Key Functionality
- **着陆页面** | **Landing Page**: 具有动态频率波浪背景的现代设计 | Animated frequency-wave background with modern design
- **用户认证** | **User Authentication**: 基于邮箱的注册和登录系统 | Email-based registration and login system
- **资料设置** | **Profile Setup**: 带进度跟踪的分步资料完善 | Step-by-step profile completion with progress tracking
- **匹配系统** | **Matching System**: 浏览和发现具有Hz兼容性评分的用户 | Browse and discover users with Hz compatibility scores
- **活动管理** | **Activity Management**: 创建、加入和管理Coffee Chat活动 | Create, join, and manage Coffee Chat events
- **申请审核** | **Application Review**: 带问卷的增强审批系统 | Enhanced approval system with questionnaires
- **状态跟踪** | **Status Tracking**: 活动申请的实时更新 | Real-time updates on activity applications

## 🚀 技术栈 | Technology Stack

### 前端 | Frontend
- **React 18** 配合TypeScript | **React 18** with TypeScript
- **Vite** 构建工具 | **Vite** for build tooling
- **Tailwind CSS** 样式设计 | **Tailwind CSS** for styling
- **React Router** 页面导航 | **React Router** for navigation
- **自定义UI组件** 基于shadcn/ui | **Custom UI Components** with shadcn/ui base

### 后端 | Backend
- **Supabase** 数据库和认证 | **Supabase** for database and authentication
- **边缘函数** 无服务器API端点 | **Edge Functions** for serverless API endpoints
- **实时订阅** 支持实时聊天功能 | **Real-time subscriptions** for live chat features
- **PostgreSQL** 数据库和自定义架构 | **PostgreSQL** database with custom schemas

### 部署 | Deployment
- **MiniMax WebApps** 部署平台 | **MiniMax WebApps** deployment platform
- **自动化CI/CD** 构建优化 | **Automated CI/CD** with build optimization

## 📱 用户流程 | User Flow

1. **着陆页面** → 频率主题的欢迎体验 | **Landing Page** → Frequency-themed welcome experience
2. **用户注册** → 邮箱验证和账户创建 | **Registration** → Email verification and account creation  
3. **资料设置** → 完善个人信息和偏好 | **Profile Setup** → Complete personal information and preferences
4. **用户匹配** → 浏览具有Hz评分的兼容用户 | **Matching** → Browse compatible users with Hz scores
5. **实时聊天** → 与匹配用户的实时消息 | **Chat** → Real-time messaging with matched users
6. **Coffee Chat** → 创建/加入线下聚会活动 | **Coffee Chat** → Create/join offline meetup activities

## 🎨 设计系统 | Design System

### 视觉识别 | Visual Identity
- **主要颜色** | **Primary Colors**: 灰度色（黑、白、灰）配合浅蓝色点缀 (#64B5F6) | Grayscale (black, white, gray) with light blue accents (#64B5F6)
- **字体设计** | **Typography**: 简洁、极简字体，充足留白 | Clean, minimal fonts with ample whitespace
- **动画效果** | **Animations**: 频率波浪图案和Hz振动效果 | Frequency wave patterns and Hz vibration effects
- **图标设计** | **Icons**: 整个界面采用波形图标体系 | Wave-based iconography throughout the interface

### UI设计原则 | UI Principles
- 极简主义设计理念 | Minimalist design philosophy
- 频率/声波视觉隐喻 | Frequency/sound wave visual metaphors
- 一致的浅蓝色强调色 | Consistent light blue accent color
- 移动端响应式布局 | Mobile-responsive layouts

## 🛠️ 安装与设置 | Installation & Setup

### 前置要求 | Prerequisites
- Node.js 18+ 
- npm 或 pnpm 包管理器 | npm or pnpm package manager
- Supabase 账户和项目 | Supabase account and project

### 本地开发 | Local Development

1. **克隆仓库** | **Clone the repository**
```bash
git clone [repository-url]
cd hz-social
```

2. **安装依赖** | **Install dependencies**
```bash
npm install
# 或者 | or
pnpm install
```

3. **环境配置** | **Environment Configuration**
创建 `.env.local` 文件 | Create `.env.local` file:
```env
VITE_SUPABASE_URL=your_supabase_project_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
```

4. **数据库设置** | **Database Setup**
应用 `/supabase/tables/` 中的SQL架构 | Apply the SQL schemas from `/supabase/tables/`:
- `hz_users.sql` - 用户资料 | User profiles
- `hz_matches.sql` - 用户兼容性数据 | User compatibility data
- `hz_conversations.sql` - 聊天会话 | Chat conversations
- `hz_messages.sql` - 聊天消息 | Chat messages
- `hz_coffee_chat_activities.sql` - 活动事件 | Event activities
- `hz_activity_participants.sql` - 活动参与 | Event participation

5. **部署边缘函数** | **Deploy Edge Functions**
从 `/supabase/functions/` 部署无服务器函数 | Deploy serverless functions from `/supabase/functions/`:
```bash
supabase functions deploy hz-match-users
supabase functions deploy hz-coffee-chat-management
supabase functions deploy hz-send-message
supabase functions deploy hz-upload-avatar
```

6. **启动开发服务器** | **Start Development Server**
```bash
npm run dev
```

## 📊 数据库架构 | Database Schema

### 核心表格 | Core Tables
- **hz_users**: 用户资料和偏好 | User profiles and preferences
- **hz_matches**: 用户间兼容性评分 | Compatibility scores between users
- **hz_conversations**: 聊天会话元数据 | Chat conversation metadata
- **hz_messages**: 单条聊天消息 | Individual chat messages
- **hz_coffee_chat_activities**: 活动列表 | Event listings
- **hz_activity_participants**: 活动参与和申请 | Event participation and applications

### 关键关系 | Key Relationships
- 用户 ↔ 匹配（多对多含评分）| Users ↔ Matches (many-to-many with scores)
- 用户 ↔ 会话（通过消息多对多）| Users ↔ Conversations (many-to-many through messages)
- 用户 ↔ 活动（通过参与者多对多）| Users ↔ Activities (many-to-many through participants)

## 🔌 API端点 | API Endpoints

### 边缘函数 | Edge Functions
- `POST /hz-match-users` - 计算用户兼容性 | Calculate user compatibility
- `POST /hz-coffee-chat-management` - 管理活动和申请 | Manage events and applications
- `POST /hz-send-message` - 发送实时消息 | Send real-time messages
- `POST /hz-upload-avatar` - 处理头像上传 | Handle avatar uploads

### 关键操作 | Key Operations
- Hz算法用户匹配 | User matching with Hz algorithm
- 实时聊天消息传递 | Real-time chat message delivery
- 活动创建和管理 | Activity creation and management
- 申请审批工作流 | Application approval workflow
- 自动通知系统 | Automatic notification system

## 📁 项目结构 | Project Structure

```
hz-social/
├── src/
│   ├── components/          # 可复用UI组件 | Reusable UI components
│   ├── pages/              # 基于路由的页面组件 | Route-based page components
│   │   ├── app/            # 认证应用页面 | Authenticated app pages
│   │   ├── LandingPage.tsx # 公共着陆页面 | Public landing page
│   │   └── LoginPage.tsx   # 认证页面 | Authentication pages
│   ├── lib/                # 工具库 | Utility libraries
│   ├── hooks/              # 自定义React hooks | Custom React hooks
│   ├── types/              # TypeScript类型定义 | TypeScript definitions
│   └── contexts/           # React上下文提供者 | React context providers
├── supabase/
│   ├── tables/             # 数据库架构文件 | Database schema files
│   ├── functions/          # 边缘函数实现 | Edge function implementations
│   └── migrations/         # 数据库迁移 | Database migrations
├── public/
│   └── avatars/           # 测试用户头像 | Test user avatars
└── data/                  # 测试数据文件 | Test data files
```

## 🌐 部署 | Deployment

### URL
- **线上网站** | **Live Website**: https://z5jjfd52lycb.space.minimax.io/ 

### 构建过程 | Build Process
```bash
npm run build
npm run preview  # 本地生产环境预览 | Local production preview
```

## 📈 功能详解 | Features in Detail

### Hz匹配算法 | Hz Matching Algorithm
- **兴趣重叠** | **Interest Overlap**: 基于共同标签的40%权重 | 40% weight based on shared tags
- **位置邻近** | **Location Proximity**: 20%权重（同城市/省份/国家）| 20% weight (same city/province/country)
- **专业对齐** | **Professional Alignment**: 相关领域20%权重 | 20% weight on related fields
- **互动潜力** | **Interaction Potential**: 来自资料分析的20%权重 | 20% weight from profile analysis

### Coffee Chat系统 | Coffee Chat System
- **增强申请** | **Enhanced Applications**: 基于问卷的申请 | Questionnaire-based applications
- **审批工作流** | **Approval Workflow**: 组织者审核与参与者详情 | Organizer review with participant details
- **自动通知** | **Automatic Notifications**: 基于聊天的状态更新 | Chat-based status updates
- **活动生命周期** | **Activity Lifecycle**: 从创建到完成的跟踪 | From creation to completion tracking

### 实时功能 | Real-time Features
- **实时聊天** | **Live Chat**: 即时消息传递和已读回执 | Instant message delivery and read receipts
- **状态更新** | **Status Updates**: 实时申请状态变更 | Real-time application status changes
- **活动通知** | **Activity Notifications**: 自动化活动相关消息 | Automatic event-related messaging

## 🔧 配置 | Configuration

### 环境变量 | Environment Variables
- `VITE_SUPABASE_URL`: Supabase项目URL | Supabase project URL
- `VITE_SUPABASE_ANON_KEY`: Supabase公钥 | Public Supabase key
- 边缘函数的额外Supabase配置 | Additional Supabase configuration for Edge Functions

### 定制选项 | Customization Options
- 匹配算法权重可在边缘函数中调整 | Matching algorithm weights can be adjusted in Edge Functions
- UI主题和颜色可在Tailwind配置中设置 | UI themes and colors configurable in Tailwind config
- 聊天消息模板可在通知函数中自定义 | Chat message templates customizable in notification functions

## 🤝 贡献 | Contributing

### 开发指南 | Development Guidelines
1. 遵循TypeScript最佳实践 | Follow TypeScript best practices
2. 保持一致的组件结构 | Maintain consistent component structure
3. 使用Tailwind CSS进行样式设计 | Use Tailwind CSS for styling
4. 部署前彻底测试功能 | Test features thoroughly before deployment

### 代码风格 | Code Style
- ESLint配置确保代码质量 | ESLint configuration for code quality
- Prettier保持一致格式 | Prettier for consistent formatting
- 启用TypeScript严格模式 | TypeScript strict mode enabled
