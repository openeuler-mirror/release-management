# Version Info

openEuler 24.03 LTS SP1是基于6.6内核的24.03-LTS版本增强扩展版本（参见[版本生命周期](https://www.openeuler.org/zh/other/lifecycle/)），面向服务器、云、边缘计算和嵌入式场景，持续提供更多新特性和功能扩展，给开发者和用户带来全新的体验，服务更多的领域和更多的用户。<br />

# Release Plan

| Stage Name                    | Deadline for PR | Begin Time | End Time  | Days | Note                                     |
| ----------------------------- | --------------- | ---------- | --------- | ---- | ---------------------------------------- |
| Collect key features          |        -        | 2024/9/1   | 2024/10/31 | 61 | 版本需求收集                              |
| Change Review 1               |        -        | 2024/10/8  | 2024/10/18 | 11 | Review 软件包变更（升级/退役/淘汰）SP版本尽可能保持版本不变  |
| Herited features              |        -        | 2024/10/8  | 2024/11/1  | 25 | 继承特性合入（Branch前完成合入） |
| Develop                       |        -        | 2024/10/8  | 2024/11/28 | 58 | 新特性开发，合入24.03 LTS Next   |
| Kernel freezing               |        -        | 2024/11/1  | 2024/11/8  | 8  | 内核冻结 |
| Branch 24.03 LTS SP1          |        -        | 2024/11/1  | 2024/11/7  | 10 | 24.03 LTS Next 拉取 24.03 LTS SP1 分支 |
| Build & Alpha                 |        -        | 2024/11/8  | 2024/11/14 | 7  | 新开发特性合入，Alpha版本发布    |
| Test round 1                  |    2024/11/13   | 2024/11/15 | 2024/11/21 | 7  | 24.03 LTS SP1 模块测试           |
| Change Review 2               |        -        | 2024/11/22 | 2024/11/24 | 3  | 发起软件包淘汰评审               |
| Test round 2 (Beta Version)   |    2024/11/20   | 2024/11/22 | 2024/11/28 | 7  | 24.03 LTS SP1 Beta版本发布       |
| Test round 3                  |    2024/11/27   | 2024/11/29 | 2024/12/5  | 7  | 全量验证(全量SIT)                |
| Change Review 3               |        -        | 2024/12/3  | 2024/12/5  | 3  | 分支启动冻结，只允许bug fix      |
| Test round 4                  |    2024/12/4    | 2024/12/6  | 2024/12/12 | 7  | 分支冻结，只允许bug fix          |
| Test round 5                  |    2024/12/11   | 2024/12/13 | 2024/12/19 | 7  | 回归测试                         |
| Test round 6 (预留)           |    2024/12/18   | 2024/12/20 | 2024/12/26 | 7  | 回归测试                         |
| Release Review                |        -        | 2024/12/19 | 2024/12/20 | 2  | 版本发布决策/ Go or No Go        |
| Release preparation           |        -        | 2024/12/27 | 2024/12/28 | 2  | 发布前准备阶段，发布件系统梳理    |
| Release                       |        -        | 2024/12/30 | 2024/12/31 | 2  | 社区Release评审通过正式发布       |



# Feature list

#### 状态说明：

- Discussion(方案讨论，需求未接受)
- Developing(开发中)
- Testing(测试中)
- Accepted(已验收)

| no   | feature | status | sig  | owner |
| :--- | :------ | :----- | :--- | :---- |
| [IASH0C](https://gitee.com/openeuler/release-management/issues/IASH0C) | wine5.5升级到wine9.17，不需要linux32依赖库情况下支持win32程序|Discussion|sig-compat-winapp|[@itisyang](https://gitee.com/itisyang)|
| [IATGD8](https://gitee.com/openeuler/release-management/issues/IATGD8) | Add compatibility patches for Zhaoxin processors | Discussion | kernel            | [leoliu-oc](https://gitee.com/leoliu-oc) |
| [IAUPHP](https://gitee.com/openeuler/release-management/issues/IAUPHP) | virtCCA机密虚机特性合入|Discussion|SIG-Kernel/SIG-Virt|[@luoyukai](https://gitee.com/luoyukai)|
| [IAWIGO](https://gitee.com/openeuler/release-management/issues/IAWIGO) | virtCCA+kata机密容器特性合入版本|Discussion|机密计算SIG/云原生SIG|[@luoyukai](https://gitee.com/luoyukai)|
| [IATGD8](https://gitee.com/openeuler/release-management/issues/IAW0BK) | Add Intel QAT packages support | Discussion |sig-Intel-Arch| [@allen-shi](https://gitee.com/allen-shi) |
| [IAYKG8](https://gitee.com/openeuler/release-management/issues/IAYKG8) | 支持plasma5桌面环境 | Discussion |sig-KDE| [@tangjie02](https://gitee.com/tangjie02) |
| [IAZNCN](https://gitee.com/openeuler/release-management/issues/IAZNCN) | 增加YouQu自动化测试平台支持 | Discussion |sig-QA| [@mikigo](https://gitee.com/mikigo) |
| [IAZNA8](https://gitee.com/openeuler/release-management/issues/IAZNA8) | 增加migration-tools支持 | Discussion |sig-migration| [@xingwei-liu](https://gitee.com/xingwei-liu/) |
| [IAZN8U](https://gitee.com/openeuler/release-management/issues/IAZN8U?from=project-issue) | 增加 utsudo 支持 | Discussion |sig-memsafety| [@wangmengc](https://gitee.com/wangmengc/) |
| [IAZN7K](https://gitee.com/openeuler/release-management/issues/IAZN7K?from=project-issue) | 增加 utshell支持 | Discussion |sig-memsafety| [@ut-wanglujun](https://gitee.com/ut-wanglujun) |
| [IAZN4N](https://gitee.com/openeuler/release-management/issues/IAZN4N?from=project-issue) | 增加DDE支持                                                  | Discussion |sig-DDE| [@ut-layne-yang](https://gitee.com/ut-layne-yang) |
| [IAYGKY](https://gitee.com/openeuler/kernel/issues/IAYGKY) | 海光CSV3支持（支持主机创建CSV3虚拟机，支持虚拟机中运行内核） | Developing |sig-kernel| [@hanliyang](https://gitee.com/hanliyang) |
| [IAZ4SZ](https://gitee.com/openeuler/release-management/issues/IAZ4SZ) | enable the SEV-SNP | Discussion |kernel| [@kile2009](https://gitee.com/kile2009) |
| [IB23QK](https://gitee.com/openeuler/release-management/issues/IB23QK) | 集成openGauss 6.0.0 LTS企业版 | Discussion |DB| [@hengliue](https://gitee.com/hengliue) , [@totaj](https://gitee.com/totaj) |
| [IAZOCV](https://gitee.com/openeuler/release-management/issues/IAZOCV) | LLVM多版本实现 | Discussion | sig-Compiler | [@eastb233](https://gitee.com/eastb233) |
| [IAWKJV](https://gitee.com/openeuler/release-management/issues/IAWKJV) | 支持树莓派 | Discussion | SIG-SBC | [@woqidaideshi](https://gitee.com/woqidaideshi/) |
| [IAZOCV](https://gitee.com/openeuler/release-management/issues/IB0JOU) | 新增密码套件openHiTLS | Discussion | sig-security-facility | [@xuhuiyue](https://gitee.com/xuhuiyue) |
| IB43SI(https://gitee.com/openeuler/release-management/issues/IB43SI?from=project-issue) | AI流水线oeDeloy 提升kubeflow部署效率 | Discussion | cicd-sig | [@superninesun](https://gitee.com/superninesun) |
| IB43MJ(https://gitee.com/openeuler/release-management/issues/IB43SI?from=project-issue) | iSula支持NRI插件式扩展（继承） | Discussion | sig-iSulad | [@xuxuepeng](https://gitee.com/xuxuepeng) |
|[IB43D0](https://gitee.com/openeuler/release-management/issues/IB43D0?from=project-issue)| epkg新型软件包及包管理器功能增强 | Discussion | cicd-sig | [@duan_pj](https://gitee.com/duan_pj) |
|[IB43AM](https://gitee.com/openeuler/release-management/issues/IB43AM?from=project-issue)| oeAware采集、调优插件等功能增强 | Discussion | A-Tune sig | [@Lostwayzxc](https://gitee.com/Lostwayzxc) |
|[IB433E](https://gitee.com/openeuler/release-management/issues/IB433E?from=project-issue)| Gazelle特性增强 | Discussion | A-Tune sig | [@nlgwcy](https://gitee.com/nlgwcy) |
|[IB431M](https://gitee.com/openeuler/release-management/issues/IB431M?from=project-issue)| syscare热补丁特性增强（继承） | Discussion | sig-ops | [@luanjianhai](https://gitee.com/luanjianhai) |
|[IB430C](https://gitee.com/openeuler/release-management/issues/IB430C?from=project-issue)| secGear功能优化（继承）| Discussion | sig-confidential-computing | [@houmingyong](https://gitee.com/houmingyong) |
|[IB42WR](https://gitee.com/openeuler/release-management/issues/IB42WR?from=project-issue)| 微服务性能问题分钟级定界/定位（TCP，IO，调度等）继承） | Discussion | A-OPS sig | [@yangyongguang](https://gitee.com/yangyongguang) |
|[IB42TS](https://gitee.com/openeuler/release-management/issues/IB42TS?from=project-issue)| 容器干扰检测，分钟级完成业务干扰源（CPU/IO）识别与干扰源发现（继承） | Discussion | sig-ops| [@wo_cow](https://gitee.com/wo_cow) |
|[IB42PR](https://gitee.com/openeuler/release-management/issues/IB42PR?from=project-issue)| DevStation 开发者工作站支持(继承) | Discussion | desktop sig | [@superninesun](https://gitee.com/superninesun) |
|[IB42MO](https://gitee.com/openeuler/release-management/issues/IB42MO?from=project-issue)| AI集群慢节点快速发现 Add Fail-slow Detection | Discussion | desktop sig | [@webankto](https://gitee.com/webankto) |
|[IB42M9](https://gitee.com/openeuler/release-management/issues/IB42M9?from=project-issue)| KubeOS支持集群参数统一配置、镜像定制化和静态完整性保护 | Discussion | SIG-CloudNative-KubeOS| [@liyuanr](https://gitee.com/liyuanr) |
|[IB42HF](https://gitee.com/openeuler/release-management/issues/IB42HF?from=project-issue)| rubik在离线混部调度协同增强 | Discussion | SIG-CloudNative-KubeOS| [@jingwoo](https://gitee.com/jingwoo) |
|[IB3ZVI](https://gitee.com/openeuler/release-management/issues/IB3ZVI?from=project-issue)| 提供GCC-14的多版本编译工具链 | Discussion | sig-Compiler | [@wangding16](https://gitee.com/wangding16) |
|[IB3ZRQ](https://gitee.com/openeuler/release-management/issues/IB3ZRQ?from=project-issue)| AI4C编译选项调优和AI编译优化提升典型应用性能 | Discussion | sig-Compiler | [@wangding16](https://gitee.com/wangding16) |
|[IB3ZL2](https://gitee.com/openeuler/release-management/issues/IB3ZL2?from=project-issue)| GCC结合sysboost实现无感知使能反馈优化 | Discussion | sig-Compiler | [@wangding16](https://gitee.com/wangding16) |
|[IB3ZG8](https://gitee.com/openeuler/release-management/issues/IB3ZG8?from=project-issue)| RPM国密签名支持 | Discussion | sig-security-facility| [@zhujianwei001](https://gitee.com/zhujianwei001) |
|[IB3ZDN](https://gitee.com/openeuler/release-management/issues/IB3ZDN?from=project-issue)| IMA度量通过异构可信根框架使能TPM/virtCCA信任根 | Discussion | sig-security-facility| [@zhujianwei001](https://gitee.com/zhujianwei001) |
|[IB3ZB1](https://gitee.com/openeuler/release-management/issues/IB3ZB1?from=project-issue)| IMA完整性保护增强，支持对解释器运行的脚本类应用程序使能完整性保护机制 | Discussion | sig-security-facility| [@zhujianwei001](https://gitee.com/zhujianwei001) |
|[IB3X9W](https://gitee.com/openeuler/release-management/issues/IB3X9W?from=project-issue)| 鲲鹏KAE加速器驱动安装包合入 | Discussion | sig-Kernel| [@H_jianmin](https://gitee.com/H_jianmin) |
|[IAZQYW](https://gitee.com/openeuler/release-management/issues/IAZQYW?from=project-issue)| Add OpenVINO packages native support | Discussion | sig-Intel-Arch/sig-intelligence| [@juntianlinux](https://gitee.com/juntianlinux) |
|[IAZQXO](https://gitee.com/openeuler/release-management/issues/IAZQXO?from=project-issue)| Add oneAPI low level native support | Discussion | sig-Intel-Arch/sig-intelligenc| [@juntianlinux](https://gitee.com/juntianlinux) |

<br />
现启动版本需求收集，欢迎各sig maintainer和社区开发者们积极反馈和交流，<br />
<br />
需求反馈基本流程： <br />
1、开发者/sig在本贴的表格中填写要合入24.03 LTS SP1的需求/特性，并同时填写需求issue <br />
2、申请在版本release management例会上评审需求 
<br /><br />
