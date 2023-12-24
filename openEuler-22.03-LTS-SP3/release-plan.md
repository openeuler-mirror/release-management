# Version Info
openEuler 22.03 LTS SP3 是22.03-LTS版本增强扩展版本（参见[版本生命周期](https://www.openeuler.org/zh/other/lifecycle/)），面向服务器、云、边缘计算和嵌入式场景，持续提供更多新特性和功能扩展，给开发者和用户带来全新的体验，服务更多的领域和更多的用户。<br>


# Release Plan

| Stage  name            | Begin time | End time   | Days | Note                                                       |
| --------------------   | ---------- | ---------- | ---- | -----------------------------------------                  |
| Collect key features   | 2023/9/7  | 2023/10/15 | 37   | 版本需求收集                                                |
| 变更检查阶段1           | 2023/10/8  | 2023/11/8  | 30   | Review软件包变更（升级/退役/淘汰）                            |
| 变更检查阶段2           | 2023/10/16 | 2023/10/16 | 1    | Review基础设施相关变更                                       |
| Develop                | 2023/10/8  | 2023/11/8  | 30   | 这个时间段内完成开发，合入22.03  LTS-Next                     |
| Kernel freezing        | 2023/11/3  | 2023/11/8  | 6    | 内核冻结                                                    |
| LTS-Next mass rebuild  | 2023/11/9  | 2023/11/10 | 2    | 22.03-LTS Next分支大规模编译构建                              |
| 变更检查阶段3           | 2023/11/11 | 2023/11/12 | 3    | 22.03-LTS Next分支发起软件包淘汰（持续编译/构建失败）评审        |
| Branch                 | 2023/11/13 | 2023/11/15 | 3    | 从22.03 LTS-Next拉SP3版本分支                                 |
| Build & Alpha          | 2023/11/16 | 2023/11/22 | 7    | 22.03-LTS SP3版本DailyBuild  & 开发自验证                      |
| Test round 1           | 2023/11/23 | 2023/11/29 | 7    | 22.03-LTS SP3版本启动集成测试                                  |
| 变更检查阶段4           | 2023/11/30 | 2023/11/30 | 1    | 22.03-LTS SP3版本分支发起软件包淘汰（持续编译/构建失败）评审      | 
| Beta Version release   | 2023/12/1  | 2023/12/2  | 2    | 22.03-LTS SP3 Beta版本发布                                    |
| Test round 2           | 2023/12/2  | 2023/12/8  | 7    | 全量SIT验证                                                   |
| 变更检查阶段5           | 2023/12/9  | 2023/12/9  | 1    | 22.03-LTS SP3版本分支代码冻结：受限合入，原则上仅允许bug fix     | 
| Test round 3           | 2023/12/9  | 2023/12/15 | 7    | 全量SIT验证，版本分支代码冻结：管控合入，原则上只允许bug fix      |
| Test round 4           | 2023/12/16 | 2023/12/22 | 7    | 回归测试                                                      |
| Test round 5           | 2023/12/23 | 2023/12/29 | 7    | 回归测试                                                      |
| Release                | 2023/12/30 | 2023/12/30 | 1    | 社区Release版本发布评审                                        |

# 代码合入说明
- 22.03 LTS SP3版本代码继承自22.03 LTS NEXT分支 <br>
- 新特性代码请及时合入版本&自验证，跟随整体计划赶在第一轮转测试



# Feature list
状态说明：Discussion(方案讨论，需求未接受)、 Developing(开发中)、 Testing(测试中)、 Accepted(已验收) <br>
发布方式：ISO、EPOL、oepkgs、独立发布等

|no|feature|status|sig|owner|发布方式|涉及软件包列表|
|:----|:---|:---|:--|:----|:----|:----|
| [I80F3Y](https://gitee.com/openeuler/release-management/issues/I80F3Y) | 支持Lustre server软件包 | Accepted | sig-SDS | [@xin3liang](https://gitee.com/xin3liang) | EPOL | lustre, lustre-release, e2fsprogs |
| [I83JRC](https://gitee.com/openeuler/release-management/issues/I83JRC) | eNFS特性合入 | Rejected | sig-kernel | [@mingqian218472](https://gitee.com/mingqian218472) | ISO | nfs,sunrpc |
| [I82A5V](https://gitee.com/openeuler/release-management/issues/I82A5V) | DDE组件更新支持服务器场景优化 | Accepted | sig-DDE | [@leeffo](https://gitee.com/leeffo) | EPOL | |
| [I84H9S](https://gitee.com/openeuler/release-management/issues/I84H9S) | FangTian视窗引擎特性合入 | Accepted | sig-FangTian | [@BruceXuXu](https://gitee.com/BruceXuXu) | EPOL | |
| [I8AU51](https://gitee.com/openeuler/release-management/issues/I8AU51) | sysMaster支持虚机场景 | Accepted | dev-utils | [@openeuler-basic](https://gitee.com/openeuler-basic) | ISO | sysmaster |
| [I8BKM5](https://gitee.com/openeuler/release-management/issues/I8BKM5) | 支持树莓派 | Accepted | sig-RaspberryPi | [@woqidaideshi](https://gitee.com/woqidaideshi) | EPOL | raspberrypi-firmware,raspberrypi-bluetooth,raspi-config,pigpio,raspberrypi-userland,raspberrypi-eeprom |
|[I8CWV4](https://gitee.com/openeuler/release-management/issues/I8CWV4)|增加 migration-tools 项目发布|Accepted|sig-migration-tools|[@xingwei-liu](https://gitee.com/xingwei-liu/)|EPOL|migration-tools|
|[I8299Y](https://gitee.com/openeuler/release-management/issues/I8299Y)|增加 utshell 项目发布|Accepted|sig-memsafety|[@tong2357](https://gitee.com/tong2357/)|EPOL|utshell|
|[I8DZVE](https://gitee.com/openeuler/release-management/issues/I8DZVE)|增加 utsudo 项目发布|Accepted|sig-memsafety|[@ut-wanglujun](https://gitee.com/ut-wanglujun/)|EPOL|utsudo|
|[I8ERGA](https://gitee.com/openeuler/release-management/issues/I8ERGA)|增加i3相关软件包发布 |Accepted|sig-infrastructure|[@mywaaagh_admin](https://gitee.com/mywaaagh_admin/)|EPOL|i3,i3status,perl-AnyEvent-I3,perl-AnyEvent,xcb-util-xrm,xcompmgr,perl-IO-Pipely,dmenu|
|[I8GQJE](https://gitee.com/openeuler/release-management/issues/I8GQJE)|支持入侵检测框架secDetector |Accepted|sig-security-facility|[@zcfsite](https://gitee.com/zcfsite/)|ISO|secDetector|
|[I8I572](https://gitee.com/openeuler/release-management/issues/I8I572)|支持embedded版本|Accepted|sig-embedded||
|[I8JQ3J](https://gitee.com/openeuler/release-management/issues/I8JQ3J)|NestOS For-Virt/For-Container多版本支持|Accepted|sig-CloudNative,sig-K8sDistro| [@ccdxx](https://gitee.com/ccdxx/) | EPOL |afterburn,bootupd,console-login-helper-messages,ignition.nestos-installer,zincati,nestos-kernel,openeuler-release-nestos-for-container,openeuler-release-nestos-for-virt|
|[I8LBX0](https://gitee.com/openeuler/release-management/issues/I8LBX0?from=project-issue)|gazelle支持vlan收发|Accepted|sig-high-performance-network|@kircher(https://gitee.com/ut-wanglujun/)|EPOL|gazelle|
|[I8LBW8](https://gitee.com/openeuler/release-management/issues/I8LBW8?from=project-issue)|gazelle支持网卡自愈|Accepted|sig-high-performance-network|@kircher(https://gitee.com/ut-wanglujun/)|EPOL|gazelle|
|[I8LBW6](https://gitee.com/openeuler/release-management/issues/I8LBW6?from=project-issue)|gazelle支持netperf标准测试工具|Accepted|sig-high-performance-network|@kircher(https://gitee.com/ut-wanglujun/)|EPOL|gazelle|
|[I8LBW5](https://gitee.com/openeuler/release-management/issues/I8LBW5?from=project-issue)|gazelle支持ipv6协议栈基本功能|Accepted|sig-high-performance-network|@kircher(https://gitee.com/ut-wanglujun/)|EPOL|gazelle|
|[I8LBW4](https://gitee.com/openeuler/release-management/issues/I8LBW4?from=project-issue)|gazelle支持bond6模式|Accepted|sig-high-performance-network|@kircher(https://gitee.com/ut-wanglujun/)|EPOL|gazelle|
|[I8LBV7](https://gitee.com/openeuler/release-management/issues/I8LBV7?from=project-issue)|grub2支持国密度量内核并上报度量信息|Accepted|sig-OS-Builder||EPOL|grub2|
|[I8LBU8](https://gitee.com/openeuler/release-management/issues/I8LBU8?from=project-issue)|shim支持国密度量grub2并上报度量信息|Accepted|sig-Base-service||EPOL|shim|
|[I8LBSO](https://gitee.com/openeuler/release-management/issues/I8LBSO?from=project-issue)|布式软总线功能增强，易用性提升|Accepted|sig-distributed-middleware||EPOL|dsoftbus_standard|
|[I8LBR7](https://gitee.com/openeuler/release-management/issues/I8LBR7?from=project-issue)|分布式软总线容器适配，支持跨节点跨容器通信|Accepted|sig-distributed-middleware||EPOL|dsoftbus_standard|
|[I8LBQS](https://gitee.com/openeuler/release-management/issues/I8LBQS?from=project-issue)|iSulad支持oci runtime并且切换默认runtime为runc|Accepted|sig-iSulad||EPOL|iSulad|
|[I8LBQJ](https://gitee.com/openeuler/release-management/issues/I8LBQJ?from=project-issue)|syscare组件支持容器化热补丁制作场景|Accepted|sig-ops||EPOL|syscare|
|[I8LBQE](https://gitee.com/openeuler/release-management/issues/I8LBQE?from=project-issue)|增加进程完整性防护特性|Accepted|sig-security-facility||EPOL|dim,dim-tools|
|[I8M0CB](https://gitee.com/openeuler/release-management/issues/I8M0CB?from=project-issue)|AOPS功能增强，支持任务粒度回退|Accepted|sig-ops|[@zhu-yuncheng](https://gitee.com/zhu-yuncheng/)|EPOL|aops-ceres，aops-apollo，aops-hermes，aops-zeus，aops-vulcanus|
|[I8M02Y](https://gitee.com/openeuler/release-management/issues/I8M02Y?from=project-issue)|DPU直连聚合：虚拟机、容器管理面DPU卸载，业务无感知|Accepted|sig-DPU |[@minknov](https://gitee.com/minknov/)|EPOL|dpu-utilities|
|[I8M02S](https://gitee.com/openeuler/release-management/issues/I8M02S?from=project-issue)|支持内核态vDPA框架实现网卡直通虚机可热迁移|Accepted|sig-Virt|[@JiaboFeng](https://gitee.com/JiaboFeng/)|EPOL|libvirt,qemu,kernel|
|[I87J40](https://gitee.com/openeuler/release-management/issues/I87J40?from=project-issue)|支持safeguard软件包|Accepted|sig-ebpf|[@tongyx633](https://gitee.com/tongyx633/)|EPOL|safeguard|
|[I8166Y](https://gitee.com/openeuler/release-management/issues/I8166Y?from=project-issue)|libtpms支持sm3算法|Rejected|sig-security-facility|[@zhujianwei001](https://gitee.com/zhujianwei001/)|EPOL|libtpms|
|[I8GWHE](https://gitee.com/openeuler/release-management/issues/I8GWHE?from=project-issue)|增加安全启动签名|Accepted|sig-security-facility|[@huangzq6](https://gitee.com/huangzq6/)|EPOL|shim,grub2,kernel|
|[I8M798](https://gitee.com/openeuler/release-management/issues/I8M798?from=project-issue)|负载算力协同|Accepted|sig-kernel|[@sereinInOpenEuler](https://gitee.com/sereinInOpenEuler/)|EPOL|kernel|


现启动版本需求/特性收集，欢迎各sig maintainer和社区开发者们积极反馈和交流。


# 需求/特性反馈基本流程 <br />
1、开发者/sig在本贴的表格中填写要合入22.03 LTS SP3的需求/特性，并同时填写需求issue及链接 （请在收集截止时间前提交）      <br>
2、申请在版本release management sig例会上评审需求 （owner或者SIG maintainer参会）
<br><br>
