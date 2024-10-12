# Version Info

openEuler 24.03 LTS SP1是基于6.6内核的24.03-LTS版本增强扩展版本（参见[版本生命周期](https://www.openeuler.org/zh/other/lifecycle/)），面向服务器、云、边缘计算和嵌入式场景，持续提供更多新特性和功能扩展，给开发者和用户带来全新的体验，服务更多的领域和更多的用户。<br />

# Release Plan

| Stage Name                    | Begin Time | End Time  | Days | Note                                     |
| ----------------------------- | ---------- | --------- | ---- | ---------------------------------------- |
| Collect key features          | 2024/9/1   | 2024/10/31 | 61 | 版本需求收集                              |
| Change Review 1               | 2024/10/8  | 2024/10/18 | 11 | Review 软件包变更（升级/退役/淘汰）SP版本尽可能保持版版本不变  |
| Herited features              | 2024/10/8  | 2024/11/1  | 25 | 继承特性合入（Branch前完成合入） |
| Develop                       | 2024/10/8  | 2024/11/28 | 58 | 新特性开发，合入24.03 LTS Next   |
| Kernel freezing               | 2024/11/1  | 2024/11/8  | 8  | 内核冻结 |
| Branch 24.03 LTS SP1          | 2024/11/1  | 2024/11/7  | 10 | 24.03 LTS Next 拉取 24.03 LTS SP1 分支 |
| Build & Alpha                 | 2024/11/8  | 2024/11/14 | 7  | 新开发特性合入，Alpha版本发布    |
| Test round 1                  | 2024/11/15 | 2024/11/21 | 7  | 24.03 LTS SP1 模块测试           |
| Change Review 2               | 2024/11/22 | 2024/11/24 | 3  | 发起软件包淘汰评审               |
| Test round 2 (Beta Version)   | 2024/11/22 | 2024/11/28 | 7  | 24.03 LTS SP1 Beta版本发布       |
| Test round 3                  | 2024/11/29 | 2024/12/5  | 7  | 全量验证(全量SIT)                |
| Change Review 3               | 2024/12/3  | 2024/12/5  | 3  | 分支启动冻结，只允许bug fix      |
| Test round 4                  | 2024/12/6  | 2024/12/12 | 7  | 分支冻结，只允许bug fix          |
| Test round 5                  | 2024/12/13 | 2024/12/19 | 7  | 回归测试                         |
| Test round 6 (预留)           | 2024/12/20 | 2024/12/26 | 7  | 回归测试                         |
| Release Review                | 2024/12/19 | 2024/12/20 | 2  | 版本发布决策/ Go or No Go        |
| Release preparation           | 2024/12/27 | 2024/12/28 | 2  | 发布前准备阶段，发布件系统梳理    |
| Release                       | 2024/12/30 | 2024/12/31 | 2  | 社区Release评审通过正式发布       |



# Feature list

#### 状态说明：

- Discussion(方案讨论，需求未接受)
- Developing(开发中)
- Testing(测试中)
- Accepted(已验收)

| no   | feature | status | sig  | owner |
| :--- | :------ | :----- | :--- | :---- |
| [IASH0C](https://gitee.com/openeuler/release-management/issues/IASH0C) | wine5.5升级到wine9.17，不需要linux32依赖库情况下支持win32程序|Discussion|sig-compat-winapp|[@itisyang](https://gitee.com/itisyang)|
| [IATGD8](https://gitee.com/openeuler/release-management/issues/IATGD8) | Add compatibility patches for Zhaoxin processors | Discussion | kernel            | [leoliu-oc](https://gitee.com/leoliu-oc) |
| [IAUPHP](https://gitee.com/openeuler/release-management/issues/IAUPHP) | virtCCA机密虚机特性合入|Discussion|SIG-Kernel/SIG-Virt|[@luoyukai](https://gitee.com/luoyukai)|
| [IAWIGO](https://gitee.com/openeuler/release-management/issues/IAWIGO) | virtCCA+kata机密容器特性合入版本|Discussion|机密计算SIG/云原生SIG|[@luoyukai](https://gitee.com/luoyukai)|


<br />
现启动版本需求收集，欢迎各sig maintainer和社区开发者们积极反馈和交流，<br />
<br />
需求反馈基本流程： <br />
1、开发者/sig在本贴的表格中填写要合入24.03 LTS SP1的需求/特性，并同时填写需求issue <br />
2、申请在版本release management例会上评审需求 
<br /><br />
