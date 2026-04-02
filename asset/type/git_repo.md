# Git仓库

## 通用

- docs: 文档
- src: 代码

## 产品单仓

### Structure

- docs 
  - prd: 产品需求文档 
  - add: 架构设计文档
  - idx: 交互设计文档
  - qa: 质量保证文档
  - user: 用户文档
- src
  - provider: FastAPI
  - studio: Flutter
  - cli: typer
    - docs
      - dev
      - ops


### Workflow

需求prd -> 前后端设计 add idx -> 各个子项目 dev -> 子项目ops -> 验收 qa -> 表达 user

### refactor

丢弃cli的Python代码换成Rust： 丢弃的文档是和这个Python项目直接相关的实现，不变的部分写在add。
