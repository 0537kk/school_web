# School Web 管理系统

## 项目简介

这是一个基于若依框架(RuoYi-Vue-Plus)开发的学校管理系统，采用现代化的微服务架构，支持多租户和分布式部署。

## 技术栈

### 后端技术
- **框架**: Spring Boot 3.5.6
- **语言**: Java 17/21  
- **权限认证**: Sa-Token + JWT
- **ORM框架**: MyBatis-Plus
- **数据库**: MySQL、Redis
- **缓存**: Redisson
- **文档**: SpringDoc + OpenAPI 3.0
- **任务调度**: SnailJob
- **工作流**: Warm-Flow

### 主要特性
- 🚀 基于Spring Boot 3.x，支持Java 17/21
- 🔐 完善的权限管理和多租户支持  
- 📱 前后端分离，支持多种前端框架
- 🌐 支持多数据源和分布式事务
- 📊 内置代码生成器，快速开发CRUD
- 🛡️ 数据加密、脱敏、权限控制
- 📈 系统监控和链路追踪
- 🔄 工作流引擎支持复杂业务流程

## 系统功能

### 系统管理
- 用户管理：用户信息维护、角色分配
- 部门管理：组织架构管理
- 岗位管理：职务管理
- 菜单管理：动态菜单配置
- 角色管理：角色权限分配
- 字典管理：系统字典维护
- 参数管理：系统参数配置

### 系统监控  
- 在线用户：实时在线用户监控
- 定时任务：任务调度管理
- 数据监控：数据库监控
- 服务监控：系统性能监控
- 缓存监控：Redis缓存监控

### 系统工具
- 代码生成：一键生成完整CRUD代码
- 系统接口：Swagger接口文档
- 文件管理：文件上传下载管理

## 项目结构

```
school_web/
├── ruoyi-admin/           # 管理后台模块
├── ruoyi-common/          # 通用工具模块
│   ├── ruoyi-common-core/     # 核心工具类
│   ├── ruoyi-common-web/      # Web相关工具
│   ├── ruoyi-common-redis/    # Redis工具
│   ├── ruoyi-common-mybatis/  # MyBatis工具
│   └── ...
├── ruoyi-modules/         # 业务模块
│   ├── ruoyi-system/          # 系统管理模块
│   ├── ruoyi-generator/       # 代码生成模块  
│   ├── ruoyi-workflow/        # 工作流模块
│   └── ruoyi-demo/           # 示例模块
├── ruoyi-extend/          # 扩展模块
└── script/               # 脚本文件
    ├── sql/                  # 数据库脚本
    └── docker/              # Docker配置
```

## 快速开始

### 环境要求
- JDK 17+
- MySQL 8.0+
- Redis 7.0+
- Maven 3.6+

### 数据库配置
1. 创建数据库 `ry-vue-plus`
2. 执行脚本 `script/sql/ry_vue_5.X.sql`

### 运行项目
```bash
# 克隆项目
git clone https://github.com/0537kk/school_web.git

# 进入项目目录
cd school_web

# 编译项目
mvn clean compile

# 运行项目
mvn spring-boot:run -pl ruoyi-admin
```

### 访问地址
- 后端接口：http://localhost:8080
- 接口文档：http://localhost:8080/doc.html

## 部署说明

### Docker部署
```bash
# 构建镜像
docker build -t school_web .

# 运行容器
docker run -d -p 8080:8080 school_web
```

### Docker Compose部署
```bash
cd script/docker
docker-compose up -d
```

## 配置说明

主要配置文件：
- `application.yml` - 主配置文件
- `application-dev.yml` - 开发环境配置  
- `application-prod.yml` - 生产环境配置

## 开发指南

### 代码生成
1. 设计数据库表结构
2. 使用代码生成器生成基础CRUD代码
3. 根据业务需求调整和扩展功能

### 多租户使用
系统支持多租户模式，可通过租户管理功能：
- 创建租户
- 分配租户套餐
- 管理租户用户

## 许可证

本项目遵循 MIT 开源协议

## 联系方式

如有问题，请通过以下方式联系：
- 提交 Issue
- 发送邮件

## 鸣谢

感谢以下开源项目：
- [RuoYi-Vue-Plus](https://gitee.com/dromara/RuoYi-Vue-Plus)
- [Spring Boot](https://spring.io/projects/spring-boot)
- [MyBatis-Plus](https://baomidou.com/)
- [Sa-Token](https://sa-token.dev33.cn/)