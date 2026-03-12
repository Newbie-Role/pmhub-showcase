# PmHub - 项目智控平台

## 项目概述

PmHub是一个基于Java开发的项目管理平台，旨在为团队提供一站式的项目管理解决方案。采用微服务架构设计，具有良好的扩展性和可维护性。

通过PMHub，团队可以实现项目的全生命周期管理，包括任务分配、进度跟踪、文档管理等功能，提高团队协作效率。

## 核心功能

### 1. 项目管理
- 创建、管理和跟踪项目进度
- 支持项目状态更新和里程碑设置
- 项目分类和标签管理
- 项目成员管理和权限控制

### 2. 任务分配
- 将任务分配给团队成员
- 设置任务截止日期和优先级
- 跟踪任务完成情况
- 任务依赖关系管理

### 3. 文档管理
- 集中存储和管理项目文档
- 支持版本控制和权限管理
- 文档分类和搜索功能
- 支持多种文档格式

### 4. 团队协作
- 提供团队沟通工具
- 支持评论、通知和实时更新
- 团队活动记录和历史查看
- 集成第三方协作工具

### 5. 数据分析
- 生成项目报表和数据分析
- 可视化项目进度和团队绩效
- 自定义报表和仪表盘
- 数据导出功能

### 6. 安全认证
- 基于角色的权限控制
- 确保数据安全和访问控制
- 登录日志和操作审计
- 支持多种认证方式

## 技术栈

### 后端技术
- **Java 1.8+**：主要开发语言
- **Spring Boot**：应用框架
- **Spring Cloud**：微服务架构
- **Spring Security**：安全认证
- **MyBatis**：ORM框架
- **MySQL**：关系型数据库
- **Redis**：缓存
- **RabbitMQ**：消息队列

### 前端技术
- **Vue.js**：前端框架
- **Element UI**：UI组件库
- **Axios**：HTTP客户端
- **ECharts**：数据可视化
- **Vue Router**：路由管理
- **Vuex**：状态管理

### 部署技术
- **Docker**：容器化部署
- **Kubernetes**：容器编排
- **Jenkins**：持续集成/持续部署
- **Nginx**：反向代理

## 系统架构

PmHub采用微服务架构，主要包含以下模块：

1. **pmhub-api**：API网关，处理所有请求
2. **pmhub-auth**：认证服务，处理用户登录和权限
3. **pmhub-base**：基础服务，提供公共功能
4. **pmhub-boot**：启动服务，负责服务注册和发现
5. **pmhub-gateway**：网关服务，路由请求
6. **pmhub-modules**：业务模块，包含核心业务逻辑
7. **pmhub-monitor**：监控服务，监控系统运行状态
8. **pmhub-ui**：前端界面

## 快速开始

### 环境要求
- JDK 1.8+
- Maven 3.6+
- MySQL 5.7+
- Redis 5.0+
- Node.js 14.0+ (前端开发)

### 安装步骤

1. **克隆仓库**
   ```bash
   git clone https://github.com/Newbie-Role/pmhub.git
   cd pmhub
   ```

2. **配置数据库**
   - 创建数据库：`CREATE DATABASE pmhub CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
   - 导入数据库脚本：`mysql -u root -p pmhub < sql/pmhub.sql`

3. **配置环境变量**
   - 修改 `application.yml` 文件中的数据库连接信息
   - 修改 Redis 连接信息

4. **构建项目**
   ```bash
   mvn clean install
   ```

5. **启动服务**
   ```bash
   # 启动注册中心
   cd pmhub-boot
   mvn spring-boot:run
   
   # 启动认证服务
   cd ../pmhub-auth
   mvn spring-boot:run
   
   # 启动其他服务...
   ```

6. **启动前端**
   ```bash
   cd pmhub-ui
   npm install
   npm run dev
   ```

7. **访问系统**
   - 后端API：http://localhost:8080
   - 前端界面：http://localhost:8081

## 使用指南

### 1. 用户注册和登录
- 访问系统首页，点击"注册"按钮
- 填写注册信息，完成注册
- 使用注册的账号登录系统

### 2. 创建项目
- 登录系统后，点击"创建项目"
- 填写项目名称、描述、起止时间等信息
- 选择项目成员和权限
- 点击"创建"按钮

### 3. 分配任务
- 进入项目详情页，点击"任务管理"
- 点击"创建任务"
- 填写任务名称、描述、截止日期、优先级等信息
- 选择任务负责人
- 点击"保存"按钮

### 4. 上传文档
- 进入项目详情页，点击"文档管理"
- 点击"上传文档"
- 选择要上传的文件
- 填写文档名称和描述
- 点击"上传"按钮

### 5. 查看报表
- 进入项目详情页，点击"数据分析"
- 选择报表类型和时间范围
- 查看生成的报表
- 可选择导出报表

## 贡献指南

欢迎为PMHub项目做出贡献！以下是贡献的基本步骤：

1. **Fork 仓库**
   - 访问 [https://github.com/Newbie-Role/pmhub](https://github.com/Newbie-Role/pmhub)
   - 点击"Fork"按钮，将仓库复制到个人账号

2. **克隆仓库**
   ```bash
   git clone https://github.com/Newbie-Role/pmhub.git
   cd pmhub
   ```

3. **创建分支**
   ```bash
   git checkout -b feature/your-feature
   ```

4. **修改代码**
   - 实现新功能或修复bug
   - 确保代码符合项目的编码规范
   - 编写测试用例

5. **提交代码**
   ```bash
   git add .
   git commit -m "Add your feature"
   ```

6. **推送到远程仓库**
   ```bash
   git push origin feature/your-feature
   ```

7. **创建 Pull Request**
   - 访问 GitHub 上的个人仓库
   - 点击"Compare & pull request"
   - 填写 PR 标题和描述
   - 点击"Create pull request"

---

感谢您使用 PmHub-项目智控平台！

