# Version Info

openEuler 24.09 LTS是基于6.6内核的创新版本（参见[版本生命周期](https://www.openeuler.org/zh/other/lifecycle/)）。<br />

# Release Plan

| Stage Name                    | Begin Time | End Time  | Days | Note                                               |
| ----------------------------- | ---------- | --------- | ---- | -------------------------------------------------- |
| Collect key features          | 2024/6/3   | 2024/7/16 | 44   | 版本需求收集                                       |
| Change Review 1               | 2024/7/1  | 2024/7/12 | 25   | Review 软件包变更（升级/退役/淘汰）                |
| Herited features              | 2024/7/1  | 2024/7/22 | 23   | 继承特性合入（Branch前完成合入）  |
| Develop                       | 2024/7/1  | 2024/8/19 | 50   | 新特性开发，合入master |
| Kernel freezing               | 2024/7/16   | 2024/7/22 | 10   | 内核冻结                                           |
| Branch 24.09                  | 2024/7/22  | 2024/8/5 | 15 | master 拉取 24.09 分支           |
| Build & Alpha                 | 2024/8/6  | 2024/8/12  | 7    | 新开发特性合入，Alpha版本发布                      |
| Test round 1                  | 2024/8/13   | 2024/8/19  | 7   | 24.09 启动集成测试                             |
| Change Review 2               | 2024/8/13  | 2024/8/15 | 3    | 发起软件包淘汰评审                                 |
| Beta version release          | 2024/8/16  | 2024/8/19 | 4    | 24.09 Beta版本发布                             |
| Test round 2                  | 2024/8/20  | 2024/8/26 | 7    | 全量验证                                           |
| Change Review 3               | 2024/8/27  | 2024/8/29 | 3    | 分支启动冻结，只允许bug fix                        |
| Test round 3                  | 2024/8/29  | 2024/9/4  | 7    | 分支冻结，只允许bug fix                            |
| Test round 4                  | 2024/9/5   | 2024/9/11 | 7    | 回归测试                                           |
| Test round 5                  | 2024/9/12  | 2024/9/19 | 7    | 回归测试（跨中秋节，预祝中秋节快乐）                 |
| Release Review                | 2024/9/20  | 2024/9/22 | 3    | 版本发布决策/ Go or No Go                          |
| Release preparation           | 2024/9/23  | 2024/9/28 | 6    | 发布前准备阶段，发布件系统梳理                     |
| Release                       | 2024/9/29  | 2024/9/30 | 2    | 社区Release评审通过正式发布                        |



# Feature list

#### 状态说明：

- Discussion(方案讨论，需求未接受)
- Developing(开发中)
- Testing(测试中)
- Accepted(已验收)

| no   | feature | status | sig  | owner |
| :--- | virtCCA机密虚机特性合入 | Discussion | SIG-Kernel/SIG-Virt | @luoyukai |
| :--- | virtCCA coDA特性合入 | Discussion  | SIG-Kernel/SIG-Virt | @luoyukai |
| :--- | :------ | :----- | :--- | :---- |
|[I9UYO9](https://gitee.com/openeuler/release-management/issues/I9UYO9?from=project-issue)| virtCCA机密虚机特性合入 | Discussion | SIG-Kernel/SIG-Virt | [@luoyukai](https://gitee.com/luoyukai) |

<br />
现启动版本需求收集，欢迎各sig maintainer和社区开发者们积极反馈和交流，<br />
<br />
需求反馈基本流程： <br />
1、开发者/sig在本贴的表格中填写要合入24.09的需求/特性，并同时填写需求issue <br />
2、申请在版本release management例会上评审需求 
<br /><br />
