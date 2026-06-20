# CHANGELOG

格式基于 [Keep a Changelog](https://keepachangelog.com/zh-CN/1.0.0/)。

版本遵循语义化版本规范：0.0.x（探索期）→ 0.x.y（验证期）→ x.y.z（正式期）

## [Unreleased]

## [0.4.6] - 2026-06-20

### Added

- asset/quality.md：执行评估与输出诊断结果章节

### Changed

- 全部 27 份手册的附录检查清单从 `- [ ]` 格式改为验收标准段落
- asset/guide.md 重命名为 asset/index.md
- asset/audit.md 重命名为 asset/quality.md
- myst.yml 修复：移除已不存在的文件引用，合并重复的"组织管理"章节

### Removed

- 移除 `- [ ]` 复选框格式（全部改为验收标准描述）

## [0.4.5] - 2026-06-20

### Added

- human/recuritment/allocation.md：HR 配置工作指南（职级定级、权限配置、发展路径）

### Changed

- human/allocation/ 重命名为 human/relation/（入离职归入劳动关系管理）
- myst.yml 更新 human/ 路径

### Fixed

- myst.yml 新增 allocation.md 引用

## [0.4.4] - 2026-06-20

### Added

- human/recuritment/assessment.md：从招聘手册独立出考核细则
- human/recuritment/index.md：招聘手册，笔试阶段保留完整流程简介

### Changed

- 重构 human/ 目录：招聘相关移入 recuritment/，入离职移入 allocation/
- human/index.md 重写
- human/onboarding.md 精简标题
- myst.yml 更新 human/ 路径

### Removed

- human/recruitment.md（拆分为 recuritment/index.md + assessment.md）
- human/onboarding.md（移至 allocation/onboarding.md）
- human/resignation.md（移至 allocation/resignation.md）

## [0.4.3] - 2026-06-18

### Changed

- media/playbook.md：移除模因构建章节（移至教程），精简内容标准
- write/engineering.md：移除核心理念和验收标准（移至教程），保留AI写作流程和检查清单
- strategy/playbook.md：移至教程目录（纯概念内容，不适合手册）

## [0.4.2] - 2026-06-18

### Added

- 新增 sales/index.md 销售工作手册门户
- 新增 sales/workflow.md 销售流程工作手册（获客→触达→转化→跟进）
- 新增 sales/scripts.md 销售话术工作手册（6 场景标准话术）
- 新增 sales/platforms.md 销售工具工作手册（跟进表、日报、CRM）
- 新增 sales/channel.md 获客渠道工作手册（社交媒体、技术社群、口碑推荐）

### Changed

- sales/social-media.md 重命名为 channel.md 并扩展为多渠道手册
- 重构 sales/index.md 为 4 问题链结构（与商务手册对称）
- 减少不必要的表格使用

## [0.4.1] - 2026-06-17

### Added

- 新增 human/index.md 人力资源工作手册门户
- 新增 human/onboarding.md 入职操作手册
- 新增 human/training.md 培训与开发手册

### Changed

- 重构 human/recruitment.md：分解入职、离职、培训为非招聘内容，合并 recurit/index.md 考核标准
- 删除 human/recurit/ 招聘考核目录（内容合并至 recruitment.md，tech.md 迁至 gallery）
- 更新 myst.yml TOC，反映 human/ 新结构

## [0.4.0] - 2026-06-17

### Changed

- 标记整个 v0.3.x 开源内部手册的完成

## [0.3.23] - 2026-06-17

### Fixed

- myst.yml 重复 children key 导致 CI 构建失败

## [0.3.22] - 2026-06-17

### Changed

- intro/ 二次整理：39 个中文目录文件合并为 7 个英文文件（status/culture/ops/stakeholders/strategy/tactics）

## [0.3.21] - 2026-06-17

### Changed

- index.md 合并工作手册首页和欢迎加入量潮内容（手册体系分类+公开渠道）

## [0.3.20] - 2026-06-17

### Added

- intro/ 公司概况手册（量潮科技手册完整迁移：经营现状、企业文化、经营体系、利益相关方、战略体系、战术体系）

## [0.3.19] - 2026-06-17

### Added

- qtclass/customer.md 量潮课堂客户画像（学生+老师）
- qtclass/sales.md 量潮课堂招生工作手册（流程+渠道+招聘降级）

### Changed

- social-media/ 重命名为 media/
- qtclass/profile.md 重命名为 customer.md
- qtclass/enrollment.md 重命名为 sales.md

## [0.3.18] - 2026-06-17

### Changed

- enterprise/ 重命名为 enterpr/
- organization/ 合并到 org/

## [0.3.17] - 2026-06-17

### Changed

- digital/ 重命名为 asset/
- communication/ 重命名为 connect/
- entrepreneurship/ 重命名为 enterprise/

## [0.3.16] - 2026-06-17

### Added

- write/engineering.md 叙事工程手册（结构化写作管理+AI辅助流程）

### Changed

- narrative/ 目录重命名为 write/

## [0.3.15] - 2026-06-17

### Added

- training/plan.md 实训管理工作手册（两阶段培养方案）

## [0.3.14] - 2026-06-17

### Added

- knowl/engineering.md 知识工程手册（生命周期+DDD建模+人机协同策略）

## [0.3.13] - 2026-06-17

### Added

- agent/engineering.md 智能体工程手册（AIGC三大领域：提示词/上下文/智能体工程）
- infra/tools.md 基础设施手册（开发工具推荐清单）

## [0.3.12] - 2026-06-17

### Added

- course/deliberative.md 课程管理工作手册（议事型课堂教研与评估）

## [0.3.11] - 2026-06-17

### Added

- human/recruitment.md 人力资源工作手册（风投模型招聘体系）
- finance/guide.md 财务管理工作手册（现金流报警机制）
- legal/compliance.md 法务管理工作手册（VPN合规红绿灯）
- org/design.md 组织管理工作手册（辅助性原则+机制设计六步法）
- delib/playbook.md 议事管理工作手册（周会/OKR/审计管理）
- admin/guide.md 行政管理工作手册（任务管理/深思工作法/去中心化审批）
- digital/guide.md 数字资产管理工作手册（分类治理/信息披露原则）

## [0.3.10] - 2026-06-17

### Added

- risk/guide.md 风险管理工作手册（财务风险+项目风险）

## [0.3.9] - 2026-06-17

### Added

- social-media/playbook.md 新媒体运营手册（双号模型+模因构建制度）

## [0.3.8] - 2026-06-17

### Added

- communication/memo.md 沟通管理工作手册（基于备忘的沟通五大原则）

## [0.3.7] - 2026-06-17

### Added

- entrepreneurship/lifecycle.md 创业管理工作手册（企业生命周期模型）

## [0.3.6] - 2026-06-17

### Added

- pr/guide.md 公共关系手册（开发者关系/平台关系/公告管理）
- sales/social-media.md 销售管理手册（新媒体场景化截流SOP）

## [0.3.5] - 2026-06-17

### Added

- strategy/playbook.md 战略管理工作手册（涌现模型+敏捷周期）

## [0.3.4] - 2026-06-17

### Added

- brand/manifesto.md 品牌管理工作手册（个性挖掘模型）

## [0.3.3] - 2026-06-17

### Added

- community/playbook.md 社群运营工作手册（舞台剧模型）

## [0.3.2] - 2026-06-17

### Added

- customer/interview.md 客户关系手册（新客户访谈）

## [0.3.1] - 2026-06-17

### Added

- business/index.md 商务工作手册索引页
- business/service.md 商务服务工作手册（售前阶段）
- business/contract.md 商务合同工作手册（含框架协议场景）
- business/negotiation.md 商务谈判工作手册

### Changed

- business/quotation.md 合并报价规范内容（遵循先例原则、用户偏好、3:4:3结构）
- README.md 改为 index.md，表格改为列表

## [0.3.0] - 2026-05-19

### Added

- qtdata/asset/ 目录：概念框架、流程、业务规格、管理蓝图文档
- hr/ 目录：入职指引手册、离职操作手册
- qtclass/ 经营目标手册
- finance/ 个税退税流程手册
- asset/ 大规模集中治理工作流程手册

### Changed

- hr/ 重命名为 human/，入职指引与离职操作整合至 human/ 目录
- qtdata/ 融合企业服务流程
- asset/ 集中治理工作流程手册去掉技术细节，保留概念框架
- CONTRIBUTING.md 更新为手册写作风格
- 开源协议切换至 CC-BY-4.0

### Removed

- 删除入职指引手册（已整合至 human/）
- 删除集中治理工作流程手册（已重构）

## [0.2.1] - 2026-05-12

### Added

- qtdata/org.md 岗位职责手册
- qtdata/support.md 客户支持手册
- qtdata/data/ 数据管理文档（category.md, blueprint.md, workflow.md）
- data/index.md 数据工程概述
- qtdata/project.md 项目管理文档

### Changed

- myst.yml TOC 维护：移除已删除的 data.md，新增 org.md、support.md、qtdata/data/、data/index.md
- qtdata/ 更新：business.md 更新，data.md 删除

### Removed

- 从 myst.yml TOC 移除 CHANGELOG

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
