# Version Info

openEuler 24.03 LTS是基于6.6内核的长周期LTS版本（参见[版本生命周期](https://www.openeuler.org/zh/other/lifecycle/)），面向服务器、云、边缘计算、AI和嵌入式场景，提供更多新特性和功能，给开发者和用户带来全新的体验，服务更多的领域和更多的用户。<br />

# Release Plan

| Stage Name                    | Begin Time | End Time  | Days | Note                                               |
| ----------------------------- | ---------- | --------- | ---- | -------------------------------------------------- |
| Collect key features          | 2023/12/8  | 2024/1/30 | 54   | 版本需求收集                                       |
| Change Review 1               | 2024/1/16  | 2024/2/10 | 25   | Review 软件包变更（升级/退役/淘汰）                |
| Herited features              | 2024/1/30  | 2024/2/29 | 30   | 继承特性合入                                       |
| Develop                       | 2023/12/1  | 2024/2/29 | 90   | 新特性开发，合入master；KABI预留，白名单制定及公示 |
| Kernel freezing               | 2024/3/1   | 2024/3/10 | 10   | 内核冻结                                           |
| Branch 24.03 LTS              | 2024/3/11  | 2024/3/20 | 10   | master 拉取24.03 LTS Next及24.03 LTS分支           |
| Branch 24.03 LTS mass rebuild | 2024/3/21  | 2024/3/26 | 6    | 新分支大规模构建                                   |
| Build & Alpha                 | 2024/3/27  | 2024/4/2  | 7    | 新开发特性合入，Alpha版本发布                      |
| Test round 1                  | 2024/4/3   | 2024/4/9  | 7    | 24.03 LTS 启动集成测试                             |
| Change Review 2               | 2024/4/10  | 2024/4/12 | 3    | 发起软件包淘汰评审                                 |
| Beta version release          | 2024/4/13  | 2024/4/19 | 7    | 24.03 LTS Beta版本发布                             |
| Test round 2                  | 2024/4/20  | 2024/4/26 | 7    | 全量验证                                           |
| Change Review 3               | 2024/4/27  | 2024/4/29 | 3    | 分支启动冻结，只允许bug fix                        |
| Test round 3                  | 2024/4/30  | 2024/5/6  | 7    | 分支冻结，只允许bug fix                            |
| Test round 4                  | 2024/5/7   | 2024/5/13 | 7    | 回归测试                                           |
| Test round 5                  | 2024/5/14  | 2024/5/20 | 7    | 回归测试                                           |
| Release Review                | 2024/5/21  | 2024/5/23 | 3    | 版本发布决策/ Go or No Go                          |
| Release preparation           | 2024/5/24  | 2024/5/30 | 7    | 发布前准备阶段，发布件系统梳理                     |
| Release                       | 2024/5/31  | 2024/5/31 | 1    | 社区Release评审通过正式发布                        |



# Feature list

#### 状态说明：

- Discussion(方案讨论，需求未接受)
- Developing(开发中)
- Testing(测试中)
- Accepted(已验收)

| no   | feature | status | sig  | owner |
| :--- | :------ | :----- | :--- | :---- |
|      |         |        |      |       |

<br />
现启动版本需求收集，欢迎各sig maintainer和社区开发者们积极反馈和交流，<br />
<br />
需求反馈基本流程： <br />
1、开发者/sig在本贴的表格中填写要合入24.03-LTS的需求/特性，并同时填写需求issue <br />
2、申请在版本release management例会上评审需求 
<br /><br />