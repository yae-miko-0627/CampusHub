# Development Setup

本文档用于统一 CampusHub 团队开发环境。

## 1. Required Tools

- JDK 17
- Maven（推荐使用仓库内 Maven Wrapper）
- Node.js 20+
- npm 10+
- MySQL 8.x
- IntelliJ IDEA / VS Code（任选其一）

## 2. Clone and Initialize

```powershell
git clone <your-repo-url>
cd CampusHub
```

## 3. Backend Setup (Spring Boot)

```powershell
cd backend
.\mvnw.cmd -v
.\mvnw.cmd clean compile
```

运行后端：

```powershell
.\mvnw.cmd spring-boot:run
```

默认配置文件：`backend/src/main/resources/application.yml`

## 4. Frontend Setup (Vue 3 + Vite)

```powershell
cd frontend
npm -v
npm ci
npm run dev
```

构建与风格检查：

```powershell
npm run build
npm run lint
```

## 5. Node Path (Windows, if npm not found)

如果 `npm -v` 提示命令不存在，可将 Node 安装目录加入系统 `Path`。

示例（你当前环境）：

- `C:\Users\11053\AppData\Roaming\JetBrains\IntelliJIdea2025.2\node\versions\24.14.1`

说明：通常**不需要**额外添加 `...\node_modules\npm\bin` 到系统变量，除非特定工具链明确要求。

## 6. CI Local Parity Checks

提交前建议本地执行：

```powershell
cd backend
.\mvnw.cmd -DskipTests compile
.\mvnw.cmd -DskipTests checkstyle:check
cd ..\frontend
npm run build
npm run lint
```

