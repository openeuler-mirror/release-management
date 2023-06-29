# openEuler社区版本锁库
## 实现方案
- 锁库功能是在PR合入流程中通过对分支状态（冻结与否）判断实现拒绝合入；
- 分支状态由release-management仓库中release-management.yaml(https://gitee.com/openeuler/release-management/blob/release-management.yaml)文件记录；
- 社区机器人ci-bot实时监控分支状态文件，并确认版本特殊权限名单；
- 若分支为冻结状态，PR除满足原本合入条件外还需指定权限人同意才可合入；

## 操作方法
### 锁库
- 修改release-management.yaml(https://gitee.com/openeuler/release-management/blob/release-management.yaml)文件，在release项下增加分支冻结状态控制记录；
	 - [ ] branch：分支名称；
	 - [ ] frozen ：表示是否冻结仓库，true为锁库，false不锁库；
	 - [ ] owner ：特殊权限用户；

### 特殊权限合入
- 在锁库状态下，PR除了满足原本的合入条件外，还需特殊权限用户执行 /check-pr 或 /lgtm 或  /approve 才能合入；

