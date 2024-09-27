# Version Info

openEuler 24.09 是基于6.6内核的创新版本（参见[版本生命周期](https://www.openeuler.org/zh/other/lifecycle/)）。<br />

# Release Plan

| Stage Name                    | Begin Time | End Time  | Days | Note                                               |
| ----------------------------- | ---------- | --------- | ---- | -------------------------------------------------- |
| Collect key features          | 2024/6/3   | 2024/7/16 | 44   | 版本需求收集                                       |
| Change Review 1               | 2024/7/1  | 2024/7/12 | 25   | Review 软件包变更（升级/退役/淘汰）                |
| Herited features              | 2024/7/1  | 2024/7/22 | 23   | 继承特性合入（Branch前完成合入）  |
| Develop                       | 2024/7/1  | 2024/8/19 | 50   | 新特性开发，合入master |
| Kernel freezing               | 2024/7/16   | 2024/7/22 | 10   | 内核冻结                                           |
| Branch 24.09                  | 2024/7/22  | 2024/8/5 | 15 | master 拉取 24.09 分支           |
| Build & Alpha                 | 2024/8/6  | 2024/8/12  | 7    | 新开发特性合入，Alpha版本发布                      |
| Test round 1                  | 2024/8/13   | 2024/8/19  | 7   | 24.09 启动集成测试                             |
| Change Review 2               | 2024/8/13  | 2024/8/15 | 3    | 发起软件包淘汰评审                                 |
| Beta version release          | 2024/8/16  | 2024/8/19 | 4    | 24.09 Beta版本发布                             |
| Test round 2                  | 2024/8/20  | 2024/8/26 | 7    | 全量验证                                           |
| Change Review 3               | 2024/8/27  | 2024/8/29 | 3    | 分支启动冻结，只允许bug fix                        |
| Test round 3                  | 2024/8/29  | 2024/9/4  | 7    | 分支冻结，只允许bug fix                            |
| Test round 4                  | 2024/9/5   | 2024/9/11 | 7    | 回归测试                                           |
| Test round 5                  | 2024/9/12  | 2024/9/19 | 7    | 回归测试（跨中秋节，预祝中秋节快乐）                 |
| Release Review                | 2024/9/20  | 2024/9/22 | 3    | 版本发布决策/ Go or No Go                          |
| Release preparation           | 2024/9/23  | 2024/9/28 | 6    | 发布前准备阶段，发布件系统梳理                     |
| Release                       | 2024/9/29  | 2024/9/30 | 2    | 社区Release评审通过正式发布                        |



# Feature list

#### 状态说明：

- Discussion(方案讨论，需求未接受)
- Developing(开发中)
- Testing(测试中)
- Accepted(已验收)

| no   | feature | status | sig  | owner |
| :--- | :------ | :----- | :--- | :---- |
|[I9UYO9](https://gitee.com/openeuler/release-management/issues/I9UYO9)| virtCCA机密虚机特性合入 | Discussion | SIG-Kernel/SIG-Virt | [@luoyukai](https://gitee.com/luoyukai) |
|[IAFDNQ](https://gitee.com/openeuler/release-management/issues/IAFDNQ)| 支持树莓派 | Discussion | SIG-SBC | [@woqidaideshi](https://gitee.com/woqidaideshi/) |
|[IADBJG](https://gitee.com/openeuler/release-management/issues/IADBJG)| 继承特性：发布Nestos-kubernetes-deployer | Discussion | SIG-CN | [@weihuanhuan_ky](https://gitee.com/weihuanhuan_ky) |
|[IAHMJ1](https://gitee.com/openeuler/release-management/issues/IAHMJ1)| 新增基于《openEuler 安全配置基线》检测工具 | Discussion | SIG-security-facility | [@chaomingmeng](https://gitee.com/chaomingmeng) |
|[IAJ6C4](https://gitee.com/openeuler/release-management/issues/IAJ6C4)|支持ROS2-humble和ROS1-noetic基础版|Discussion|sig-ROS|[@davidhan008](https://gitee.com/davidhan008/)|
|[IAJVVH](https://gitee.com/openeuler/release-management/issues/IAJVVH)|增加 utshell 项目发布|Discussion|sig-memsafety|[@wangmengc](https://gitee.com/wangmengc/)|EPOL|utshell|
|[IAJQIB](https://gitee.com/openeuler/release-management/issues/IAJQIB)|增加 utsudo 项目发布|Discussion|sig-memsafety|[@trackers-love](https://gitee.com/trackers-love/)|EPOL|utsudo|
|[IAMSTO](https://gitee.com/openeuler/release-management/issues/IAMSTO?from=project-issue)| epkg新型软件包的OS镜像构建 | Discussion | cicd-sig | [@duan_pj](https://gitee.com/duan_pj) |
|[IAMSQP](https://gitee.com/openeuler/release-management/issues/IAMSQP?from=project-issue)| DevStation 开发者工作站支持 | Discussion | desktop sig | [@superninesun](https://gitee.com/superninesun) |
|[IAMLWI](https://gitee.com/openeuler/release-management/issues/IAMLWI?from=project-issue)| 微服务性能问题分钟级定界/定位（TCP，IO，调度等） | Discussion | A-OPS sig | [@yangyongguang](https://gitee.com/yangyongguang) |
|[IAMLGE](https://gitee.com/openeuler/release-management/issues/IAMLGE?from=project-issue)| Aops支持智能运维助手 | Discussion | sig-ops/ sig-AI | [@solarhu](https://gitee.com/solarhu) |
|[IAMLAK](https://gitee.com/openeuler/release-management/issues/IAMLAK?from=project-issue)| 容器干扰检测，分钟级完成业务干扰源（CPU/IO）识别与干扰源发现 | Discussion | sig-ops| [@wo_cow](https://gitee.com/wo_cow) |
|[IAML7Y](https://gitee.com/openeuler/release-management/issues/IAML7Y?from=project-issue)| 构建远程证明统一框架，支持部署远程证明服务 | Discussion | sig-confidential-computing| [@houmingyong](https://gitee.com/houmingyong) |
|[IAML6V](https://gitee.com/openeuler/release-management/issues/IAML6V?from=project-issue)| IMA摘要列表支持三方PKI证书导入 | Discussion | sig-security-facility| [@HuaxinLuGitee](https://gitee.com/HuaxinLuGitee) |
|[IAML3W](https://gitee.com/openeuler/release-management/issues/IAML3W?from=project-issue)| KubeOS支持串、并行多种升级策略、状态更新等声明式API | Discussion | SIG-CloudNative-KubeOS| [@liyuanr](https://gitee.com/liyuanr) |
|[IAMKXU](https://gitee.com/openeuler/release-management/issues/IAMKXU?from=project-issue)| etmem内存扩展，实现虚机内存超分 | Discussion | storage sig| [@liubo254](https://gitee.com/liubo254) |
|[IAMKUJ](https://gitee.com/openeuler/release-management/issues/IAMKUJ?from=project-issue)| 构建双内核（5.10+6.6内核），完成基本功能验证 | Discussion | QA Sig | [@duan_pj](https://gitee.com/duan_pj) |
|[IAMKQL](https://gitee.com/openeuler/release-management/issues/IAMKQL?from=project-issue)| oeAware 支持本地网络加速 | Discussion | A-Tune sig | [@Lostwayzxc](https://gitee.com/Lostwayzxc) |
|[IAMKHS](https://gitee.com/openeuler/release-management/issues/IAMKHS?from=project-issue)| iSula支持NRI插件式扩展 | Discussion | sig-iSulad | [@xuxuepeng](https://gitee.com/xuxuepeng) |
|[IAMKB1](https://gitee.com/openeuler/release-management/issues/IAMKB1?from=project-issue)| 支持GCC 14多版本使能多样算力新特性 | Discussion | sig-Compiler | [@zhaoshujian](https://gitee.com/zhaoshujian) |
|[IAMK8J](https://gitee.com/openeuler/release-management/issues/IAMK8J?from=project-issue)| secGear功能优化 | Discussion | sig-confidential-computing | [@houmingyong](https://gitee.com/houmingyong) |
|[IAMK2Q](https://gitee.com/openeuler/release-management/issues/IAMK2Q?from=project-issue)| syscare特性增强：用户态热补丁支持栈检测 | Discussion | sig-ops | [@bb-cat](https://gitee.com/bb-cat) |
|[IAMJYQ](https://gitee.com/openeuler/release-management/issues/IAMJYQ?from=project-issue)| syscare特性增强：用户态热补丁支持容器化制作 | Discussion | sig-ops | [@luanjianhai](https://gitee.com/luanjianhai) |
|[IADN2N](https://gitee.com/openeuler/release-management/issues/IADN2N?from=project-issue)| 支持embedded版本 | Discussion | sig-embedded | [@fanglinxu](https://gitee.com/fanglinxu) |
|[IAOLZ3](https://gitee.com/openeuler/release-management/issues/IAOLZ3?from=project-issue)|  增加pandoc 项目发布 | Discussion | sig-haskell | [@lrzlin](https://gitee.com/lrzlin) |
|[IAPEKI](https://gitee.com/ncti-gba-ide/release-management/issues/IAPEKI?from=project-issue)|  增加国创OS开发工具 | Discussion | sig-ide | [@ncti-gba-ide](https://gitee.com/ncti-gba-ide) |
|[IAT24U](https://gitee.com/openeuler/release-management/issues/IAT24U?from=project-issue)|  为 RISC-V 架构引入 Penglai TEE 支持 | Discussion | sig-RISC-V | [ @Jingwiw ](https://gitee.com/Jingwiw) |
|[IATWZR](https://gitee.com/openeuler/release-management/issues/IATWZR?from=project-issue)|  平行宇宙计划 增加 24.09 RISC-V 架构 Preview 版本 | Discussion | sig-RISC-V | [ @jchzhou ](https://gitee.com/jchzhou) |

<br />
现启动版本需求收集，欢迎各sig maintainer和社区开发者们积极反馈和交流，<br />
<br />
需求反馈基本流程： <br />
1、开发者/sig在本贴的表格中填写要合入24.09的需求/特性，并同时填写需求issue <br />
2、申请在版本release management例会上评审需求 
<br /><br />
