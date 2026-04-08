# AGENTS.md

本仓库是量潮科技工作手册系统中的公司手册。

## 工程标准规范

遵循量潮科技工程标准规范，使用版本化链接保持内容不可变：

**最新版本**：v0.1.0

- 版本发布标准：https://github.com/quanttide/quanttide-specification-of-business-entity/blob/v0.1.0/devops/release.md
- Git使用标准：https://github.com/quanttide/quanttide-specification-of-business-entity/blob/v0.1.0/devops/git.md
- 文档格式标准：https://github.com/quanttide/quanttide-specification-of-business-entity/blob/v0.1.0/docs/format.md
- Git仓库标准：https://github.com/quanttide/quanttide-specification-of-business-entity/blob/v0.1.0/asset/type/git_repo.md

## Project Overview

This is the **quanttide-handbook-of-business-entity** submodule, part of the quanttide handbook system. It contains documentation for business entities, specifically focusing on supply chain management (SCM).

## Project Structure

```
.
├── CHANGELOG.md      # Change log following Keep a Changelog format
├── LICENSE          # Open source license
├── README.md        # Project description
├── index.md         # Content overview
├── scm/             # Supply chain management documentation
│   ├── index.md     # SCM overview
│   └── purchase.md  # Purchasing management
└── qtdata/          # Quanttide data business development
    ├── index.md     # Quanttide data overview
    ├── business.md  # Business expansion processes
    └── project.md   # Project management documentation
```

## Content Architecture

- **SCM Documentation**: The `scm/` directory contains supply chain management documentation
  - `index.md`: Overview of supply chain management, content structure, and core topics
  - `purchase.md`: Detailed purchasing workflows, types, and supplier management

- **Quanttide Data Documentation**: The `qtdata/` directory contains business development and customer management documentation
  - `index.md`: Overview of quanttide data business development
  - `business.md`: Customer message handling processes and system automation planning
  - `project.md`: Project scope decomposition and time management processes

## Relationship to Parent Repository

This is a **Git submodule** managed by the parent repository `quanttide-handbook`. Key rules from parent AGENTS.md:

1. **Do NOT modify submodule files directly in parent repository**
2. **Make changes in submodule repository independently, then update reference in parent**
3. **Build commands are executed at parent level**

## Common Commands

Since this is a documentation submodule, there are no build, test, or lint commands specific to this directory. All Jupyter Book builds are performed at the parent repository level.

### Git Submodule Operations

```bash
# Update submodule to latest commit from remote
git submodule update --remote --merge

# Check submodule status
git submodule status

# Update parent repository reference after submodule changes
git add entity/company
git commit -m "Update submodule reference"
```

## Development Workflow

1. **Edit documentation**: Modify Markdown files in this submodule
2. **Commit changes**: Commit and push to the submodule repository
3. **Update parent**: In parent repository, update submodule reference
4. **Build verification**: Build is performed at parent level using `jupyter-book build index.md --site`

## File Naming and Structure Conventions

- Use meaningful directory names (e.g., `scm/` for supply chain management)
- Each directory should have an `index.md` file providing overview
- Follow consistent Markdown formatting
- Update `CHANGELOG.md` for significant changes following semantic versioning:
  - `0.0.x` (exploration phase)
  - `0.x.y` (validation phase)  
  - `x.y.z` (production phase)

## Key Considerations

- This is a **documentation-only** repository - no code, tests, or build configurations
- All Jupyter Book configuration and building happens at parent level
- Maintain clear separation between different documentation domains (SCM, qtdata, etc.)
- Keep internal links relative and ensure linked files exist
- Update both `index.md` and `README.md` when adding new content sections
- Follow the same pattern for new domains: create directory with `index.md` and topic-specific files