# Version Info
openEuler 24.03 LTS SP2 是基于6.6内核的LTS版本（参见[版本生命周期](https://www.openeuler.org/zh/other/lifecycle/)），面向服务器、云、边缘计算和嵌入式场景，提供更多新特性和功能，给开发者和用户带来全新的体验，服务更多的领域和更多的用户。<br>


# Release Plan

| Stage Name                    | Deadline for PR | Begin Time | End Time   | Days | Note                                     |
| ----------------------------- | --------------- | ---------- | ---------  | ---- | ---------------------------------------- |
| Collect key features          |        -        | 20xx/xx/xx | 20xx/xx/xx | xx | 版本需求收集                              |
| Change Review 1               |        -        | 20xx/xx/xx | 20xx/xx/xx | xx | Review 软件包变更（升级/退役/淘汰）  |
| Herited features              |        -        | 20xx/xx/xx | 20xx/xx/xx | xx | 继承特性合入（Branch前完成合入） |
| Develop                       |        -        | 20xx/xx/xx | 20xx/xx/xx | xx | 新特性开发，合入Master |
| Kernel freezing               |        -        | 20xx/xx/xx | 20xx/xx/xx | xx | 内核冻结（随Beta版本，内核冻结） |
| Branch 24.03 LTS SP2          |        -        | 20xx/xx/xx | 20xx/xx/xx | xx | Master 拉取 24.03 LTS SP2 分支 (跨春节，预祝开发者春节快乐) |
| Build & Alpha                 |        -        | 20xx/xx/xx | 20xx/xx/xx | xx | 新开发特性合入，Alpha版本发布    |
| Test round 1                  |    20xx/xx/xx   | 20xx/xx/xx | 20xx/xx/xx | xx | 24.03 LTS SP2 模块测试           |
| Change Review 2               |        -        | 20xx/xx/xx | 20xx/xx/xx | xx | 发起软件包淘汰评审               |
| Test round 2 (Beta Version)   |    20xx/xx/xx   | 20xx/xx/xx | 20xx/xx/xx | xx | 24.03 LTS SP2 Beta版本发布       |
| Test round 3                  |    20xx/xx/xx   | 20xx/xx/xx | 20xx/xx/xx | xx | 全量验证(全量SIT)                |
| Change Review 3               |        -        | 20xx/xx/xx | 20xx/xx/xx | xx | 只允许bug fix      |
| Test round 4                  |    20xx/xx/xx   | 20xx/xx/xx | 20xx/xx/xx | xx | 分支冻结，只允许bug fix          |
| Test round 5                  |    20xx/xx/xx   | 20xx/xx/xx | 20xx/xx/xx | xx | 回归测试                         |
| Test round 6 (预留)           |    20xx/xx/xx   | 20xx/xx/xx | 20xx/xx/xx | xx | 回归测试                         |
| Release Review                |        -        | 20xx/xx/xx | 20xx/xx/xx | xx | 版本发布决策/ Go or No Go        |
| Release preparation           |        -        | 20xx/xx/xx | 20xx/xx/xx | xx | 发布前准备阶段，发布件系统梳理    |
| Release                       |        -        | 20xx/xx/xx | 20xx/xx/xx | xx | 社区Release评审通过正式发布       |



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


# 需求/特性反馈基本流程 <br />
1、开发者/sig在本贴的表格中填写要合入该版本的需求/特性，并同时填写需求issue及链接 （请在收集截止时间前提交）      <br>
2、申请在版本release management sig例会上评审需求 （owner或者SIG maintainer参会）
<br><br>
