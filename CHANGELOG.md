# CHANGELOG

格式基于 [Keep a Changelog](https://keepachangelog.com/zh-CN/1.0.0/)。

版本遵循语义化版本规范：0.0.x（探索期）→ 0.x.y（验证期）→ x.y.z（正式期）

## [Unreleased]

## [0.2.0] - 2026-05-12

### Added

- myst.yml MyST 文档站点配置
- .github/workflows/deploy.yml GitHub Pages 部署工作流
- qtdata/project.md 项目管理文档
- qtdata/data.md 数字资产清单文档

### Changed

- qtdata/ 重构：engineering.md → data.md，management.md → project.md
- intro/vibe_anything.md 重命名为 intro/platform.md
- intro/ 目录重命名为 work/

### Removed

- 删除 meta/ 目录（README.md, memory/ 存档）
- 删除 write/ 目录（README.md, workflow.md）
- 删除 infra/ 目录（README.md, index.md, ubuntu.md, opencode.md, ollama.md, openclaw.md）

## [0.1.0] - 2026-05-05

### Added

- ROADMAP.md 产品路线图
- company-representative.md 法定代表人制度文档
- 企业文化手册 (culture.md)
- 招聘流程手册 (recruit.md) 及面试评估方法
- 供应商管理博弈策略 (vendor.md)
- BRD 文档方法体系（BRD 本质、方法论）
- 组织架构文档 (org.md)
- 技能生成工作流文档
- CONTRIBUTING 贡献指南
- Skill 工作流文档

### Changed

- 重构文化文档为结构化手册格式
- 重构招聘文档为手册格式
- 应用 docs-format 文档格式规范
- 标准化角色名称为"高级技术工程师"
- 精简 release 技能文档

## [0.0.6] - 2026-04-09

### Added

- 新增 scm/vendor.md：云厂商工单博弈实战策略，包含三轮不满意差评机制、水平判断标准和处理步骤话术

### Changed

- 优化 AGENTS.md：简化工作流程，引用 CONTRIBUTING 文档格式优化方法
- 优化 CONTRIBUTING.md：新增文档格式优化方法四步流程

## [0.0.5] - 2026-04-08

### Added

- 新增CONTRIBUTING.md：贡献指南和维护经验
- 新增devops/release.md：版本发布操作指南

### Changed

- 更新规范链接到v0.1.1
- 简化文档格式：删除加粗标签、减少层级
- 重组CHANGELOG：补充缺失的v0.0.2和v0.0.3版本记录

## [0.0.4] - 2026-04-02

### Added

- 合并quanttide-handbook-of-founder内容
  - asset/governace/ - 治理文档
  - devops/release/ - 发布流程
  - infra/ - 基础设施文档
  - meta/memory/ - 记忆存档
  - product/ - 产品文档
  - stdn/ - 标准文档
- 添加qtdata/目录：量潮数据商务拓展文档
  - index.md - 量潮数据概述
  - business.md - 商务拓展流程与系统规划
  - project.md - 项目管理文档

### Changed

- 更新根目录index.md包含新内容板块
- 更新README.md项目说明

## [0.0.3] - 2026-03-05

### Added

- 添加qtclass/目录：量潮课堂业务拓展文档
  - index.md - 量潮课堂概述
  - business.md - 业务拓展文档

## [0.0.2] - 2026-03-05

### Added

- 添加qtdata/目录：量潮数据商务拓展文档
  - index.md - 量潮数据概述
  - business.md - 商务拓展流程与系统规划
  - project.md - 项目管理文档

### Changed

- 更新根目录index.md包含qtdata板块
- 更新README.md项目说明

## [0.0.1] - 2026-03-05

### Added

- 初始化项目结构
- 添加LICENSE - 开源许可证
- 添加README.md - 项目说明
- 添加scm/目录：供应链管理
  - index.md - 供应链管理概述
  - purchase.md - 采购管理
