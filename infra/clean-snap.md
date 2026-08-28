# 检查云资源快照使用情况

## 背景

阿里云 ECS 运行在多个区域（cn-hangzhou、cn-shanghai、us-east-1），手动快照与自动快照会持续积累。快照按存储量计费，其中不再被使用的「孤儿快照」是纯成本浪费——源磁盘已释放、或没有任何资源依赖它的快照，留着只会持续扣费。

清理快照前必须先盘点：确认哪些快照还在被使用、哪些可以清理。本检查脚本是清理流程的第一步（只读操作），输出各区域快照的使用情况，为清理决策提供依据。

## 检查脚本

```bash
#!/bin/bash
# check-orphan-resources.sh - 检查各区域快照使用情况
REGIONS="cn-hangzhou cn-shanghai us-east-1"

for region in $REGIONS; do
  echo "=== $region ==="
  aliyun ecs DescribeSnapshots --RegionId $region --PageSize 50 \
    --query 'Snapshots.Snapshot[].{Name:SnapshotName,Size:SourceDiskSize,Created:CreationTime,Usage:Usage}' \
    --output table 2>/dev/null
done
```

## 输出字段说明

| 字段 | 含义 | 用途 |
|------|------|------|
| Name | 快照名称 | 识别快照来源：手动快照通常含实例名，自动快照有固定前缀 |
| Size | 源盘大小 | 估算快照费用：按存储量计费，源盘越大费用越高 |
| Created | 创建时间 | 判断时效：长期未更新的旧快照优先考虑清理 |
| Usage | 用途 | 判断是否仍被使用：有用途的快照不可清理 |

## 使用步骤

1. 运行脚本，按区域查看快照清单
2. 标记疑似孤儿快照：用途为空、且无法对应到现有磁盘或镜像的快照
3. 对疑似孤儿快照核实：确认源磁盘已释放、无镜像依赖
4. 核实后执行清理（删除快照不可恢复，需二次确认）

## 注意事项

- 脚本是只读检查，可随时运行，不影响线上资源
- 快照数量多时注意分页（PageSize 50）：输出不完整时需翻页查看
- 删除快照前必须完成核实：快照删除不可恢复，误删可能导致数据无法找回
- 本检查应纳入定期运维节奏，与费用监控联动
