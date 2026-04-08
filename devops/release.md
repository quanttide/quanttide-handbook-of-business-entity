# 版本发布操作指南

## 规范来源

版本发布操作遵循量潮科技工程标准规范。

**最新版本**：[v0.1.0](https://github.com/quanttide/quanttide-specification-of-business-entity/releases/tag/v0.1.0)

**规范文档**：
- 版本发布标准：https://github.com/quanttide/quanttide-specification-of-business-entity/blob/v0.1.0/devops/release.md
- Git使用标准：https://github.com/quanttide/quanttide-specification-of-business-entity/blob/v0.1.0/devops/git.md

## 操作方法

### 使用opencode执行发布

1. **读取规范**：
   让opencode读取最新版本的发布规范文档链接

2. **执行发布**：
   opencode会根据规范自动执行以下步骤：
   - 更新CHANGELOG.md
   - 创建Git标签
   - 推送标签
   - 创建GitHub Release

3. **验证发布**：
   检查Release链接是否正确生成

## 链接不可变性

**重要**：使用版本化的链接（包含版本号），而不是main分支链接。

- ✅ 正确：`https://github.com/quanttide/quanttide-specification-of-business-entity/blob/v0.1.0/devops/release.md`
- ❌ 错误：`https://github.com/quanttide/quanttide-specification-of-business-entity/blob/main/devops/release.md`

版本化链接确保规范内容不可变，即使后续版本更新，当前版本链接指向的内容不会改变。

## 版本更新

当specification发布新版本时，更新本文档中的版本号和链接。

## 相关文档

- [AGENTS.md](../AGENTS.md) - AI操作指南（包含规范链接）
- [CHANGELOG.md](../CHANGELOG.md) - 版本历史记录