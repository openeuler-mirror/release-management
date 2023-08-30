# Version Info
openEuler 20.03-LTS-SP4 作为20.03-LTS版本的增强扩展版本（参见[版本生命周期](https://www.openeuler.org/zh/other/lifecycle/)），面向服务器、云、边缘计算和嵌入式场景，提供更多新特性和功能增强，给开发者和用户带来更加稳定可靠的体验，服务更多的领域和更多的用户。<br>


# Release Plan

| Stage  name          | Begin time | End time   | Days | Note                                      |
| -------------------- | ---------- | ---------- | ---- | ----------------------------------------- |
| Collect key features | 2023/8/10      | 2023/9/10    | 30       | 收集openEuler 20.03-LTS-SP4版本关键特性（各SIG自行录入release-plan）    |
| Develop              | 2023/8/10      | 2023/9/24    | 45       | 特性完成开发和自验证，代码提交合入openEuler 20.03-LTS-SP4              |
| 内核冻结             | 2023/9/25      | 2023/9/30    | 5      | 内核冻结，KABI接口基线化评审 |
| 分支全量Build        | 2023/10/8      | 2023/10/12    | 5       | 拉取openEuler 20.03-LTS-SP4分支，完成分支全量构建 |
| Alpha                | 2023/10/14      | 2023/10/18    | 5        | 发布Alpha版本，启动全版本功能冒烟测试                            |
| Test round 1（Beta） | 2023/10/21      | 2023/10/25    | 5        | 发布Beta版本，启动版本SIT测试                                |
| Test round 2         | 2023/10/28      | 2023/11/1     | 5        | SIT测试，特性基线合入冻结，不再接纳功能性代码合入                                                      |
| Test round 3         | 2023/11/4       | 2023/11/8     | 5        |   SIT测试                |
| Test round 4         | 2023/11/11      | 2023/11/15    | 5        |   SIT测试                                                     |
| Test round 5         | 2023/11/18      | 2023/11/22    | 5        |   发布release预览版本，版本缺陷回归验证                                                     |
| Release              | 2023/11/28      | 2023/11/28    | 1        |   版本GO/NO GO发布评审                                               |


# 代码合入说明
openEuler 20.03-LTS-SP4 版本基线继承openEuler 20.03-LTS-Next分支 <br>
// 新特性代码请及时合入版本&自验证，跟随整体计划赶在第一轮转测试


# Feature list
状态说明：Discussion(方案讨论，需求未接受)、 Developing(开发中)、 Testing(测试中)、 Accepted(已验收) <br>
发布方式：ISO、EPOL、oepkgs、独立发布等

|no|feature|status|sig|owner|发布方式|涉及软件包列表|
|:----|:---|:---|:--|:----|:----|:----|
|1|eNFS|Discussion|Kernel|闫海涛|ISO|nfs，sunrpc，eNfs|
|2|metalink|Discussion|Infrastructure|mywaaagh_admin|ISO|openEuler-repos|
|3|OpenStack Train|Discussion|OpenStack|郑挺|EPOL|OpenStack-SIG|

<br>
现启动版本需求/特性收集，欢迎各sig maintainer和社区开发者们积极反馈和交流，<br>
<br>



# 需求/特性反馈基本流程 <br />
1、开发者/sig在本贴的表格中填写要合入openEuler 20.03-LTS-SP4的需求/特性，并同时填写需求issue及链接 （请在收集截止时间前提交）      <br>
2、申请在版本release management sig例会上评审需求 （owner或者SIG maintainer参会）
<br><br>
