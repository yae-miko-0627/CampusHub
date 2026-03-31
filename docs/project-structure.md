# Project Structure

当前项目采用前后端分离结构：

```text
CampusHub/
├─ backend/
│  ├─ src/main/java/com/campushub/campusbackend/
│  │  ├─ controller/
│  │  ├─ service/
│  │  └─ model/
│  └─ src/main/resources/
│     ├─ static/
│     └─ templates/
├─ frontend/
│  └─ src/
│     ├─ components/
│     └─ assets/
├─ docs/
│  ├─ P0/
│  ├─ development-setup.md
│  └─ git-branching-strategy.md
└─ .github/workflows/
```

## Convention

- 后端业务代码放置于 `controller/service/model`。
- 前端页面和组件放置于 `frontend/src`。
- 课程阶段性文档放置于 `docs/`（如 `P0`, `P1` ...）。
- CI 配置统一放置于 `.github/workflows/`。

