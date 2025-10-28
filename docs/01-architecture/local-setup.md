# 校趣淘本地开发环境搭建指南
## 1. 后端环境搭建（Spring Boot）
### 1.1 前置条件
- 安装JDK 17（验证：`java -version` 显示 17.x.x）
- 安装Maven 3.8（验证：`mvn -v` 显示 3.8.x）
- 安装MySQL 8.0，创建数据库 `campus_secondhand_db`（SQL脚本在项目 `/sql/init_db.sql`）

### 1.2 步骤
1.  克隆仓库：`git clone https://github.com/your-username/campus-secondhand-system.git`
2.  导入数据库：打开MySQL客户端（如Navicat），执行 `/sql/init_db.sql`，创建表和测试数据（含1个测试用户：test@xxx.edu.cn，密码123456）
3.  配置数据库连接：打开 `backend/src/main/resources/application.yml`，修改以下内容：
    ```yaml
    spring:
      datasource:
        url: jdbc:mysql://localhost:3306/campus_secondhand_db?useSSL=false&serverTimezone=UTC
        username: 你的MySQL用户名（如root）
        password: 你的MySQL密码（如123456）
