# 版本发布操作指南

## 规范来源

版本发布操作遵循量潮科技工程标准的版本发布标准
[https://github.com/quanttide/quanttide-specification-of-business-entity/blob/v0.1.0/devops/release.md](https://github.com/quanttide/quanttide-specification-of-business-entity/blob/v0.1.0/devops/release.md)
当specification发布新版本时，更新本文档中的版本号和链接。

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
