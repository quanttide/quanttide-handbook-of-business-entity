# 版本发布操作指南

## 规范来源

版本发布操作遵循量潮科技工程标准的版本发布标准
[https://github.com/quanttide/quanttide-specification-of-business-entity/blob/v0.1.1/devops/release.md](https://github.com/quanttide/quanttide-specification-of-business-entity/blob/v0.1.1/devops/release.md)
当specification发布新版本时，更新本文档中的版本号和链接。

## 操作方法

使用opencode执行发布：

1. 让opencode读取最新版本的发布规范文档链接
2. opencode会根据规范自动执行：更新CHANGELOG.md、创建Git标签、推送标签、创建GitHub Release
3. 检查Release链接是否正确生成

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
