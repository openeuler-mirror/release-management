# Version Info

openEuler 24.03 LTS SP4 是基于6.6内核的LTS版本（参见[版本生命周期](https://www.openeuler.org/zh/other/lifecycle/)），面向服务器、云、边缘计算、嵌入式和超节点场景，提供更多新特性和功能，给开发者和用户带来全新的体验，服务更多的领域和更多的用户。

# Release Plan

| Stage Name                  | Deadline for PR | Begin Time | End Time  | Days | Notes                              |
| --------------------------- | --------------- | ---------- | --------- | ---- | ---------------------------------- |
| Collect key features        | -               | 2026/3/23  | 2026/4/30 | 39   | 版本需求收集                             |
| Change Review 1             | -               | 2026/4/1   | 2026/5/8  | 38   | Review 软件包变更（升级）SP版本尽可能保持版本不变      |
| Herited features            | -               | 2026/3/20  | 2026/4/10 | 22   | 继承特性合入（Branch前完成合入）                |
| Develop                     | -               | 2026/4/1   | 2026/6/6  | 67   | 新特性开发，合入24.03 LTS Next+SP4分支       |
| Kernel freezing             | -               | 2026/4/1   | 2026/5/8  | 38   | 内核冻结，KABI稳定                        |
| Branch                      | <br />          | 2026/3/27  | 2026/4/10 | 15   | 24.03 LTS Next 拉取 24.03 LTS SP4 分支 |
| Next Build                  | -               | 2026/4/4   | 2026/4/10 | 7    | 启动新版本构建，新开发特性合入                    |
| Alpha                       | 2026/4/8        | 2026/4/11  | 2026/4/17 | 7    | Alpha版本发布，24.03 LTS SP4 开发者测试      |
| Test round 1                | 2026/4/15       | 2026/4/18  | 2026/4/24 | 7    | 24.03 LTS SP4 模块测试                 |
| Test round 2                | 2026/4/22       | 2026/4/25  | 2026/5/8 | 6    | 24.03 LTS SP4 模块测试，五一劳动节快乐         |
| Change Review 2             | <br />          | 2026/5/6   | 2026/5/8  | 3    | 发起软件包淘汰评审                          |
| Test round 3 (Beta Version) | 2026/5/6       | 2026/5/9   | 2026/5/15 | 7    | 24.03 LTS SP4 模块测试                 |
| Test round 4                | 2026/5/13       | 2026/5/16  | 2026/5/22 | 7    | 24.03 LTS SP4 模块测试                 |
| Test round 5                | 2026/5/20       | 2026/5/23  | 2026/5/29 | 7    | 24.03 LTS SP4 模块测试                 |
| Test round 6                | 2026/5/27       | 2026/5/30  | 2026/6/5  | 7    | 24.03 LTS SP4 模块测试                 |
| Change Review 3             | <br />          | 2026/6/3   | 2026/6/5  | 3    | 确定软件包发布范围                          |
| Test round 7                | 2026/6/3        | 2026/6/6   | 2026/6/12 | 7    | 全量验证(全量SIT)，分支冻结，只允许bug fix        |
| Test round 8                | 2026/6/10       | 2026/6/13  | 2026/6/18 | 6    | 全量验证(全量SIT)，分支冻结，只允许bug fix        |
| Test round 9                | 2026/6/17       | 2026/6/22  | 2026/6/26 | 5    | 回归测试，只允许阻塞bug fix                  |
| Release Review              | -               | 2026/6/25  | 2026/6/26 | 2    | 版本发布决策/ Go or No Go                |
| Release preparation         | -               | 2026/6/22  | 2026/6/28 | 7    | 发布前准备阶段，发布件系统梳理                    |
| Release                     | -               | 2026/6/29  | 2026/6/30 | 2    | 社区Release评审通过正式发布                  |

# 代码合入说明

LTS SPX版本代码继承master分支&#x20;
// 新特性代码请及时合入版本&自验证，跟随整体计划赶在第一轮转测试

# Feature list

状态说明：Discussion(方案讨论，需求未接受)、 Developing(开发中)、 Testing(测试中)、 Accepted(已验收)&#x20;
发布方式：ISO、Everything、EPOL、oepkgs、独立发布等

| no                                                                   | feature                                                                        | status     | sig                   | owner                                         | 发布方式 | 涉及软件包列表                  |
| :------------------------------------------------------------------- | :----------------------------------------------------------------------------- | :--------- | :-------------------- | :-------------------------------------------- | :--- | :----------------------- |
| [2366](https://gitcode.com/openeuler/release-management/issues/2366) | 增加可信计算资源分发服务组件                                                                 | Developing | sig-security-facility | [@yang8621](https://gitcode.com/yang8621)     | EPOL | globaltrustauthority-rbs |
| [2434](https://gitcode.com/openeuler/release-management/issues/2434) | 远程证明支持DICE                                                                     | Developing | sig-security-facility | [@yang8621](https://gitcode.com/yang8621)     | EPOL | global-trust-authority   |
| [2441](https://atomgit.com/openeuler/release-management/issues/2441) | [海光ccp驱动升级，支持sm4-xts和sm4-gcm](https://atomgit.com/openeuler/kernel/pull/21130) | Developing | SIG-Kernel            | [@partycoder](https://atomgit.com/partycoder) | ISO  | kernel                   |
| [2442](https://atomgit.com/openeuler/release-management/issues/2442) | 新增海光CIS指令集sm3,sm4驱动                                                            | Developing | SIG-Kernel            | [@partycoder](https://atomgit.com/partycoder) | ISO  | kernel                   |
| [2448](https://atomgit.com/openeuler/release-management/issues/2448) | 支持树莓派 | Developing | sig-SBC | [@woqidaideshi](https://atomgit.com/woqidaideshi) | EPOL | raspberrypi-firmware,raspberrypi-bluetooth,raspi-config,pigpio,raspberrypi-userland,raspberrypi-eeprom,raspberrypi-utils |

# 需求/特性反馈基本流程&#x20;

1、开发者/sig在本贴的表格中填写要合入该版本的需求/特性，并同时填写需求issue及链接 （请在收集截止时间前提交）     &#x20;
2、申请在版本release management sig例会上评审需求 （owner或者SIG maintainer参会）
