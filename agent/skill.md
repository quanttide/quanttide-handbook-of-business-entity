# Skill 工作流

Skill 是可复用的工作流程模板，来源于两种生成方式。

## 工作流一：自下而上总结

从 AGENTS 对话中提炼可复用技能。

1. **抽取到 CONTRIBUTING**：从 AGENTS 对话中抽取工作经验和流程，写入项目 CONTRIBUTING 文档
2. **抽取到项目 Skill**：将 CONTRIBUTING 中的某个主体内容提取为 `.agents/skills/<skill>/SKILL.md`
3. **同步到全局**：将稳定的 Skill 同步到 gallery 仓库。

## 工作流二：自上而下生成

从 specification 规范文档直接生成 Skill。

1. **编写规范文档**：在 specification 仓库编写标准规范
2. **生成 Skill**：将规范内容结构化为 `.agents/skills/<skill>/SKILL.md`
3. **发布 gallery**：发布 gallery 子模块并更新全局 Skill

## 示例

- 从 AGENTS 对话 → 写入 `CONTRIBUTING.md` → 创建 `.agents/skills/commit/SKILL.md`
- 从 specification 规范 → 生成 `.agents/skills/release/SKILL.md` → 发布 gallery
