# 校趣淘后端设计文档
## 1. 模块划分
按校园二手交易流程，后端分为4个核心模块：
- 用户模块（user）：校园邮箱注册、登录、身份认证、个人信息管理
- 商品模块（goods）：商品发布、分类、搜索、收藏、图片上传
- 订单模块（order）：订单创建、状态更新（待付款→待自提→已完成）、订单查询
- 沟通模块（chat）：买卖双方即时消息、消息记录存储（基于WebSocket）

## 2. 技术栈
- 核心框架：Spring Boot 3.2.0
- ORM框架：MyBatis-Plus 3.5.5（简化数据库操作）
- 数据库：MySQL 8.0（存储结构化数据）
- 缓存：Redis 7.0（缓存热门商品列表，减少数据库查询）
- 图片存储：本地存储（开发环境）/ 阿里云OSS（生产环境，存储商品图片）
- 认证：JWT（生成登录令牌，避免session共享问题）

## 3. 数据库设计（核心表）
- `user`（用户表）：id（主键）、username（用户名）、email（校园邮箱，唯一）、password（加密存储）、avatar（头像）、create_time（注册时间）
- `goods`（商品表）：id、title（商品标题）、category_id（分类ID，关联category表）、price（价格）、status（状态：0-待审核，1-在售，2-已卖出）、user_id（发布者ID，关联user表）、create_time
- `order`（订单表）：id、order_no（订单编号）、goods_id（商品ID）、buyer_id（买家ID）、seller_id（卖家ID）、status（订单状态）、meet_place（自提地点）、create_time
- `category`（商品分类表）：id、name（分类名：书籍、电子产品、生活用品、体育器材等）
