# 更新记录

## 0.7.0

- 将 `pi_slot_deque` 依赖（dependency）提升至 `0.6`，间接使用 `pi_slotmap 0.6`，保留 `pi_key 0.4` 与 `pi_null 0.2`。
- 公开存储类型（public storage type）和队列类型（deque type）切换到新版依赖（dependency），通过次要版本（minor version）提升隔离已发布的 `0.6` 系列。
- 合入最新主分支（master），保留其 `move_from_external` 修复（fix）及多任务回归测试（regression test）。

## 0.6.0

- 升级直接依赖至 `pi_key = "0.4"`、`pi_slot_deque = "0.5"`，保留 `pi_null = "0.2"`。
- 公开键 trait、存储和队列类型关联新版依赖；调用方直接使用这些类型时需同步升级。方法调用方式不变。
- 修复 `move_from_external` 指定非队尾键时误迁移队尾任务的问题。
- 增加首层与高层的多任务回归测试，覆盖头部、中间键及目标槽已有任务的场景。
- 补充共享存储、轮外队列、按键迁入和依赖迁移说明。
