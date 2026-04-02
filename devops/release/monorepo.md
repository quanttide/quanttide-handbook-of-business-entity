# 单仓 (Mono-Repo) 发布

目前 AI 很容易在单仓发布版本时犯错，因此要注意提醒 AI 注意遵循单仓规范，建议先查看现有文件的规范和之前的实践。

## 核心规范

### Tag 命名规则

| 项目类型 | Git Tag 格式 | GitHub Release Tag | Release 标题 |
|----------|-------------|-------------------|-------------|
| 独立仓库 | `v0.1.0` | `v0.1.0` | `v0.1.0` |
| 单仓子模块 | `项目名/v0.1.0` | `项目名/v0.1.0` | `项目名/v0.1.0` |

### 发布流程

1. **更新 CHANGELOG.md** - 添加新版本和变更内容
2. **提交变更** - `cz commit` 或 `git commit -m "chore: bump version"`
3. **创建 Git Tag** - `git tag <project>/v<version>`
4. **推送 Tag** - `git push origin <project>/v<version>`
5. **创建 Release** - `gh release create <project>/v<version> --title "<project>/v<version>"`

### 关键原则

> **GitHub Release 的 Tag Name 必须与 Git Tag 完全一致**

这样 GitHub 才能正确关联 Release 和 Git Tag，避免混乱。

## 常见错误

### ❌ 错误：Release Tag 与 Git Tag 不一致

**问题**：Git Tag 使用 `cli/v0.0.1-alpha.4`，但 GitHub Release 使用 `v0.0.1-alpha.4`

**原因**：
1. 混淆了单仓项目与独立仓库的发布规范
2. 误以为 GitHub Release 的 Tag 应该去掉项目前缀
3. 文档规范不够明确

**正确做法**：
```bash
# Git Tag（带项目前缀）
git tag cli/v0.0.1-alpha.4
git push origin cli/v0.0.1-alpha.4

# GitHub Release（与 Git Tag 一致）
gh release create cli/v0.0.1-alpha.4 --title "cli/v0.0.1-alpha.4" --notes "..."
```

## 参考文档

- [Git 仓库资产管理](../../handbook/asset/governace/git_repo.md) - 版本发布规范章节
