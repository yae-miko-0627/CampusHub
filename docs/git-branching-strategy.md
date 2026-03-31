# Git Branching Strategy

## Branch Roles

- `main`: 稳定可发布分支，仅通过 Pull Request 合并。
- `dev`: 日常集成分支，功能开发合并到该分支后统一测试。
- `feature/<name>`: 功能分支，从 `dev` 拉取，完成后合并回 `dev`。
- `hotfix/<name>`: 紧急修复分支，从 `main` 拉取，修复后同时回合并到 `main` 和 `dev`。

## Workflow

1. 从 `dev` 创建功能分支：`feature/task-name`
2. 本地开发并提交（建议小步提交）
3. 发起到 `dev` 的 Pull Request
4. CI 通过 + 代码评审通过后合并
5. 里程碑版本由 `dev` 合并到 `main`

## Commit Message Convention (建议)

- `feat:` 新功能
- `fix:` 缺陷修复
- `docs:` 文档更新
- `refactor:` 重构
- `test:` 测试相关
- `chore:` 构建/依赖/工具维护

