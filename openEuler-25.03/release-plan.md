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
| Branch 25.03                  |        -        | 2025/1/23  | 2025/2/6   | 7  | Master 拉取 25.03 分支 (跨春节，预祝开发者春节快乐) |
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
| :--- | :------ | :----- | :--- | :---- | :--- | :---- |
|[IBGAHV](https://gitee.com/openeuler/release-management/issues/IBGAHV?from=project-issue)| 为AArch64编译默认开启PAC/BTI | Discussion | sig-Arm | [@junhe_arm](https://gitee.com/junhe_arm) |
|[IBJFPX](https://gitee.com/openeuler/release-management/issues/IBJFPX)| 支持树莓派 | Discussion | sig-SBC | [@woqidaideshi](https://gitee.com/woqidaideshi/) |
|[IBLBJ2](https://gitee.com/openeuler/release-management/issues/IBLBJ2?from=project-issue)| Aops: cve修复/配置溯源实现运维智能化，支持主动通知和图文混合交互 | Developing|sig-ops | [@Lostwayzxc](https://gitee.com/Lostwayzxc/) |
|[IBLB8F](https://gitee.com/openeuler/release-management/issues/IBLB8F?from=project-issue)| 基于sysboost实现启动时优化，通用兼容性增强 | Developing| sig-Compiler | [@wangding16](https://gitee.com/wangding16/) |
|[IBLB3B](https://gitee.com/openeuler/release-management/issues/IBLB3B?from=project-issue)| GCC for openEuler编译链接加速，缩减编译时间 | Developing| sig-Compiler | [@wangding16](https://gitee.com/wangding16/) |
|[IBLA9W](https://gitee.com/openeuler/release-management/issues/IBLA9W?from=project-issue)| 机密容器Kuasar适配virtCCA | Developing| sig-CloudNative | [@xuxuepeng](https://gitee.com/xuxuepeng/) |
|[IBLA6Q](https://gitee.com/openeuler/release-management/issues/IBLA6Q?from=project-issue)| secGear支持机密容器镜像密钥托管 | Developing|sig-security-facility | [@houmingyong](https://gitee.com/houmingyong/) |
|[IBLA66](https://gitee.com/openeuler/release-management/issues/IBLA66?from=project-issue)| 构建基于远程证明的TLS协议（RA-TLS） | Developing|sig-security-facility | [@houmingyong](https://gitee.com/houmingyong/) |
|[IBK2MJ](https://gitee.com/openeuler/release-management/issues/IBK2MJ?from=project-issue)| Trace IO加速容器快速启动 | Developing|| sig-Kernel| [@hongbo-lee](https://gitee.com/hongbo-lee/) |
|[IBJ7WU](https://gitee.com/openeuler/release-management/issues/IBJ7WU?from=project-issue)| 默认系统集成 liteview，代替 firefox | Discussion | sig-Desktop | [@shinwell_hu](https://gitee.com/shinwell_hu/) |
|[IBD46F](https://gitee.com/openeuler/kernel/issues/IBD46F)| 引入vkernel概念增强容器隔离能力 | Developing|| sig-Kernel | [@joyallen](https://gitee.com/joyallen/) |
|[IBC4SJ](https://gitee.com/openeuler/kernel/issues/IBC4SJ)| uncore动态调频 | Developing|| sig-Kernel | [@li-wei2110](https://gitee.com/li-wei2110/) |
|[IBI0TX](https://gitee.com/openeuler/release-management/issues/IBI0TX?from=project-issue)| openAMDC合入 | Developing|| sig-BigData | [@changzhi1123](https://gitee.com/changzhi1123/) |
|[IBFDJ9](https://gitee.com/openeuler/release-management/issues/IBFDJ9?from=project-issue)| oncn-bwm支持host network 类型pod的带宽管理 | Developing | sig-high-performance-network | [@supercharge](https://gitee.com/supercharge/) |
|[IBLJRD](https://gitee.com/openeuler/release-management/issues/IBLJRD?from=project-issue)| oeAware支持瓶颈评估一键推荐调优等特性增强 | Developing | sig-A-Tune | [@Lostwayzxc](https://gitee.com/Lostwayzxc/) |
|[IBLJWU](https://gitee.com/openeuler/release-management/issues/IBLJWU?from=project-issue)| oeDeploy 部署能力增强 | Developing | sig-ops | [@dingjiahuichina](https://gitee.com/dingjiahuichina/) |
|[IBLKJY](https://gitee.com/openeuler/release-management/issues/IBLKJY?from=project-issue)| 主流工业中间件支持 | Developing | sig-embedded| [@Lostwayzxc](https://gitee.com/Lostwayzxc/) |
|[IBLKHB](https://gitee.com/openeuler/release-management/issues/IBLKHB?from=project-issue)| 跨域通信框架，支持接口调用跨域通信 | Developing | sig-embedded| [@Lostwayzxc](https://gitee.com/Lostwayzxc/) |
|[IBLKF9](https://gitee.com/openeuler/release-management/issues/IBLKF9?from=project-issue)| 虚拟化底座，使能XEN虚拟化框架 | Developing | sig-embedded| [@Lostwayzxc](https://gitee.com/Lostwayzxc/) |
|[IBLJWU](https://gitee.com/openeuler/release-management/issues/IBLJWU?from=project-issue)| 硬实时南向生态：EtherCAT支持 | Developing | sig-embedded| [@hzc04](https://gitee.com/hzc04/) |
|[IBLKCQ](https://gitee.com/openeuler/release-management/issues/IBLKCQ?from=project-issue)| 嵌入式：硬实时POSIX接口补齐 | Developing | sig-embedded | [@hzc04](https://gitee.com/hzc04/) |
|[IBLK62](https://gitee.com/openeuler/release-management/issues/IBLK62?from=project-issue)| DevStation社区原生/图形化/南向兼容性等新增特性 | Developing |sig-ops/IDE | [@duan_pj](https://gitee.com/duan_pj/) |
|[IBLK0E](https://gitee.com/openeuler/release-management/issues/IBLK0E?from=project-issue)|  EPKG包管理器优化，提升epkg易用性 | Developing |sig-CICD | [@duan_pj](https://gitee.com/duan_pj/) |
|[IBLJWU](https://gitee.com/openeuler/release-management/issues/IBLJWU?from=project-issue)| oeDeploy 部署能力增强 | Developing |sig-ops | [@dingjiahuichina](https://gitee.com/dingjiahuichina/) |
|[IBLJRD](https://gitee.com/openeuler/release-management/issues/IBLJRD?from=project-issue)| oeAware支持瓶颈评估一键推荐调优等特性增强 | Developing |sig-A-Tune | [@Lostwayzxc](https://gitee.com/Lostwayzxc/) |


# 需求/特性反馈基本流程 <br />
1、开发者/sig在本贴的表格中填写要合入23.03的需求/特性，并同时填写需求issue及链接 （请在收集截止时间前提交）      <br>
2、申请在版本release management sig例会上评审需求 （owner或者SIG maintainer参会）
<br><br>
