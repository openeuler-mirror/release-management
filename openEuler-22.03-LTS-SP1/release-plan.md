# Version Info
openEuler 22.03 LTS SP1 是基于5.10内核的创新版本（参见[版本生命周期](https://www.openeuler.org/zh/other/lifecycle/)），面向服务器、云、边缘计算和嵌入式场景，提供更多新特性和功能，给开发者和用户带来全新的体验，服务更多的领域和更多的用户。<br>


# Release Plan

| Stage  name          | Begin time | End time   | Days | Note                                      |
| -------------------- | ---------- | ---------- | ---- | ----------------------------------------- |
| Collect key features | 2022/9/2  | 2022/9/30 | 28   | 收集22.03 LTS SP1版本关键特性（各SIG自行录入release-plan）   |

# 代码合入说明
创新版本代码继承22.03 LTS NEXT分支 <br>
// 新特性代码请及时合入版本&自验证，跟随整体计划赶在第一轮转测试


# Feature list
状态说明：Discussion(方案讨论，需求未接受)、 Developing(开发中)、 Testing(测试中)、 Accepted(已验收) <br>
发布方式：ISO、EPOL、oepkgs、独立发布等

|no|feature|status|sig|owner|发布方式|涉及软件包列表|
|:----|:---|:---|:--|:----|:----|:----|
| [I5RDEG](https://gitee.com/openeuler/release-management/issues/I5RDEG) | DDE组件更新支持服务器场景优化 | Discussion | sig-DDE | [@weidongkl](https://gitee.com/weidongkl) [@panchenbo](https://gitee.com/panchenbo) | EPOL |     |
|[I5RDGW](https://gitee.com/openeuler/release-management/issues/I5RDGW)|新增软件更新工具支持|Discussion|sig-DDE|[@weidongkl](https://gitee.com/weidongkl) [@panchenbo](https://gitee.com/panchenbo)|EPOL|deepin-upgrade-tool|
|[I5RDJS](https://gitee.com/openeuler/release-management/issues/I5RDJS)|新增备份还原功能支持|Discussion|sig-Migration|[@blueblue](https://gitee.com/blublue)|EPOL|ubackup|
|现启动版本需求/特性收集，欢迎各sig maintainer和社区开发者们积极反馈和交流，<br>|||||||
|<br>|||||||

# 需求/特性反馈基本流程 <br />
1、开发者/sig在本贴的表格中填写要合入22.03 LTS SP1的需求/特性，并同时填写需求issue及链接 （请在收集截止时间前提交）      <br>
2、申请在版本release management sig例会上评审需求 （owner或者SIG maintainer参会）
<br><br>
