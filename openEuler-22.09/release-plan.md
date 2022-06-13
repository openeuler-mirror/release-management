# Version Info
openEuler 22.09 是基于5.10内核的创新版本（参见[版本生命周期](https://www.openeuler.org/zh/other/lifecycle/)），面向服务器、云、边缘计算和嵌入式场景，提供更多新特性和功能，给开发者和用户带来全新的体验，服务更多的领域和更多的用户。<br>


# Release Plan

| Stage  name          | Begin time | End time   | Days | Note                                      |
| -------------------- | ---------- | ---------- | ---- | ----------------------------------------- |
| Collect key features | 2022/4/15  | 2022/6/15 | 60   | 收集22.09版本关键特性（各SIG自行录入release-plan）   |
| Develop              | 2022/4/15  | 2022/7/31   | 105   | 特性完成开发和自验证，代码提交合入master    |
| Master Pre-build      | 2022/6/1  | 2022/6/30  | 30    | 审视Master构建工程，修复构建问题，为版本分支准备     |
| Branch 22.09 & Build   | 2022/7/5  | 2022/7/20   | 16    | 22.09版本从Master分支拉取（版本范围的包），构建版本 |
| Kernel freezing    | 2022/7/16   | 2022/7/20  | 15   | 内核代码冻结，管控合入   |
| Alpha        | 2022/7/21   | 2022/7/31  | 11    | 开发自验证              |
| Test round 1         | 2022/8/1 | 2022/8/7 | 7    | 版本启动测试                           |
| Test round 2         | 2022/8/11 | 2022/8/17 | 7    | 版本全量集成测试                         |
| Test round 3         | 2022/8/23 | 2022/8/29  | 7    |  版本分支代码冻结：管控合入，原则上只允许bug fix   |
| Test round 4         | 2022/9/2  | 2022/9/8 | 7    |   回归测试      |
| Test round 5         | 2022/9/12 | 2022/9/18 | 7    |  回归测试 (9.20~9.29预留buffer)     |
| Release              | 2022/9/30 | 2022/9/30 | 1    |                                           |


# 代码合入说明
创新版本代码继承master分支 <br>
// 新特性代码请及时合入版本&自验证，跟随整体计划赶在第一轮转测试


# Feature list
状态说明：Discussion(方案讨论，需求未接受)、 Developing(开发中)、 Testing(测试中)、 Accepted(已验收) <br>
发布方式：ISO、EPOL、oepkgs、独立发布等

|no|feature|status|sig|owner|发布方式|涉及软件包列表|
|:----|:---|:---|:--|:----|:----|:----|
|[I5BIHV](https://gitee.com/openeuler/release-management/issues/I5BIHV)|支持OpenStack Yoga版本，并且引入Helm组件|Discussion|SIG-OpenStack|[@joec88](https://gitee.com/joec88) [@huangtianhua](https://gitee.com/huangtianhua) [@xiyuanwang](@https://gitee.com/xiyuanwang)  [@zh-f](https://gitee.com/zh-f)  [@liksh](https://gitee.com/liksh) [@zhangy1317](https://gitee.com/zhangy1317)|     |     |
|[I5BIM9](https://gitee.com/openeuler/release-management/issues/I5BIM9)|正式发布联通开源的OpenStack部署工具opensd，支持OpenStack基本部署|Discussion|SIG-OpenStack|[@joec88](https://gitee.com/joec88) [@huangtianhua](https://gitee.com/huangtianhua) [@xiyuanwang](@https://gitee.com/xiyuanwang)  [@zh-f](https://gitee.com/zh-f)  [@liksh](https://gitee.com/liksh) [@zhangy1317](https://gitee.com/zhangy1317)|     |     |
|[I5ASLE](https://gitee.com/openeuler/release-management/issues/I5ASLE?from=project-issue)|发布kiran-desktop 2.3版本|Discussion|sig-KIRAN-DESKTOP|[@tangjie02](https://gitee.com/tangjie02)|EPOL|kiran-cpanel-xxx,kiran-control-panel,kiran-qt5-integration,kiran-widgets-qt5|
|[I5BJ7W](https://gitee.com/openeuler/release-management/issues/I5BJ7W)|支持树莓派|Discussion|sig-RaspberryPi|[@woqidaideshi](https://gitee.com/woqidaideshi)|EPOL|raspberrypi-kernel,raspberrypi-firmware,raspberrypi-bluetooth,raspi-config,pigpio,raspberrypi-userland,raspberrypi-eeprom|

<br>
现启动版本需求/特性收集，欢迎各sig maintainer和社区开发者们积极反馈和交流，<br>
<br>

# 需求/特性反馈基本流程 <br />
1、开发者/sig在本贴的表格中填写要合入22.09的需求/特性，并同时填写需求issue及链接 （请在收集截止时间前提交）      <br>
2、申请在版本release management sig例会上评审需求 （owner或者SIG maintainer参会）
<br><br>
