# CampusHub

## 1. 项目简介 (Project Introduction)

- **项目名称**：校园互助服务平台 (CampusHub)
- **课程背景**：软件工程与计算 II
- **核心目标**：旨在解决校园内信息碎片化、匹配效率低的问题，提供统一的互助平台（如快递代取、学习辅导、二手交易等）
- **项目周期**：10 周

## 2. 团队成员与角色 (Team Members & Roles)

- **团队名称**：
- **成员 A**：郑智文 241880567
- **成员 B**：张苏楠 241880199
- **成员 C**：马宇航 241880054
- **成员 D**：李冠锦 241880129

## 3. 技术栈 (Technology Stack)

- **架构模式**：前后端分离架构
- **后端**：Spring Boot 3, JDK 17, Maven
- **前端**：Vue 3, Node.js 20.x
- **数据库**：MySQL 8.x
- **AI 工具链**：
    - **AI编程助手**：GitHub Copilot
    - **AI对话工具**：Gemini
- **AI 工具链**：GitHub Copilot、Gemini

## 4. 仓库结构 (Repository Structure)

```text
CampusHub/
|- backend/                 # Spring Boot 后端
|- frontend/                # Vue 前端（当前为基础目录）
|- docs/                    # 课程文档与规范
|  |- P0/
|  |- branch-strategy.md
|  `- development-setup.md
|- .github/workflows/       # CI 配置
|- .gitignore
`- README.md
```

## 5. 分支策略 (Branching Strategy)

采用 `main + dev + feature/*` 模型：

- `main`：稳定可发布代码
- `dev`：日常集成分支
- `feature/*`：功能开发分支（示例：`feature/user-login`）

详细规范见 `docs/branch-strategy.md`。

## 6. CI 流水线 (Continuous Integration)

项目已配置 GitHub Actions（见 `.github/workflows/ci.yml`），默认在 `main`、`dev` 及 `feature/*` 的 Push/PR 时触发：

- 后端编译与测试检查（Maven）
- 后端代码风格检查（Checkstyle）

## 7. 本地开发快速开始 (Quick Start)

### 后端

```powershell
Set-Location .\backend
.\mvnw.cmd clean verify
```

### 前端

前端目录当前为初始化结构，待补充 `package.json` 后可接入 lint/test/build 流程。

## 8. 开发环境说明文档

详细环境安装、配置与常用命令见 `docs/development-setup.md`。
