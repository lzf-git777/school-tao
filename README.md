# 校趣淘校园二手交易系统
[![GitHub license](https://img.shields.io/github/license/your-username/campus-secondhand-system)](https://github.com/your-username/campus-secondhand-system)

> 专为高校学生设计的二手交易平台，支持商品发布、分类筛选、在线聊天、订单跟踪，解决校园闲置物品处理难题。

## 核心特性
*   特性 1：商品分类管理（按书籍、电子产品、生活用品等校园常见类别划分）
*   特性 2：学生身份认证（绑定校园邮箱，确保交易双方为在校学生）
*   特性 3：在线即时沟通（内置聊天功能，支持买卖双方协商价格、自提地点）
*   特性 4：订单状态跟踪（待付款、待自提、已完成、售后等状态可视化）

## 快速开始
### 先决条件
*   前端：Node.js 16+（Vue 3 依赖）、npm 8+
*   后端：JDK 17+、Maven 3.8+
*   数据库：MySQL 8.0（需提前创建数据库 `campus_secondhand_db`）
*   工具：Git、Postman（接口测试）、Docker（可选，部署用）

### 安装与运行
#### 后端启动（Spring Boot）
1.  `git clone https://github.com/your-username/campus-secondhand-system.git`
2.  `cd campus-secondhand-system/backend`（假设后端代码放在 backend 目录）
3.  修改 `src/main/resources/application.yml` 中的数据库连接（用户名、密码替换为本地配置）
4.  `mvn clean install`（构建项目）
5.  `java -jar target/campus-secondhand-0.0.1-SNAPSHOT.jar`（启动后端服务，默认端口 8080）

#### 前端启动（Vue）
1.  新开终端，进入前端目录：`cd campus-secondhand-system/frontend`
2.  `npm install`（安装依赖，若速度慢可配置淘宝镜像：`npm config set registry https://registry.npm.taobao.org`）
3.  `npm run dev`（启动前端服务，默认端口 5173）
4.  浏览器访问 `http://localhost:5173`，即可进入系统首页

## 项目结构
├── backend/       # 后端Spring Boot代码（用户、商品、订单模块）
├── frontend/      # 前端Vue代码（页面、组件、接口请求）
├── docs/          # 项目详细文档（架构、开发指南等）
├── sql/           # 数据库初始化脚本（创建表、测试数据）
├── README.md      # 项目自述（当前文件）
└── LICENSE        # 许可证文件

## 如何贡献
我们欢迎校园开发者贡献功能！请阅读我们的 [贡献指南](CONTRIBUTING.md)（如新增“校园自提点管理”模块）。

## 许可证
本项目基于 [MIT](LICENSE) 许可证开源，供高校学习使用。

## 获取帮助
*   [提交 Issue](https://github.com/your-username/campus-secondhand-system/issues) - 报告Bug（如“商品发布后图片不显示”）或提出新特性（如“新增二手书籍ISBN查询”）
*   沟通群：QQ群 12345678（校园开发者交流群）
