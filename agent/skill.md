# Skill 工作流

从 AGENTS 对话中提炼可复用技能的标准流程。

## 工作流

1. **抽取到 CONTRIBUTING**：从 AGENTS 对话中抽取工作经验和流程，写入项目 CONTRIBUTING 文档
2. **抽取到项目 Skill**：将 CONTRIBUTING 中的某个主体内容提取为 `.agents/skills/<skill>/SKILL.md`
3. **同步到全局**：将稳定的 Skill 同步到 gallery 仓库，并安装到全局 `.agents`

## 示例

- 从 AGENTS 对话 → 写入 `CONTRIBUTING.md`
- 从 `CONTRIBUTING.md` 提交规范 → 创建 `.agents/skills/commit/SKILL.md`
- 发布 gallery 子模块，更新全局 `.agents/skills`