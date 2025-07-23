# Version Info
openEuler 25.09 是基于6.6内核的创新版本（参见[版本生命周期](https://www.openeuler.org/zh/other/lifecycle/)），面向服务器、云、边缘计算和嵌入式场景，提供更多新特性和功能，给开发者和用户带来全新的体验，服务更多的领域和更多的用户。<br>


# Release Plan

| Stage Name                    | Deadline for PR | Begin Time | End Time   | Days | Note                                     |
| ----------------------------- | --------------- | ---------- | ---------  | ---- | ---------------------------------------- |
| Collect key features          |        -        | 2025/06/01 | 2025/07/30 | 60 | 版本需求收集                              |
| Change Review 1               |        -        | 2025/07/01 | 2025/08/13 | 44 | Review 软件包变更（升级/退役/淘汰）  |
| Herited features              |        -        | 2025/07/01 | 2025/08/13 | 44 | 继承特性合入（Beta前完成合入） |
| Develop                       |        -        | 2025/07/01 | 2025/09/03 | 65 | 新特性开发，Branch前合入Master，Branch后合入Master+25.09(round 6冻结前合入) |
| Kernel freezing               |        -        | 2025/07/01 | 2025/08/13 | 44 | 内核冻结（随Beta版本，内核冻结） |
| Branch 25.09                  |        -        | 2025/07/16 | 2025/07/22 | 07 | Master 拉取 25.09 分支|
| Build & Alpha                 |    2025/07/23   | 2025/07/25 | 2025/07/31 | 07 | 新开发特性合入，Alpha版本发布    |
| Test round 1                  |    2025/07/30   | 2025/08/01 | 2025/08/07 | 07 | 25.09 模块测试（重点关注软件选型&构建问题）    |
| Test round 2                  |    2025/08/06   | 2025/08/08 | 2025/08/14 | 07 | 25.09 模块测试           |
| Test round 3 (Beta Version)   |    2025/08/13   | 2025/08/15 | 2025/08/21 | 07 | 25.09 Beta版本发布（KABI基线）    |
| Change Review 2               |        -        | 2025/08/15 | 2025/08/20 | 06 | 发起软件包淘汰评审 |
| Test round 4                  |    2025/08/20   | 2025/08/22 | 2025/08/28 | 07 | 25.09 模块测试       |
| Test round 5                  |    2025/08/27   | 2025/08/29 | 2025/09/04 | 07 | 全量验证(全量SIT)  |
| Change Review 3               |        -        | 2025/08/29 | 2020/09/03 | 06 | 发起软件包淘汰评审      |
| Test round 6                  |    2025/09/03   | 2025/09/05 | 2025/09/11 | 07 | 分支冻结，只允许bug fix          |
| Test round 7                  |    2025/09/10   | 2025/09/12 | 2025/09/18 | 07 | 回归测试                         |
| Test round 8 (预留)           |    2025/09/17   | 2025/09/19 | 2019/09/24 | 06 | 回归测试                         |
| Release Review                |        -        | 2025/09/22 | 2025/09/26 | 05 | 版本发布决策/ Go or No Go        |
| Release preparation           |        -        | 2025/09/24 | 2025/09/26 | 03 | 发布前准备阶段，发布件系统梳理    |
| Release                       |        -        | 2025/09/28 | 2025/09/30 | 03 | 社区Release评审通过正式发布       |

* ```Deadline for PR```: 构建启动(即PR停止接收构建)时间，当天晚8点后启动构建；
* ```Begin Time```: 转测开始时间，即在当天早9点前，完成转测镜像的构建、AT冒烟及发布；
* ```End Time```: 转测结束时间，下一轮 ```Begin Time``` -1天，测试团队需完成本轮次所有问题的提交;


# 代码合入说明
创新版本代码继承master分支 <br>
// 新特性代码请及时合入版本&自验证，跟随整体计划赶在第一轮转测试


# Feature list
状态说明：Discussion(方案讨论，需求未接受)、 Developing(开发中)、 Testing(测试中)、 Accepted(已验收) <br>
发布方式：ISO、Everything、EPOL、oepkgs、独立发布等

|no|feature|status|sig|owner|发布方式|涉及软件包列表|
|:----|:---|:---|:--|:----|:----|:----|
|[ICKOE7](https://gitee.com/openeuler/release-management/issues/ICKOE7?from=project-issue)|  GTA远程证明支持VirtCCA | Developing | sig-security-facility | [ @yang8621 ](https://gitee.com/yang8621) |ISO| global-trust-authority、secGear|
|[ICM8OF](https://gitee.com/openeuler/release-management/issues/ICM8OF)|以 valkey 取代 redis 作为首选的内存数据库|Developing|DB|[@fundawang](https://gitee.com/fundawang)|Everything|valkey|
| [ICMV3X](https://gitee.com/openeuler/release-management/issues/ICMV3X) | 支持树莓派 | Developing | sig-SBC | [@woqidaideshi](https://gitee.com/woqidaideshi/) | EPOL | raspberrypi-firmware,raspberrypi-bluetooth,raspi-config,pigpio,raspberrypi-userland,raspberrypi-eeprom,raspberrypi-utils |
| [ICOAHM](https://gitee.com/openeuler/release-management/issues/ICOAHM) | kuasar机密容器低底噪，高性能 | Developing | sig-CloudNative | [@liuxu180400617](https://gitee.com/liuxu180400617/) | Everything | kuasar |

# 需求/特性反馈基本流程 <br />
1、开发者/sig在本贴的表格中填写要合入该版本的需求/特性，并同时填写需求issue及链接 （请在收集截止时间前提交）      <br>
2、申请在版本release management sig例会上评审需求 （owner或者SIG maintainer参会）
<br><br>
