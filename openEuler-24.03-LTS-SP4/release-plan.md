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
 | [2463](https://atomgit.com/openeuler/release-management/issues/2463) | cu-cockpit  | Developing | sig-security-facility | [@qiucx15](https://atomgit.com/qiucx15) | EPOL | cu-cockpit  |
| [2459](https://atomgit.com/openeuler/release-management/issues/2459) | fastblock块存储项目 | Developing | sig-SDS | [@wuxingyi](https://atomgit.com/wuxingyi) | EPOL | fastblock,fastblock-osd,fastblock-mon,fastblock-kmod |
| [2460](https://atomgit.com/openeuler/release-management/issues/2460) | cu-concrete | Developing | sig-security-facility | [@liuk311](https://gitcode.com/liuk311) | EPOL | cu-concrete |
| [2461](https://atomgit.com/openeuler/release-management/issues/2461) | cu-scanner | Developing | sig-security-facility | [@caojingbo](https://gitcode.com/caojingbo) | EPOL | cu-scanner |
| [2462](https://atomgit.com/openeuler/release-management/issues/2462) | safeguard | Developing | sig-ebpf | [@tongyx633](https://atomgit.com/tongyx633) | EPOL | safeguard |
| [2476](https://atomgit.com/openeuler/release-management/issues/2476) | sysSentry支持节点故障快速通告 | Developing | Kernel-sig, Base-service | [@tong_1001](https://atomgit.com/tong_1001),[@minknov](https://atomgit.com/minknov) | ISO | Kernel,sysSentry |
| [82](https://atomgit.com/openeuler/libvirt/issues/82) | UBNative支持libvirt自动管理vfio-ub驱动 | Developing | Virt-sig | [@xiangzixua](https://atomgit.com/xiangzixua) | ISO | libvirt |
| [8929](https://atomgit.com/openeuler/kernel/issues/8929) | 混部场景，降低在线任务P99劣化率，提高整机的CPU利用率 | Developing | Kernel-sig | [@liaochang](https://atomgit.com/liaochang) | ISO | Kernel |
| [1](https://gitcode.com/openeuler/witty-opentunex/issues/1) | 提供OS层性能分析调优skills，TopDown性能瓶颈自动化识别 | Developing | sig-intelligence | [@hubin95](https://atomgit.com/hubin95) | EPOL | witty-opentunex |
| [8862](https://atomgit.com/openeuler/kernel/issues/8862) | EXT4支持硬件原子写  | Developing | Kernel-sig | [@lonuxli](https://atomgit.com/lonuxli) | ISO | Kernel |
| [2478](https://atomgit.com/openeuler/release-management/issues/2478) | 针对社区kernel包的性能维度问题的自动化定位 | Developing | sig-cicd | [@xiaoniuzi](https://atomgit.com/xiaoniuzi) | 独立发布 | compass-ci |
| [113](https://atomgit.com/src-openeuler/ignition/issues/113) | Support ignition new features | Developing | sig-k8sdistro | [@shiyang0321](https://atomgit.com/shiyang0321) | ISO | ignition |
| [2479](https://atomgit.com/openeuler/release-management/issues/2479) | 虚拟化支持vtimer透传 | Developing | Virt | [@wanywhn](https://atomgit.com/wanywhn) | ISO | qemu,KVM |
| [2480](https://atomgit.com/openeuler/release-management/issues/2480) | AI推理场景支持运行时/基础库行为采集、分析 | Developing | sig-intelligence | [@h3288824963](https://atomgit.com/h3288824963) | EPOL | witty-profiler |
| [2481](https://atomgit.com/openeuler/release-management/issues/2481) | AI训练场景慢卡、慢节点检测算法增强 | Developing | sig-ops | [@JDLihoo](https://atomgit.com/JDLihoo) | EPOL | sysTrace |
| [8424](https://atomgit.com/openeuler/kernel/issues/8424) | 支持 NPU 显存 MB 级切分及隔离 | Developing | Kernel-sig | [@lukace](https://atomgit.com/lukace) | ISO | kernel |
| [2482](https://atomgit.com/openeuler/release-management/issues/2482) | OBMM共享内存支持GDB | Developing | Kernel-sig | [@TrueAI](https://atomgit.com/TrueAI), [@kazero00](https://atomgit.com/kazero00) | ISO | kernel |
| [4](https://gitcode.com/openeuler/ANNC/issues/4) | AI图编译器Embedding复杂算子自动图融合&常量折叠等优化，提升搜推广性能 | Developing | Compiler SIG | [@zhaiwuyue](https://atomgit.com/zhaiwuyue) | Everything | ANNC |
| [2](https://gitcode.com/openeuler/golang/issues/2) | Go编译器静态编译优化增强，运行时内存分区等优化，提升程序性能 | Developing | Compiler SIG, Go SIG | [@wd-gitcode](https://atomgit.com/wd-gitcode) | Everything | golang |
| [2477](https://atomgit.com/openeuler/release-management/issues/2477) | openEuler 24.03 LTS SP4支持CGroupV2 | Developing | Kernel SIG | [@lujialin2](https://atomgit.com/lujialin2) | ISO | kernel |
| [2483](https://atomgit.com/openeuler/release-management/issues/2483) | openEuler支持64k内核发布(双内核方案) | Developing | sig-os-builder  | [@zhangqiumiao](https://atomgit.com/zhangqiumiao),  [@haoyonghao10](https://atomgit.com/haoyonghao10) | ISO | kernel, oemaker, anaconda |
| [117](https://atomgit.com/openeuler/llvm-project/issues/117) | Dwarfutil功能增强，减少典型应用编译后Debug信息 | Developing | Compiler SIG  | [@eastb233](https://atomgit.com/eastb233) | Everything | llvm-project, llvm |
| [2484](https://atomgit.com/openeuler/release-management/issues/2484) | 优化内核补丁回合，提升内核版本补丁合入效率 | Developing | sig-devstation  | [@duan_pengjie](https://atomgit.com/duan_pengjie) | 独立发布 | nvwa-cve-fixer |
| [9216](https://https://atomgit.com/openeuler/kernel/issues/9216) | 大页内存支持swap机制 | Developing | Kernel-sig  | [@zhangliang5](https://atomgit.com/zhangliang5) | ISO | kernel |
| [2490](https://atomgit.com/openeuler/release-management/issues/2490) | 优化鲲鹏950虚拟化转换率 | Developing | Virt-sig  | [@cfalfie](https://atomgit.com/cfalfie) | ISO | spdk |
| [2491](https://atomgit.com/openeuler/release-management/issues/2491) | AI软件包适配（新增30+），覆盖推理场景，兼容DeepSeek，使能沐曦 | Developing | sig-intelligence  | [@jimmy_hero](https://atomgit.com/jimmy_hero),  [@fromhsc](https://atomgit.com/fromhsc) | NA | NA |
| [20](https://gitcode.com/openeuler/MLCacheDirect/issues/20) | RH2D多级缓存直通加速 | Developing | sig long  | [@PhoenixVang](https://atomgit.com/PhoenixVang) | EPOL | MLCacheDirect |

# 需求/特性反馈基本流程&#x20;

1、开发者/sig在本贴的表格中填写要合入该版本的需求/特性，并同时填写需求issue及链接 （请在收集截止时间前提交）     &#x20;
2、申请在版本release management sig例会上评审需求 （owner或者SIG maintainer参会）
