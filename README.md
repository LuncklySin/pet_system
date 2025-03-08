Pet System - 宠物领养系统 -- 更多微信：jackSinWu

项目介绍

宠物领养系统是一个集 宠物领养、寄养、丢失宠物查找、丢失主人寻回 于一体的平台，旨在帮助宠物找到合适的主人，同时提供宠物相关的交流与服务。

![image](https://github.com/user-attachments/assets/8f5213ac-ab5e-4bc5-8214-04e836063d74)


技术栈

前端：Vue.js + Vuex

后端：Spring Boot + MyBatis + Shiro + Netty

数据库：MySQL

存储：MinIO（对象存储服务）

核心功能

宠物管理：

浏览宠物信息（图片、特征、年龄、健康状况等）

发布宠物领养信息

申请领养宠物，提交审核

寄养管理：

提交寄养申请

管理寄养记录

丢失宠物查找：

发布丢失宠物信息

认领宠物

用户管理：

账号注册、登录、权限管理（Shiro）

用户实名认证

个人资料管理

聊天系统（Netty 实现）：

领养者和发布者之间的即时聊天

消息记录存储

存储管理（MinIO）：

上传宠物照片、用户头像等

文件管理

项目部署

1. 环境要求

JDK 11+

Node.js 16+

MySQL 8+

MinIO 服务器

2. 后端启动

# 进入后端项目目录
cd backend

# 编译打包
mvn clean package

# 运行 Spring Boot
java -jar target/pet-system.jar

3. 前端启动

# 进入前端项目目录
cd frontend

# 安装依赖
npm install

# 启动前端项目
npm run serve

4. MinIO 配置

启动 MinIO 服务器：

minio server /data --console-address ":9001"

访问 MinIO 控制台：http://localhost:9001

配置 Access Key 和 Secret Key，并在后端 application.yml 配置 MinIO 连接信息。

目录结构

pet-system/
├── backend/        # 后端 Spring Boot
│   ├── src/main/   # Java 代码
│   ├── resources/  # 配置文件
│   ├── pom.xml     # Maven 配置
│   └── ...
├── frontend/       # 前端 Vue 项目
│   ├── src/        # Vue 代码
│   ├── public/     # 静态资源
│   ├── package.json# 依赖管理
│   └── ...
├── docs/           # 项目文档
├── README.md       # 项目说明
└── ...

贡献指南

如果你想参与贡献代码，请遵循以下步骤：

Fork 本仓库

创建新分支 (git checkout -b feature-xxx)

提交代码 (git commit -m '添加新功能 xxx')

推送分支 (git push origin feature-xxx)

提交 Pull Request

许可证

本项目基于 MIT License 进行开源。
