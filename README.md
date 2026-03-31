# CampusHub

校园互助服务平台（CampusHub），面向校园场景提供统一的互助服务入口（如快递代取、学习辅导、二手交易）。

## 1. 项目简介 (Project Introduction)

- **项目名称**：校园互助服务平台 (CampusHub)
- **课程背景**：软件工程与计算 II
- **核心目标**：解决校园信息碎片化与匹配效率低的问题
- **项目周期**：10 周

## 2. 团队成员与角色 (Team Members & Roles)

- **团队名称**：`[请填写团队名称]`
- **成员 A**：郑智文 241880567（初始角色：需求负责人）
- **成员 B**：张苏楠 241880199（初始角色：架构负责人）
- **成员 C**：马宇航 241880054（初始角色：开发负责人）
- **成员 D**：李冠锦 241880129（初始角色：测试负责人）
- **角色轮换计划**：每个阶段更换主导角色，确保需求、架构、开发、测试能力轮转

## 3. 技术栈 (Technology Stack)

- **架构模式**：前后端分离
- **后端**：Spring Boot、JDK 17、Maven
- **前端**：Vue 3、Vite、Node.js 20+
- **数据库**：MySQL 8.x
- **AI 工具链**：GitHub Copilot、Gemini

## 4. Git 仓库与分支策略

首次初始化仓库可参考：

```powershell
git init
git add .
git commit -m "chore: initialize CampusHub infrastructure"
git branch -M main
git checkout -b dev
```

关联远程仓库（GitHub/GitLab/Gitee 任一）：

```powershell
git remote add origin <your-repo-url>
git push -u origin main
git push -u origin dev
```

- 默认分支：`main`
- 集成分支：`dev`
- 功能分支：`feature/<feature-name>`
- 紧急修复：`hotfix/<issue-name>`

详细规范见：`docs/git-branching-strategy.md`

## 5. CI 流水线

项目使用 GitHub Actions，配置文件：`.github/workflows/ci.yml`。

当前包含：
- 后端编译检查（Maven compile）
- 后端代码风格检查（Checkstyle）
- 前端构建检查（Vite build）
- 前端代码风格检查（Prettier check）

## 6. 项目结构

```text
CampusHub/
├─ backend/                # Spring Boot 后端
├─ frontend/               # Vue 前端
├─ docs/                   # 项目文档
└─ .github/workflows/      # CI 配置
```

完整目录说明见：`docs/project-structure.md`

## 7. 本地开发环境

开发环境配置说明见：`docs/development-setup.md`

### 快速启动

后端：

```powershell
cd backend
.\mvnw.cmd spring-boot:run
```

前端：

```powershell
cd frontend
npm install
npm run dev
```
