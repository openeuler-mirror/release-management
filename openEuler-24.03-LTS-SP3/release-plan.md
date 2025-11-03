# Version Info
openEuler 24.03 LTS SP3 是基于6.6内核的LTS版本（参见[版本生命周期](https://www.openeuler.org/zh/other/lifecycle/)），面向服务器、云、边缘计算和嵌入式场景，提供更多新特性和功能，给开发者和用户带来全新的体验，服务更多的领域和更多的用户。<br>


# Release Plan
| Stage Name                  | Deadline for PR | Begin Time | End Time   | Days |     Notes                                        |
|-----------------------------|-----------------|------------|------------|------|-------------------------------------------       |
| Collect key features        | -               | 2025/9/1   | 2025/10/30 | 60   | 版本需求收集                                      |
| Change Review 1             | -               | 2025/10/1  | 2025/11/6  | 37   | Review 软件包变更（升级）SP版本尽可能保持版本不变   |
| Herited features            | -               | 2025/10/1  | 2025/10/29 | 29   | 继承特性合入（Branch前完成合入）                   |
| Develop                     | -               | 2025/10/1  | 2025/12/4  | 65   | 新特性开发，合入24.03 LTS Next                    |
| Kernel freezing             | -               | 2025/10/1  | 2025/11/5  | 36   | 内核冻结，KABI稳定                                |
| Next Build                  | -               | 2025/10/1  | 2025/10/16 | 16   | 启动新版本构建，新开发特性合入                      |
| Branch                      | -               | 2025/9/29  | 2025/10/14 | 16   | 24.03 LTS Next 拉取 24.03 LTS SP3 分支            |
| Alpha                       |                 | 2025/10/17 | 2025/10/23 | 7    | Alpha版本发布，24.03 LTS SP3开发者测试             |
| Test round 1                | 2025/10/22      | 2025/10/24 | 2025/10/30 | 7    | 24.03 LTS SP3模块测试                             |
| Test round 2                | 2025/10/29      | 2025/10/31 | 2025/11/6  | 7    | 24.03 LTS SP3 模块测试                            |
| Change Review 2             |                 | 2025/11/3  | 2025/11/6  | 4    | 发起软件包淘汰评审                                 |
| Test round 3 (Beta Version) | 2025/11/5       | 2025/11/7  | 2025/11/13 | 7    | 24.03 LTS SP3 Beta版本发布，24.03 LTS SP3 模块测试 |
| Test round 4                | 2025/11/12      | 2025/11/14 | 2025/11/20 | 7    | 24.03 LTS SP3 模块测试                            |
| Test round 5                | 2025/11/19      | 2025/11/21 | 2025/11/27 | 7    | 24.03 LTS SP3 模块测试                            |
| Test round 6                | 2025/11/26      | 2025/11/28 | 2025/12/4  | 7    | 24.03 LTS SP3 模块测试                            |
| Change Review 3             |                 | 2025/12/2  | 2025/12/4  | 3    | 确定软件包发布范围                                 |
| Test round 7                | 2025/12/3       | 2025/12/5  | 2025/12/11 | 7    | 全量验证(全量SIT)                                 |
| Test round 8                | 2025/12/10      | 2025/12/12 | 2025/12/18 | 7    | 回归测试，分支冻结，只允许bug fix                  |
| Test round 9                | 2025/12/17      | 2025/12/19 | 2025/12/25 | 7    | 回归测试                                          |
| Release Review              | -               | 2025/12/25 | 2025/12/26 | 2    | 版本发布决策/ Go or No Go                         |
| Release preparation         | -               | 2025/12/20 | 2025/12/29 | 10   | 发布前准备阶段，发布件系统梳理                      |
| Release                     | -               | 2025/12/30 | 2025/12/31 | 2    | 社区Release评审通过正式发布                        |


# 代码合入说明
创新版本代码继承master分支 <br>
// 新特性代码请及时合入版本&自验证，跟随整体计划赶在第一轮转测试


# Feature list
状态说明：Discussion(方案讨论，需求未接受)、 Developing(开发中)、 Testing(测试中)、 Accepted(已验收) <br>
发布方式：ISO、Everything、EPOL、oepkgs、独立发布等

|no|feature|status|sig|owner|发布方式|涉及软件包列表|
|:----|:---|:---|:--|:----|:----|:----|
|1|[isa-l库：CRC算法在RISC-V架构的优化](https://gitee.com/openeuler/release-management/issues/ICW20J?from=project-issue)|Accepted|dev-utils|@qtliu666|EPOL|isa-l|
|2|[snappy库：FindMatchLength支持RISC-V架构的优化](https://gitee.com/openeuler/release-management/issues/ICW4C5?from=project-issue)|Accepted|Base-service| @QingtaoLiu |ISO|snappy|
|3|[lz4库：提高riscv架构的压缩速度](https://gitee.com/openeuler/release-management/issues/ICWGMF?from=project-issue)|Testing|Base-service|@QingtaoLiu|EPOL|ISO|
|4|[openssl库：RISC-V架构的系列优化-SM2优化](https://gitee.com/openeuler/release-management/issues/ICW5SK?from=project-issue)|Testing|dev-utils|@QingtaoLiu|ISO|openssl|
|5|[virtcca: 支持virtCCA机密虚机热迁移](https://gitee.com/openeuler/release-management/issues/ID1Y44?from=project-issue)|Discussion|kernel,virt|@hjx_gitff|ISO|kernel,qemu|
|6|[golang: Backport RVA23 支持](https://gitee.com/openeuler/release-management/issues/ID2QHV?from=project-issue)|Testing|sig-golang|@HeliC829|OS|golang|
|7|[TSB-agent: 支持可信计算虚拟化vTPCM](https://gitee.com/openeuler/release-management/issues/ID3BZ8?from=project-issue)|Accepted|sig-security-facility|@cx22757|EPOL| virtrust-sh,libvirtrust,libvirtrustd |
|8|[openssl：Backport 主线 RISC-V 架构的 SHA-2 汇编优化](https://gitee.com/openeuler/release-management/issues/ID3WE6?from=project-issue)|Testing|dev-utils|@HeliC829|ISO|openssl|
|9|[URMA：URMA支持UB基础通信能力](https://gitee.com/openeuler/release-management/issues/ID3WJX?from=project-issue)|Developing|sig-UnifiedBus|@qianguoxin|ISO|liburma,libubagg,urma-tools,uvs|
|10|[UMS：UMS支持socket接口通信](https://gitee.com/openeuler/release-management/issues/ID3WK9?from=project-issue)|Developing|sig-UnifiedBus|@jillwu|ISO|ums,ums-tools|
|11|[DLock：支持基于UB的分布式锁](https://gitee.com/openeuler/release-management/issues/ID3WJY?from=project-issue)|Developing|sig-UnifiedBus|@jillwu|ISO|libdlock|
|12|[URPC：URPC支持UB](https://gitee.com/openeuler/release-management/issues/ID3WJO?from=project-issue)|Developing|sig-UnifiedBus|@nemeiju|ISO|liburpc|
|13|[UBTurbo: HAM支持确定性热迁移能力](https://gitee.com/openeuler/release-management/issues/ID42J5?from=project-issue)|Developing|sig-UnifiedBus|@leeCii|ISO|libham|
|14|[UBTurbo： SMAP支持内存冷热扫描和迁移能力](https://gitee.com/openeuler/release-management/issues/ID40VW?from=project-issue)|Developing|sig-UnifiedBus|@leeCii|ISO|libsmap|
|15|[UBTurbo：RMRS Agent支持内存迁移决策与执行](https://gitee.com/openeuler/release-management/issues/ID42GJ?from=project-issue)|Developing|sig-UnifiedBus|@meng_zhaohui|ISO|librmrs_ub_turbo_plugin|
|16|[UB Turbo： UBTurbo提供基础框架(配置读取、插件加载、日志管理、IPC通信等)能力](https://gitee.com/openeuler/release-management/issues/ID42G7?from=project-issue)|Developing|sig-UnifiedBus|@meng_zhaohui|ISO|ub_turbo,libubturbo_client|
|17|[UBS Engine: UBS Engine支持UB池化资源管理能力](https://gitee.com/openeuler/release-management/issues/ID4155?from=project-issue)|Developing|sig-UB-ServiceCore|@xuchenfengcleancode|ISO|libubse_client,ubse,ubsectl|
|18|[UBS Comm: HCOM支持UB通信能力](https://gitee.com/openeuler/release-management/issues/ID40GU?from=project-issue)|Developing|sig-UB-ServiceCore|@fanzhaonan|ISO|libhcom|
|19|[OBMM: 提供跨节点内存访问与一致性控制能力](https://gitee.com/openeuler/release-management/issues/ID45O2?from=project-issue)|Developing|sig-Long|@kazero00|ISO|kernel,libobmm|
|20|[sysSentry：支持UB故障劫持能力及超节点故障上报能力](https://gitee.com/openeuler/release-management/issues/ID45WQ?from=project-issue)|Developing|Base-service|@luckky7|ISO|kernel,sysSentry|
|21|[qemu：支持基于urma通道的内存热迁移](https://gitee.com/openeuler/release-management/issues/ID49H5)|Developing|Virt|@eillon|ISO|qemu,libvirt|
|22|[UBNative：灵衢虚拟化基础能力支持UBNative直通虚拟化](https://gitee.com/openeuler/release-management/issues/ID49MB)|Developing|Virt|@caojinhuahw|ISO|qemu,libvirt|
|23|[memlink：灵衢虚拟化基础能力支持memlink大规格虚拟机、内存回收](https://gitee.com/openeuler/release-management/issues/ID49LF)|Developing|sig-long|@leizongkun|ISO|memlink|
|24|[utpam：基于Rust开发的身份认证模块](https://gitee.com/openeuler/release-management/issues/ID4CRS)|Developing|sig-memsafety|@trackers-love|ISO|utpam|

# 需求/特性反馈基本流程 <br />
1、开发者/sig在本贴的表格中填写要合入该版本的需求/特性，并同时填写需求issue及链接 （请在收集截止时间前提交）      <br>
2、申请在版本release management sig例会上评审需求 （owner或者SIG maintainer参会）
<br><br>
