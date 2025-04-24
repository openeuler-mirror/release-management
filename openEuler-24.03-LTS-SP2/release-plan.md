# Version Info
openEuler 24.03 LTS SP2 是基于6.6内核的LTS版本（参见[版本生命周期](https://www.openeuler.org/zh/other/lifecycle/)），面向服务器、云、边缘计算和嵌入式场景，提供更多新特性和功能，给开发者和用户带来全新的体验，服务更多的领域和更多的用户。<br>


# Release Plan
| Stage Name                    | Deadline for PR | Begin Time| End Time  | Days | Note                                     |
| ----------------------------- | --------------- | ----------| --------- | ---- | ---------------------------------------- |
| Collect key features          |        -        | 2025/3/1  | 2025/4/30 |  61  | 版本需求收集                              |
| Change Review 1               |        -        | 2025/4/1  | 2025/5/8  |  38  | Review 软件包变更（升级/退役/淘汰）        |
| Herited features              |        -        | 2025/4/1  | 2025/4/24 |  24  | 继承特性合入（Branch前完成合入）           |
| Develop                       |        -        | 2025/4/1  | 2025/5/27 |  57  | 新特性开发，合入24.03 LTS next            |
| Kernel freezing               |        -        | 2025/5/1  | 2025/5/8  |  8  | 内核冻结（随Beta版本，内核冻结）           |
| Next Build                    |        -        | 2025/4/1  | 2025/4/10 |  10  | 启动新版本构建，新开发特性合入             |
| Alpha                         |    2025/4/9     | 2025/4/11 | 2025/4/17 |  7   | 24.03 LTS SP2 模块测试                   |
| Test round 1                  |    2025/4/16    | 2025/4/18 | 2025/4/24 |  7   | 24.03 LTS SP2 模块测试                   |
| Branch                        |                 | 2025/4/18 | 2025/4/23 |  7   | 24.03 LTS Next 拉取 24.03 LTS SP2 分支   |
| Test round 2                  |    2025/4/23    | 2025/4/25 | 2025/5/8  |  14  | 24.03 LTS SP2 模块测试，五一劳动节快乐     |
| Change Review 2               |        -        | 2025/5/6  | 2025/5/8  |  3   | 发起软件包淘汰评审                        |
| Test round 3 (Beta Version)   |    2025/5/7     | 2025/5/9  | 2025/5/15 |  7   | 24.03 LTS SP2 Beta版本发布，24.03 LTS SP2 模块测试       |
| Test round 4                  |    2025/5/12    | 2025/5/16 | 2025/5/22 |  7   | 24.03 LTS SP2 模块测试                   |
| Test round 5                  |    2025/5/21    | 2025/5/23 | 2025/5/29 |  7   | 24.03 LTS SP2 模块测试                   |
| Test round 6                  |    2025/5/28    | 2025/5/30 | 2025/6/6  |  8   | 24.03 LTS SP2 模块测试，端午节快乐        | 
| Change Review 3               |        -        | 2025/6/3  | 2025/6/5  |  3   | 确定软件包发布范围                        |
| Test round 7                  |     2025/6/5    | 2025/6/7  | 2025/6/13 |  7   | 全量验证(全量SIT)                         |
| Test round 8                  |     2025/6/12   | 2025/6/14 | 2025/6/20 |  7   | 回归测试，分支冻结，只允许bug fix          |
| Test round 9                  |     2025/6/19   | 2025/6/21 | 2025/6/27 |  7   | 回归测试                                 |
| Release Review                |       -         | 2025/6/21 | 2025/6/22 |  2   | 版本发布决策/ Go or No Go                 |
| Release preparation           |       -         | 2025/6/20 | 2025/6/28 |  9   | 发布前准备阶段，发布件系统梳理              |
| Release                       |       -         | 2025/6/29 | 2025/6/30 |  2   | 社区Release评审通过正式发布                |   





# 代码合入说明
创新版本代码继承master分支 <br>
// 新特性代码请及时合入版本&自验证，跟随整体计划赶在第一轮转测试


# Feature list
状态说明：Discussion(方案讨论，需求未接受)、 Developing(开发中)、 Testing(测试中)、 Accepted(已验收) <br>
发布方式：ISO、Everything、EPOL、oepkgs、独立发布等

|no|feature|status|sig|owner|发布方式|涉及软件包列表|
|:----|:---|:---|:--|:----|:----|:----|
|IBXVC7|virtCCA机密虚机相关特性合入版本|Developing||SIG-Kernel/SIG-Virt|@luoyukai||
| [IBSO3U](https://gitee.com/openeuler/release-management/issues/IBSO3U?from=project-issue) | OVMF_CODE.fd支持CSV1/2/3开箱即用 | Developing| sig-kernel/sig-qemu/sig-libvirt/sig-edk2 | [@hanliyang](https://gitee.com/hanliyang) |
| [IBSO3U](https://gitee.com/openeuler/release-management/issues/IBSO3U?from=project-issue) | OVMF.fd支持CSV1/2/3开箱即用 | Developing| sig-kernel/sig-qemu/sig-libvirt/sig-edk2 | [@hanliyang](https://gitee.com/hanliyang) |
| [IBSO3U](https://gitee.com/openeuler/release-management/issues/IBSO3U?from=project-issue) | 支持CSV1/2/3直通DCU功能开箱即用 | Developing| sig-kernel/sig-qemu/sig-libvirt/sig-edk2 | [@hanliyang](https://gitee.com/hanliyang) |
| [IBSO3U](https://gitee.com/openeuler/release-management/issues/IBSO3U?from=project-issue) | 新的psp/ccp device id支持 | Developing| sig-kernel/sig-tpm2-tss/sig-tpm2-tools/sig-tpm2-abrmd | [@chench00](https://gitee.com/chench00) |
| [IBSO3U](https://gitee.com/openeuler/release-management/issues/IBSO3U?from=project-issue) | 可信功能内核驱动剥离sev依赖 | Developing| sig-kernel/sig-tpm2-tss/sig-tpm2-tools/sig-tpm2-abrmd | [@chench00](https://gitee.com/chench00) |
| [IBSO3U](https://gitee.com/openeuler/release-management/issues/IBSO3U?from=project-issue) | 海光4号美密支持，sm4-xts,sm4-gcm支持，avx/cis指令集接口支持 | Developing| sig-kernel | [@partycoder](https://gitee.com/partycoder) |
| [IBSO3U](https://gitee.com/openeuler/release-management/issues/IBSO3U?from=project-issue) | vTKM 性能优化 | Developing| sig-kernel | [@xisme](https://gitee.com/xisme) |
| [IBSO3U](https://gitee.com/openeuler/release-management/issues/IBSO3U?from=project-issue) | 需要合入bcache的bug fix | Developing| sig-kernel | [@geshifei-linux](https://gitee.com/geshifei-linux) |
| [IBSO3U](https://gitee.com/openeuler/release-management/issues/IBSO3U?from=project-issue) | 对hygon 8h DF PMU的适配 | Developing| sig-kernel | [@liuqi_77777](https://gitee.com/liuqi_77777) |
| [IBSO3U](https://gitee.com/openeuler/release-management/issues/IBSO3U?from=project-issue) | 代码段复制patch的适配 | Developing| sig-kernel | [@qiuzhiteng](https://gitee.com/qiuzhiteng) |
| [IBSO3U](https://gitee.com/openeuler/release-management/issues/IBSO3U?from=project-issue) | 需要合入海光分支patch和memset的nt patch | Developing| sig-kernel | [@jiamei01](https://gitee.com/jiamei01) |
|[IBZ9CK](https://gitee.com/openeuler/release-management/issues/IBZ9CK)|支持树莓派|Discussion|sig-SBC|[@woqidaideshi](https://gitee.com/woqidaideshi/)|EPOL|raspberrypi-firmware,raspberrypi-bluetooth,raspi-config,pigpio,raspberrypi-userland,raspberrypi-eeprom,raspberrypi-utils|
| [IC3KIG](https://gitee.com/openeuler/release-management/issues/IC3KIG) | 支持 OpenStack Antelope/Wallaby 版本 | Developing | sig-openstack | [@tzing_t](https://gitee.com/tzing_t) |



# 需求/特性反馈基本流程 <br />
1、开发者/sig在本贴的表格中填写要合入该版本的需求/特性，并同时填写需求issue及链接 （请在收集截止时间前提交）      <br>
2、申请在版本release management sig例会上评审需求 （owner或者SIG maintainer参会）
<br><br>
