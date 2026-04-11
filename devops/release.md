# 版本发布操作指南

## Skill 位置

发布技能已提炼到 gallery 仓库：[https://github.com/quanttide/quanttide-gallery-of-business-entity/blob/v0.0.3/devops/release/SKILL.md](https://github.com/quanttide/quanttide-gallery-of-business-entity/blob/v0.0.3/devops/release/SKILL.md)

## 使用方法

1. 复制 skill 到本地 `.agents/skills/release/SKILL.md`
2. 提示 opencode 使用 release 技能执行发布

```bash
# 示例：将 skill 复制到本地系统
cp docs/gallery/devops/release/SKILL.md .agents/skills/release/SKILL.md
```

## 规范来源

版本发布操作遵循量潮科技工程标准的版本发布标准
[https://github.com/quanttide/quanttide-specification-of-business-entity/blob/v0.1.1/devops/release.md](https://github.com/quanttide/quanttide-specification-of-business-entity/blob/v0.1.1/devops/release.md)
当 specification 发布新版本时，更新本文档中的版本号和链接。

## 操作方法

使用 opencode 执行发布：

1. 让 opencode 读取最新版本的发布规范文档链接
2. opencode 会根据规范自动执行：更新 CHANGELOG.md、创建 Git 标签、推送标签、创建 GitHub Release
3. 检查 Release 链接是否正确生成

## 问题处理

### Release notes不符合规范

opencode使用`--generate-notes`创建Release，自动生成的Release notes可能不符合CHANGELOG格式。

检查方法：对比Release notes与CHANGELOG中对应版本的内容是否一致。

纠正方法：
```bash
gh api repos/<owner>/<repo>/releases/<release-id> \
  -X PATCH \
  -f body="### Added

- 内容从CHANGELOG提取

### Changed

- 内容从CHANGELOG提取"
```

预防措施：让opencode创建Release后，主动询问是否需要更新Release notes。
