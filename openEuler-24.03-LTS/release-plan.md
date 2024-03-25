# Version Info

openEuler 24.03 LTS是基于6.6内核的长周期LTS版本（参见[版本生命周期](https://www.openeuler.org/zh/other/lifecycle/)），面向服务器、云、边缘计算、AI和嵌入式场景，提供更多新特性和功能，给开发者和用户带来全新的体验，服务更多的领域和更多的用户。<br />

# Release Plan

| Stage Name                    | Begin Time | End Time  | Days | Note                                               |
| ----------------------------- | ---------- | --------- | ---- | -------------------------------------------------- |
| Collect key features          | 2023/12/8  | 2024/1/30 | 54   | 版本需求收集                                       |
| Change Review 1               | 2024/1/16  | 2024/2/10 | 25   | Review 软件包变更（升级/退役/淘汰）                |
| Herited features              | 2024/1/30  | 2024/2/29 | 30   | 继承特性合入                                       |
| Develop                       | 2023/12/1  | 2024/2/29 | 90   | 新特性开发，合入master；KABI预留，白名单制定及公示 |
| Kernel freezing               | 2024/3/1   | 2024/3/10 | 10   | 内核冻结                                           |
| Branch 24.03 LTS              | 2024/3/11  | 2024/3/20 | 10   | master 拉取24.03 LTS Next及24.03 LTS分支           |
| Branch 24.03 LTS mass rebuild | 2024/3/21  | 2024/3/26 | 6    | 新分支大规模构建                                   |
| Build & Alpha                 | 2024/3/27  | 2024/4/2  | 7    | 新开发特性合入，Alpha版本发布                      |
| Test round 1                  | 2024/4/3   | 2024/4/9  | 7    | 24.03 LTS 启动集成测试                             |
| Change Review 2               | 2024/4/10  | 2024/4/12 | 3    | 发起软件包淘汰评审                                 |
| Beta version release          | 2024/4/13  | 2024/4/19 | 7    | 24.03 LTS Beta版本发布                             |
| Test round 2                  | 2024/4/20  | 2024/4/26 | 7    | 全量验证                                           |
| Change Review 3               | 2024/4/27  | 2024/4/29 | 3    | 分支启动冻结，只允许bug fix                        |
| Test round 3                  | 2024/4/30  | 2024/5/6  | 7    | 分支冻结，只允许bug fix                            |
| Test round 4                  | 2024/5/7   | 2024/5/13 | 7    | 回归测试                                           |
| Test round 5                  | 2024/5/14  | 2024/5/20 | 7    | 回归测试                                           |
| Release Review                | 2024/5/21  | 2024/5/23 | 3    | 版本发布决策/ Go or No Go                          |
| Release preparation           | 2024/5/24  | 2024/5/30 | 7    | 发布前准备阶段，发布件系统梳理                     |
| Release                       | 2024/5/31  | 2024/5/31 | 1    | 社区Release评审通过正式发布                        |



# Feature list

#### 状态说明：

- Discussion(方案讨论，需求未接受)
- Developing(开发中)
- Testing(测试中)
- Accepted(已验收)

| no   | feature | status | sig  | owner |
| :--- | :------ | :----- | :--- | :---- |
|[I8WG9C](https://gitee.com/openeuler/release-management/issues/I8WG9C) | 发布kiran-desktop 2.6版本 | Discussion | sig-KIRAN-DESKTOP | [@liubuguiii](https://gitee.com/liubuguiii) |
|[I8UU1C](https://gitee.com/openeuler/release-management/issues/I8UU1C)|iSulad支持CRI v1.29|Discussion|sig-iSulad|[@xuxuepeng](https://gitee.com/xuxuepeng)|
|[I8UUCX](https://gitee.com/openeuler/release-management/issues/I8UUCX)|iSulad支持CDI|Discussion|sig-iSulad|[@xuxuepeng](https://gitee.com/xuxuepeng)|
|[I8UVAY](https://gitee.com/openeuler/release-management/issues/I8UVAY)|iSulad支持NRI|Discussion|sig-iSulad|[@xuxuepeng](https://gitee.com/xuxuepeng)|
|[I8W6CJ](https://gitee.com/openeuler/release-management/issues/I8W6CJ)|iSulad支持cgroup v2|Discussion|sig-iSulad|[@xuxuepeng](https://gitee.com/xuxuepeng)|
|[I8Y48L](https://gitee.com/openeuler/release-management/issues/I8Y48L)|为 RISC-V 架构增加内核热补丁能力|Discussion|sig-RISC-V|[@laokz](https://gitee.com/laokz)|
|[I8Y3WV](https://gitee.com/openeuler/release-management/issues/I8Y3WV)|为 RISC-V 架构引入 Penglai TEE 支持|Discussion|sig-RISC-V|[@dongduResearcher](https://gitee.com/dongduResearcher)|
|[I8YAGF](https://gitee.com/openeuler/release-management/issues/I8YAGF)|wine5.5升级到wine9.0，不需要linux32依赖库情况下支持win32程序|Discussion|sig-compat-winapp|[@niko_yhc](https://gitee.com/niko_yhc)|
|[I8Y4I0](https://gitee.com/openeuler/release-management/issues/I8Y4I0)|支持树莓派|Discussion|sig-RaspberryPi|[@woqidaideshi](https://gitee.com/woqidaideshi/)|
|[I914GW](https://gitee.com/openeuler/release-management/issues/I914GW)|DDE支持|Discussion|sig-DDE|[@ut-layne-yang](https://gitee.com/ut-layne-yang)|
|[I8ZJBA](https://gitee.com/openeuler/release-management/issues/I8ZJBA)|migration-tools增加图形化迁移openeuler功能|Discussion|sig-Migration|[@xingwei-liu](https://gitee.com/xingwei-liu/)|
|[I8ZJFG](https://gitee.com/openeuler/release-management/issues/I8ZJFG)|增加 utshell 项目发布|Discussion|sig-memsafety|[@wangmengc](https://gitee.com/wangmengc/)|EPOL|utshell|
|[I8ZJGW](https://gitee.com/openeuler/release-management/issues/I8ZJGW)|增加 utsudo 项目发布|Discussion|sig-memsafety|[@ut-wanglujun](https://gitee.com/ut-wanglujun/)|EPOL|utsudo|
|[I94ET0](https://gitee.com/openeuler/release-management/issues/I94ET0)|发布Nestos-kubernetes-deployer |Discussion|sig-K8sDistro|[@duyiwei7w](https://gitee.com/duyiwei7w)|
|[I9780H](https://gitee.com/openeuler/release-management/issues/I9780H)| 支持vCPU热插拔 |Discussion|sig-kernel|[@JiaboFeng](https://gitee.com/JiaboFeng)|
|[I9780Y](https://gitee.com/openeuler/release-management/issues/I9780Y)| A-Ops gala提供网络L4层TCP主流指标观测能力 |Discussion|sig-ops|[@MrRlu](https://gitee.com/MrRlu)|
|[I97814](https://gitee.com/openeuler/release-management/issues/I97814)| A-Ops gala提供网络L7层RED指标观测能力 |Discussion|sig-ops |[@MrRlu](https://gitee.com/MrRlu)|
|[I97817](https://gitee.com/openeuler/release-management/issues/I97817)| A-Ops gala提供应用粒度的I/O、CPU、MEM资源占用观测能力|Discussion|sig-ops |[@MrRlu](https://gitee.com/MrRlu)|
|[I9781E](https://gitee.com/openeuler/release-management/issues/I9781E)| A-Ops gala支持可观测行为的动态变更 |Discussion|sig-ops |[@MrRlu](https://gitee.com/MrRlu)|
|[I9781K](https://gitee.com/openeuler/release-management/issues/I9781K)|内存潮汐调度：支持serverless容器热备份 |Discussion|sig-kernel |[@ stkid](https://gitee.com/stkid)|
|[I9782E](https://gitee.com/openeuler/release-management/issues/I9782E)| LLVM版本升级到17.0.6 |Discussion|sig-Compiler |[@ cf-zhao](https://gitee.com/cf-zhao)|
|[I9784H](https://gitee.com/openeuler/release-management/issues/I9784H)| 支持系统运维套件x-diagnosis |Discussion|sig-ops ||
|[ I9784N](https://gitee.com/openeuler/release-management/issues/I9784N)| 支持自动化热升级组件nvwa |Discussion|sig-ops ||
|[ I9785W](https://gitee.com/openeuler/release-management/issues/I9785W)| 支持DPU直连聚合特性 |Discussion|sig-DPU ||
|[ I9786D](https://gitee.com/openeuler/release-management/issues/I9786D)| 支持系统热修复组件syscare |Discussion|sig-ops ||
|[ I9786H](https://gitee.com/openeuler/release-management/issues/I9786H)| 支持内存分级扩展组件etmem |Discussion|sig-Storage|[@swf504](https://gitee.com/swf504)|
|[ I97878](https://gitee.com/openeuler/release-management/issues/I97878)| iSula容器镜像构建工具isula-build |Discussion|sig-iSulad||
|[ I9787D](https://gitee.com/openeuler/release-management/issues/I9787D)| 一键式、轻量化、可配置集群部署工具eggo |Discussion|sig-isulad ||
|[ I9787G](https://gitee.com/openeuler/release-management/issues/I9787G)| 支持容器引擎isulad |Discussion|sig-iSulad ||
|[ I9787L](https://gitee.com/openeuler/release-management/issues/I9787L)| 支持进程完整性防护特性 |Discussion|sig-security-facility |[@HuaxinLuGitee](https://gitee.com/HuaxinLuGitee)|
|[ I9787O](https://gitee.com/openeuler/release-management/issues/I9787O)| 支持入侵检测框架secDetector|Discussion|sig-security-facility |[@zcfsite](https://gitee.com/zcfsite)|
|[ I9787P](https://gitee.com/openeuler/release-management/issues/I9787P)| imageTailor支持树莓派镜像定制|Discussion|sig-OS-Builder |[@zhuchunyi](https://gitee.com/zhuchunyi)|
|[ I9787U](https://gitee.com/openeuler/release-management/issues/I9787U)| 支持secPaver特性 |Discussion|sig-security-facility |[@HuaxinLuGitee](https://gitee.com/HuaxinLuGitee)|
|[ I9788R](https://gitee.com/openeuler/release-management/issues/I9788R)| 支持机密计算安全应用开发组件 secGear |Discussion|sig-confidential-computing |[@houmingyong](https://gitee.com/houmingyong)|
|[ I9788S](https://gitee.com/openeuler/release-management/issues/I9788S)| 系统性能自优化组件A-Tune |Discussion|sig-A-Tune|[@ gaoruoshu](https://gitee.com/gaoruoshu)|
|[ I9788W](https://gitee.com/openeuler/release-management/issues/I9788W)| isocut镜像裁剪易用性提升 |Discussion|sig-OS-Builder |[@zhuchunyi](https://gitee.com/zhuchunyi)|
|[ I97890](https://gitee.com/openeuler/release-management/issues/I97890)| 支持devmaster组件 |Discussion|sig-dev-utils ||
|[ I9789Q](https://gitee.com/openeuler/release-management/issues/I9789Q)| 支持TPCM特性 |Discussion|sig-Base-service|[@t_feng](https://gitee.com/t_feng)|
|[ I9789U](https://gitee.com/openeuler/release-management/issues/I9789U)| 支持sysMaster组件 |Discussion|sig-dev-utils ||
|[ I9789V](https://gitee.com/openeuler/release-management/issues/I9789V)| 安全配置规范框架设计及核心内容构建 |Discussion|sig-security-facility||
|[ I9789Y](https://gitee.com/openeuler/release-management/issues/I9789Y)| A-OPS智能运维工具 |Discussion|sig-ops||
|[ I978A1](https://gitee.com/openeuler/release-management/issues/I978A1)| 支持sysmonitor特性 |Discussion|sig-ops|[@foreson](https://gitee.com/foreson)|
|[ I978A3](https://gitee.com/openeuler/release-management/issues/I978A3)| kmesh-bwm高性能网络带宽管理 |Discussion|sig-high-performance-network|[@yanan-rock](https://gitee.com/yanan-rock)|
|[ I978A5](https://gitee.com/openeuler/release-management/issues/I978A5)| Gazelle用户态协议栈 |Discussion|sig-high-performance-network |[@yanan-rock](https://gitee.com/yanan-rock)|
|[ I978A7](https://gitee.com/openeuler/release-management/issues/I978A7)| 混合部署rubik |Discussion|sig-CloudNative||
|[ I978AC](https://gitee.com/openeuler/release-management/issues/I978A1)| isulad支持oci runtime并且切换默认runtime为runc |Discussion|sig-iSulad ||
|[ I97DTY](https://gitee.com/openeuler/release-management/issues/I97DTY)| 支持embedded |Discussion|sig-embedded|[@fanglinxu](https://gitee.com/fanglinxu)|
|[I942Y9](https://gitee.com/openeuler/release-management/issues/I942Y9)|发布PilotGo及其插件特性新版本 |Discussion|sig-ops|[@yangzhao_kl](https://gitee.com/yangzhao_kl)|
|[I95KTM](https://gitee.com/openeuler/release-management/issues/I95KTM)|UKUI支持|Discussion|sig-UKUI|[@hua_yadong](https://gitee.com/hua_yadong)|
|[I98UXD](https://gitee.com/openeuler/release-management/issues/I98UXD)|支持ROS2-humble和ROS1-noetic基础版|Discussion|sig-ROS|[@davidhan008](https://gitee.com/davidhan008/)|
|[I985WB](https://gitee.com/openeuler/release-management/issues/I985WB) | 支持 OpenStack Wallaby、Antelope 多版本 | Discussion | sig-openstack | [@han-guangyu](https://gitee.com/han-guangyu) |
|[I97AX0](https://gitee.com/openeuler/release-management/issues/I97AX0)| 社区签名体系建立 |Discussion|sig-security-facility |[@HuaxinLuGitee](https://gitee.com/HuaxinLuGitee)|
|[I97D8Z](https://gitee.com/openeuler/release-management/issues/I97D8Z)| 智能问答在线服务 |Discussion| |[@fromhsc](https://gitee.com/fromhsc)|
|[I97IVO](https://gitee.com/openeuler/release-management/issues/I97IVO)| 支持国密特性 |Discussion|sig-security-facility |[@HuaxinLuGitee](https://gitee.com/HuaxinLuGitee)|
|[ I980D1](https://gitee.com/openeuler/release-management/issues/I980D1)| Gazelle支持UDP协议栈|Discussion|sig-high-performance-network |[@yanan-rock](https://gitee.com/yanan-rock)|
|[I8ZTS2](https://gitee.com/openeuler/release-management/issues/I8ZTS2)| 增加 AO.space 项目发布 |Discussion|sig-RaspberryPi  |[@jianminw](https://gitee.com/jianminw)|
|[I8XFUF](https://gitee.com/openeuler/release-management/issues/I8XFUF)| 合入GreatSQL 8.0.32-25及更高版本 |Discussion| |[@GreatSQL_admin](https://gitee.com/GreatSQL_admin)|
|[I8YUI2](https://gitee.com/openeuler/release-management/issues/I8YUI2)| 发布elastisearch-py 7.13.4版本 |Discussion| |[@lin-shoubao](https://gitee.com/lin-shoubao)|
|[I9B6RR](https://gitee.com/openeuler/release-management/issues/I9B6RR)| ZGCLab 发布内核安全增强补丁 | Discussion | sig-kernel | [@amjac](https://gitee.com/amjac) |

<br />
现启动版本需求收集，欢迎各sig maintainer和社区开发者们积极反馈和交流，<br />
<br />
需求反馈基本流程： <br />
1、开发者/sig在本贴的表格中填写要合入24.03-LTS的需求/特性，并同时填写需求issue <br />
2、申请在版本release management例会上评审需求 
<br /><br />
