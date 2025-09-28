# School Web 项目文件结构

## 项目概述
这是一个基于RuoYi-Vue-Plus框架的学校管理系统，包含732个核心源代码文件。

## 主要模块结构

### 1. ruoyi-admin（管理后台模块）
- **主要功能**: Web服务入口，系统启动类
- **关键文件**:
  - `DromaraApplication.java` - Spring Boot启动类
  - `src/main/java/org/dromara/web/controller/` - 控制器层
    - `AuthController.java` - 认证控制器
    - `CaptchaController.java` - 验证码控制器
    - `IndexController.java` - 首页控制器
  - `src/main/java/org/dromara/web/service/` - 服务层
    - `SysLoginService.java` - 登录服务
    - `SysRegisterService.java` - 注册服务
  - `src/main/resources/` - 配置文件
    - `application.yml` - 主配置文件
    - `application-dev.yml` - 开发环境配置
    - `application-prod.yml` - 生产环境配置

### 2. ruoyi-common（通用模块）
包含25个子模块，提供各种通用功能：

#### 核心模块
- **ruoyi-common-core**: 核心工具类和基础组件
- **ruoyi-common-web**: Web相关工具和配置
- **ruoyi-common-mybatis**: MyBatis增强和配置

#### 安全和认证
- **ruoyi-common-security**: 安全配置
- **ruoyi-common-satoken**: Sa-Token权限框架集成
- **ruoyi-common-encrypt**: 数据加密模块
- **ruoyi-common-sensitive**: 数据脱敏模块

#### 数据存储
- **ruoyi-common-redis**: Redis缓存工具
- **ruoyi-common-oss**: 对象存储服务
- **ruoyi-common-excel**: Excel导入导出

#### 通信和消息
- **ruoyi-common-mail**: 邮件服务
- **ruoyi-common-sms**: 短信服务
- **ruoyi-common-websocket**: WebSocket支持
- **ruoyi-common-sse**: Server-Sent Events

#### 其他功能模块
- **ruoyi-common-json**: JSON处理
- **ruoyi-common-log**: 日志记录
- **ruoyi-common-doc**: 接口文档
- **ruoyi-common-translation**: 数据翻译
- **ruoyi-common-tenant**: 多租户支持
- **ruoyi-common-ratelimiter**: 限流组件
- **ruoyi-common-idempotent**: 幂等性处理
- **ruoyi-common-job**: 定时任务
- **ruoyi-common-social**: 第三方登录

### 3. ruoyi-modules（业务模块）

#### ruoyi-system（系统管理模块）
- **用户管理**: 用户信息维护、角色分配
- **部门管理**: 组织架构管理  
- **菜单管理**: 动态菜单配置
- **角色管理**: 角色权限分配
- **字典管理**: 系统字典维护
- **参数管理**: 系统参数配置
- **通知公告**: 系统公告管理
- **操作日志**: 系统操作记录
- **登录日志**: 用户登录记录

#### ruoyi-workflow（工作流模块）
- **流程定义**: 工作流流程设计
- **流程实例**: 流程实例管理
- **任务管理**: 工作流任务处理
- **流程监控**: 流程执行监控

#### ruoyi-generator（代码生成模块）
- **表管理**: 数据库表管理
- **代码生成**: 自动生成CRUD代码
- **模板管理**: 代码生成模板

#### ruoyi-job（定时任务模块）
- **任务管理**: 定时任务配置
- **任务日志**: 任务执行记录
- **执行器管理**: 任务执行器配置

#### ruoyi-demo（演示模块）
- **功能演示**: 框架功能使用示例
- **测试用例**: 各种测试案例

### 4. ruoyi-extend（扩展模块）
- **ruoyi-monitor-admin**: 系统监控管理
- **ruoyi-snailjob-server**: 分布式任务调度服务

### 5. script（脚本目录）
- **sql/**: 数据库脚本
  - `ry_vue_5.X.sql` - 主数据库脚本
  - `ry_job.sql` - 定时任务脚本
  - `ry_workflow.sql` - 工作流脚本
  - `update/` - 数据库升级脚本
- **docker/**: Docker部署脚本
- **bin/**: 启动脚本

## 技术特性

### 后端技术栈
- **框架**: Spring Boot 3.5.6
- **语言**: Java 17/21
- **权限**: Sa-Token + JWT
- **ORM**: MyBatis-Plus 3.5.14
- **数据库**: MySQL 8.0+ (支持Oracle、PostgreSQL、SQL Server)
- **缓存**: Redis 7.0+ + Redisson
- **消息队列**: Redis Stream
- **任务调度**: SnailJob
- **工作流**: Warm-Flow
- **监控**: Spring Boot Admin
- **文档**: SpringDoc + OpenAPI 3.0

### 核心功能特性
- ✅ 多租户支持
- ✅ 数据权限控制
- ✅ 数据加密脱敏
- ✅ 接口限流防刷
- ✅ 分布式锁
- ✅ 幂等性处理
- ✅ 国际化支持
- ✅ 代码生成器
- ✅ 在线用户管理
- ✅ 系统性能监控

## 文件统计
- 总文件数: 796
- Java源码文件: ~600+
- 配置文件: ~100+
- SQL脚本: ~30+
- 其他文件: ~60+

## 部署方式
1. **传统部署**: JAR包部署
2. **Docker部署**: 容器化部署
3. **K8s部署**: Kubernetes集群部署

## 开发环境要求
- JDK 17或21
- Maven 3.6+
- MySQL 8.0+
- Redis 7.0+
- Node.js 16+ (前端开发)

---

*注: 由于项目文件较多，当前仅上传了主要的配置文件和结构说明。完整源代码已在本地Git仓库中管理。*