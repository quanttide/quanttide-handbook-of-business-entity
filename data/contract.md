# 数据契约

数据契约（Data Contract）是数据生产方与消费方之间的约定，定义数据的结构、质量、时效和安全。

## 契约元数据

| 字段 | 说明 | 示例 |
|------|------|------|
| `contract_version` | 契约版本号 | `1.0.0` |
| `schema_version` | Schema 版本号 | `0.0.1` |
| `id` | 资产唯一标识 | `garment-factory` |
| `name` | 资产名称 | 隆昌制衣厂数据清洗 |
| `description` | 资产描述 | — |

## 契约双方（parties）

| 角色 | 说明 |
|------|------|
| `provider` | 数据提供方（名称、联系人、复核人） |
| `consumer` | 数据消费方（名称、联系人） |

## 时效承诺（sla）

| 字段 | 说明 |
|------|------|
| `delivery_deadline` | 交付截止日期 |
| `project_duration` | 项目工期 |
| `delivery_mode` | 交付方式（如"分批交付"） |
| `penalty` | 违约条款 |

## 安全与保密（security）

| 字段 | 说明 |
|------|------|
| `classification` | 密级（公开/内部/机密） |
| `policies` | 安全策略列表 |

## 数据资产（raw_assets / cleaned_assets）

每个资产包含以下标准字段：

| 字段 | 说明 | 必填 |
|------|------|------|
| `id` | 资产唯一标识 | ✓ |
| `name` | 资产名称 | ✓ |
| `path` | 文件路径 | ✓ |
| `format` | 文件格式（xlsx/csv/dta/json） | ✓ |
| `source` | 数据来源 | ✓ |
| `description` | 资产描述 | ✓ |
| `schema.fields` | 字段级 Schema 定义 | ✓ |
| `quality` | 质量验收规则 | 仅 cleaned |
| `owners` | 数据负责人列表 | 可选 |
| `count` | 文件数量 | 可选 |
| `notes` | 备注 | 可选 |

### 字段级 Schema（schema.fields）

| 字段 | 说明 | 示例 |
|------|------|------|
| `name` | 字段名 | `款号` |
| `type` | 数据类型 | `string` / `integer` / `float` / `date` |
| `description` | 字段描述 | "款式编号，需清洗冗余符号" |
| `nullable` | 是否可空 | `true` / `false` |
| `enum` | 枚举值列表 | 可选 |

### 质量验收规则（quality）

| 字段 | 说明 | 示例 |
|------|------|------|
| `match_rate` | 匹配率阈值 | `>= 90%` |
| `row_count` | 行数一致性要求 | "与源表一致" |
| `key_uniqueness` | 主键唯一性 | `true` |
| `unmatched_fill` | 未匹配填充策略 | `0` / `null` |

## 数据血缘（lineage）

每条血缘记录包含：

| 字段 | 说明 |
|------|------|
| `step` | pipeline 步骤标识 |
| `inputs` | 输入资产路径列表 |
| `output` | 输出资产路径 |

## 全局验收规则（acceptance）

| 字段 | 说明 | 示例 |
|------|------|------|
| `rule` | 规则名称 | "款号匹配率" |
| `threshold` | 阈值 | `>= 90%` |
| `method` | 检验方法 | "统计匹配成功/失败记录数" |

## 变更日志（changelog）

| 字段 | 说明 |
|------|------|
| `version` | 版本号 |
| `date` | 变更日期 |
| `changes` | 变更说明 |
