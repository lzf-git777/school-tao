# 校趣淘项目贡献指南
欢迎各位同学参与校园二手交易系统的开发，以下是贡献规范：

## 1. 开发工作流
采用 **GitHub Flow**（适配学生开发节奏，流程简洁）：
1. 从 `main` 分支创建功能分支（例如开发“商品收藏”“自提点管理”等校园特色功能）
2. 在分支上完成开发，提交代码并推送至远程仓库
3. 在GitHub上发起 Pull Request（PR），详细描述功能细节
4. 审核通过后，合并到 `main` 分支，删除功能分支

## 2. 分支命名规范
严格按以下格式命名，便于识别功能类型：
- 新功能：`feat/模块-具体功能`（如 `feat/goods-collect` 表示“商品收藏功能”）
- Bug修复：`fix/模块-问题描述`（如 `fix/order-status-display` 表示“修复订单状态显示错误”）
- 文档更新：`docs/文档类型`（如 `docs/update-api` 表示“更新API文档”）
- 测试代码：`test/模块`（如 `test/user-login` 表示“添加用户登录测试”）

## 3. Pull Request（PR）模板
提交PR时需包含以下信息，方便审核：
- 关联Issue：若有相关Issue，注明编号（如“Fix #12，修复商品详情页加载慢”）
- 功能描述：简要说明实现的功能（如“实现商品收藏功能，用户可点击收藏按钮添加/取消收藏”）
- 测试情况：测试的场景（如“测试了收藏/取消收藏、收藏列表展示、未登录收藏提示”）
- 截图：关键页面截图（如商品收藏按钮状态、收藏列表页面）

## 4. 代码风格规范
- 后端（Spring Boot）：遵循阿里巴巴Java开发手册，类名使用大驼峰，方法名、变量名使用小驼峰
- 前端（Vue）：组件名使用大驼峰，变量名使用小驼峰，注释清晰（如`// 商品收藏按钮点击事件`）

## 5. 如何提交代码
1. 克隆仓库：`git clone https://github.com/lzf-git777/school-tao.git`
2. 创建分支：`git checkout -b feat/your-feature`（替换为你的功能分支名）
3. 提交代码：`git add . && git commit -m "feat: 你的功能描述"`
4. 推送分支：`git push origin feat/your-feature`
5. 发起PR：在GitHub仓库页面点击“New pull request”，选择目标分支为`main`
