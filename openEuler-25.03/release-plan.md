# Version Info
openEuler 25.03 是基于6.6内核的创新版本（参见[版本生命周期](https://www.openeuler.org/zh/other/lifecycle/)），面向服务器、云、边缘计算和嵌入式场景，提供更多新特性和功能，给开发者和用户带来全新的体验，服务更多的领域和更多的用户。<br>


# Release Plan

| Stage Name                    | Deadline for PR | Begin Time | End Time   | Days | Note                                     |
| ----------------------------- | --------------- | ---------- | ---------  | ---- | ---------------------------------------- |
| Collect key features          |        -        | 2024/12/1  | 2025/1/31  | 61 | 版本需求收集                              |
| Change Review 1               |        -        | 2025/1/2   | 2025/1/16  | 15 | Review 软件包变更（升级/退役/淘汰）  |
| Herited features              |        -        | 2025/1/2   | 2025/2/18  | 25 | 继承特性合入（Branch前完成合入） |
| Develop                       |        -        | 2025/1/2   | 2025/2/25  | 55 | 新特性开发，合入Master |
| Kernel freezing               |        -        | 2025/1/23  | 2024/2/27  | 8  | 内核冻结（随Beta版本，内核冻结） |
| Branch 24.03 LTS SP1          |        -        | 2025/1/23  | 2025/2/6   | 7  | Master 拉取 25.03 分支 (跨春节，预祝开发者春节快乐) |
| Build & Alpha                 |        -        | 2025/2/7   | 2025/2/13  | 7  | 新开发特性合入，Alpha版本发布    |
| Test round 1                  |    2025/2/11    | 2025/2/14  | 2025/2/20  | 7  | 25.03 模块测试           |
| Change Review 2               |        -        | 2025/x/xx  | 2025/x/xx  | 3  | 发起软件包淘汰评审               |
| Test round 2 (Beta Version)   |    2025/2/18    | 2025/2/21  | 2025/2/27  | 7  | 25.03 Beta版本发布       |
| Test round 3                  |    2025/2/25    | 2025/2/28  | 2025/3/6   | 7  | 全量验证(全量SIT)                |
| Change Review 3               |        -        | 2025/x/x   | 2025/x/x   | 3  | 只允许bug fix      |
| Test round 4                  |    2025/3/4     | 2025/3/7   | 2025/3/13  | 7  | 分支冻结，只允许bug fix          |
| Test round 5                  |    2025/3/11    | 2025/3/14  | 2025/3/20  | 7  | 回归测试                         |
| Test round 6 (预留)           |    2025/3/18    | 2025/3/21  | 2025/3/25  | 7  | 回归测试                         |
| Release Review                |        -        | 2025/3/25  | 2025/3/26  | 2  | 版本发布决策/ Go or No Go        |
| Release preparation           |        -        | 2025/3/27  | 2025/3/28  | 2  | 发布前准备阶段，发布件系统梳理    |
| Release                       |        -        | 2025/3/28  | 2025/3/31  | 2  | 社区Release评审通过正式发布       |



# 代码合入说明
创新版本代码继承master分支 <br>
// 新特性代码请及时合入版本&自验证，跟随整体计划赶在第一轮转测试


# Feature list
状态说明：Discussion(方案讨论，需求未接受)、 Developing(开发中)、 Testing(测试中)、 Accepted(已验收) <br>
发布方式：ISO、Everything、EPOL、oepkgs、独立发布等

|no|feature|status|sig|owner|发布方式|涉及软件包列表|
|:----|:---|:---|:--|:----|:----|:----|
||||||||


# 需求/特性反馈基本流程 <br />
1、开发者/sig在本贴的表格中填写要合入23.03的需求/特性，并同时填写需求issue及链接 （请在收集截止时间前提交）      <br>
2、申请在版本release management sig例会上评审需求 （owner或者SIG maintainer参会）
<br><br>
