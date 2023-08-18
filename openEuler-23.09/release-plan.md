# Version Info
openEuler 23.09 是基于6.4内核的创新版本（参见[版本生命周期](https://www.openeuler.org/zh/other/lifecycle/)），面向服务器、云、边缘计算和嵌入式场景，提供更多新特性和功能，给开发者和用户带来全新的体验，服务更多的领域和更多的用户。<br>


# Release Plan

| Stage  name          | Begin time | End time   | Days | Note                                      |
| -------------------- | ---------- | ---------- | ---- | ----------------------------------------- |
| Collect key features | 2023/6/21      | 2023/7/20    | 30       | 收集23.09版本关键特性（各SIG自行录入release-plan）    |
| Develop              | 2023/6/26      | 2023/8/25    | 60       | 特性完成开发和自验证，代码提交合入23.09               |
| 内核升级             | 2023/6/26      | 2023/7/7     | 10       | master主线升级内核到6.4                               |
| BaseOS构建           | 2023/7/10      | 2023/7/21    | 10       | Master主线BaseOS构建，基础包能用                      |
| BaseOS测试           | 2023/7/24      | 2023/7/28    | 5        | 内核升级后BaseOS可用                                  |
| 分支全量Build        | 2023/7/31      | 2023/8/11    | 10       | 从master拉23.09分支，完成分支全量构建，基础包升级完毕 |
| Alpha                | 2023/8/14      | 2023/8/18    | 5        | 软件包升级完成，首版本发布                            |
| Test round 1         | 2023/8/21      | 2023/8/25    | 5        | 版本启动测试，内核冻结                                |
| Test round 2         | 2023/8/28      | 2023/9/1     | 5        |                                                       |
| Test round 3         | 2023/9/4       | 2023/9/8     | 5        | 特性合入冻结，不再接纳新特性代码合入                  |
| Test round 4         | 2023/9/11      | 2023/9/15    | 5        |                                                       |
| Test round 5         | 2023/9/18      | 2023/9/22    | 5        |                                                       |
| Release              | 2023/9/28      | 2023/9/28    | 1        |                                                       |


# 代码合入说明
创新版本代码继承master分支 <br>
// 新特性代码请及时合入版本&自验证，跟随整体计划赶在第一轮转测试


# Feature list
状态说明：Discussion(方案讨论，需求未接受)、 Developing(开发中)、 Testing(测试中)、 Accepted(已验收) <br>
发布方式：ISO、EPOL、oepkgs、独立发布等

|no|feature|status|sig|owner|发布方式|涉及软件包列表|
|:----|:---|:---|:--|:----|:----|:----|
|[I7GRO2](https://gitee.com/openeuler/release-management/issues/I7GRO2)|增加 utshell 项目发布|discussion|sig-utshell|[@tong2357](https://gitee.com/tong2357/)|EPOL|utshell|
|[I7GYQK](https://gitee.com/openeuler/release-management/issues/I7GYQK)|增加 utsudo 项目发布|discussion|sig-utsudo|[@ut-wanglujun](https://gitee.com/ut-wanglujun/)|EPOL|utsudo|
|[I7HXX2](https://gitee.com/openeuler/release-management/issues/I7HXX2)|增加 migration-tools 项目发布|discussion|sig-migration-tools|[@xingwei-liu](https://gitee.com/xingwei-liu/)|EPOL|migration-tools|
|[I7K7FQ](https://gitee.com/openeuler/release-management/issues/I7K7FQ)|DDE组件更新支持服务器场景优化|Testing|sig-DDE|[@leeffo](https://gitee.com/leeffo)|EPOL||
|[I7INU0](https://gitee.com/openeuler/release-management/issues/I7INU0?from=project-issue)|增加 Kmesh 项目发布|Developing|sig-ebpf|[@sky](https://gitee.com/nlgwcy)|extras|Kmesh|
|[I7K5TZ](https://gitee.com/openeuler/release-management/issues/I7K5TZ)|增加i3相关软件包发布|Developing|sig-epol|[@mywaaagh_admin](https://gitee.com/mywaaagh_admin)|EPOL|i3,i3status,perl-AnyEvent-I3,perl-AnyEvent,xcb-util-xrm,xcompmgr,perl-IO-Pipely,perl-Guard,perl-Glib,perl-Curses,dmenu,perl-Task-Weaken,perl-POE-Test-Loops,perl-Test-Command|
|[I7L1TT](https://gitee.com/openeuler/release-management/issues/I7L1TT)|A-Ops gala发布精细化性能Profiling特性|Developing|sig-ops|[@Vchanger](https://gitee.com/Vchanger)|ISO|gala-gopher|
|[I7K9ZJ](https://gitee.com/openeuler/release-management/issues/I7K9ZJ?from=project-issue)|增加DPU-OS镜像发布|Discussion|sig-DPU|[@minknov](https://gitee.com/minknov)|ISO|dpu-utilities|
|[I7MAWT](https://gitee.com/openeuler/release-management/issues/I7MAWT)|Aops支持配置溯源功能|Discussion|sig-ops|[@byrobins](https://gitee.com/byrobins)|EPOL|A-Ops,aops-hermes,aops-zeus,aops-ceres|
|[I7K7I7](https://gitee.com/openeuler/release-management/issues/I7K7I7)|sysMaster支持虚机场景|Discussion|dev-utils|[@overweight](https://gitee.com/overweight)|ISO|sysmaster|
|[I7PNTH](https://gitee.com/openeuler/release-management/issues/I7PNTH)|增加异构通用内存管理框架（GMEM）特性发布|Developing|sig-kernel,sig-Computing|[@fangchuang](https://gitee.com/fangchuang),[@weixizhu94](https://gitee.com/weixizhu94)|ISO|kernel,libgmem|
|[I7MR9U](https://gitee.com/openeuler/release-management/issues/I7MR9U?from=project-issue)|增加RISC-V架构QEMU镜像|Developing|sig-RISC-V|[@phoebe-xi](https://gitee.com/phoebe-xi)|ISO||
|[I7LQ45](https://gitee.com/openeuler/release-management/issues/I7LQ45?from=project-issue)|增加进程完整性防护特性|Developing|sig-security-facility|[@jinlun123123](https://gitee.com/jinlun123123)|ISO|dim,dim-tools|
|[I7LPVO](https://gitee.com/openeuler/release-management/issues/I7LPVO?from=project-issue)|Kuasar 统一容器运行时特性|Developing|SIG-CloudNative|[@flyflyflypeng](https://gitee.com/flyflyflypeng)|ISO|kuasar,iSulad|
|[I7L1TM](https://gitee.com/openeuler/release-management/issues/I7L1TM?from=project-issue)|A-Ops gala支持K8S Pod全栈可观测及诊断|Developing|sig-ops|[@Vchanger](https://gitee.com/Vchanger)|ISO|gala-gopher|
|[I7KXN5](https://gitee.com/openeuler/release-management/issues/I7KXN5?from=project-issue)|syscare组件支持容器化热补丁制作场景|Developing|sig-ops|[@RenoSeven](https://gitee.com/RenoSeven)|ISO|syscare|
|[I7KXLQ](https://gitee.com/openeuler/release-management/issues/I7KXLQ?from=project-issue)|syscare支持容器内补丁制作|Developing|sig-ops|[@RenoSeven](https://gitee.com/RenoSeven)|ISO|syscare|
|[I7G3JV](https://gitee.com/openeuler/release-management/issues/I7G3JV?from=project-issue)|增加sysBoost项目发布|Developing|atune-sig|[@ironictwist](https://gitee.com/ironictwist)|ISO|sysboost|
|[I7FB2R](https://gitee.com/openeuler/release-management/issues/I7FB2R?from=project-issue)|增加CTinspector项目发布|Developing|ebpf-sig|[@wonleing](https://gitee.com/wonleing)|ISO|CTinspector|
|[I6V32Y](https://gitee.com/openeuler/kernel/issues/I6V32Y?from=project-issue)|openEuler-22.03-SP2继承需求回合（内核）|Developing|kernel|[@stkid](https://gitee.com/stkid)|ISO|kernel|
|[I7RPQG](https://gitee.com/openeuler/release-management/issues/I7RPQG?from=project-issue)|继承特性回合|Developing|相关sig组|[@sujinling](https://gitee.com/sujinling)|ISO||
|[I7RPOW](https://gitee.com/openeuler/release-management/issues/I7RPOW?from=project-issue)|软件包升级适配|Developing|相关sig组|[@sujinling](https://gitee.com/sujinling)|ISO||
|[I6V436](https://gitee.com/openeuler/kernel/issues/I6V436?from=project-issue)|内核基线版本升级到v6.4 Release|Developing|kernel|[@stkid](https://gitee.com/stkid)|ISO|kernel|
|[I7TYZ8](https://gitee.com/openeuler/release-management/issues/I7TYZ8)|支持embedded|Developing|sig-embedded|[@fanglinxu](https://gitee.com/fanglinxu)|img|sig-embedded|

<br>
现启动版本需求/特性收集，欢迎各sig maintainer和社区开发者们积极反馈和交流，<br>
<br>



# 需求/特性反馈基本流程 <br />
1、开发者/sig在本贴的表格中填写要合入23.09的需求/特性，并同时填写需求issue及链接 （请在收集截止时间前提交）      <br>
2、申请在版本release management sig例会上评审需求 （owner或者SIG maintainer参会）
<br><br>
