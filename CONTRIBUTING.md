# 贡献指南

欢迎贡献本项目！

## 贡献方式

- 报告问题：通过 GitHub Issues 反馈
- 提交修改：通过 Pull Request 贡献文档

## 提交流程

1. Fork 仓库
2. 创建分支：`git checkout -b feature/xxx`
3. 进行修改
4. 提交更改：遵循Git提交规范
5. 推送分支：`git push origin branch-name`
6. 创建 Pull Request

## 编写规范

### 文档格式规范

遵循量潮科技文档格式标准：
- 删：删除不必要的格式元素，优先用段落和标题
- 简：能用列表就不表格，能用文字就不列表
- 少：全文格式元素（分隔线、表格、加粗）尽量少
- 一：同一概念全程使用相同名称

具体规范：https://github.com/quanttide/quanttide-specification-of-business-entity/blob/v0.1.1/docs/format.md

### 手册资产规范

手册文档应该极简：
- 只说怎么做，不解释为什么
- 引用而非重复规范内容
- 版本化链接，一句话说明更新方法

具体规范：https://github.com/quanttide/quanttide-specification-of-business-entity/blob/v0.1.1/asset/category/handbook.md

## 版本发布

操作指南：devops/release.md

规范来源：https://github.com/quanttide/quanttide-specification-of-business-entity/blob/v0.1.1/devops/release.md

## 维护经验

### Release notes格式问题

问题：opencode使用`--generate-notes`创建Release，自动生成的Release notes可能不符合CHANGELOG格式。

检查：对比Release notes与CHANGELOG中对应版本的内容。

纠正：通过GitHub API更新Release notes内容。

预防：让opencode创建Release后，主动询问是否需要更新Release notes。

### 文档格式优化

避免：
- 加粗标签（如**问题**、**方法**）
- 不必要的子标题
- 冗余的列表层级

采用：
- 段落直接说明
- 极简的列表
- 必要的代码示例