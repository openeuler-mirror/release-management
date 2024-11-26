# Version Info

openEuler 22.03 LTS SP4是基于5.10内核的22.03-LTS版本增强扩展版本（参见[版本生命周期](https://www.openeuler.org/zh/other/lifecycle/)），面向服务器、云、边缘计算和嵌入式场景，持续提供更多新特性和功能扩展，给开发者和用户带来全新的体验，服务更多的领域和更多的用户。<br />

# Release Plan

| Stage Name                    | Begin Time | End Time  | Days | Note                                               |
| ----------------------------- | ---------- | --------- | ---- | -------------------------------------------------- |
| Collect key features          | 2024/3/1   | 2024/4/30 | 60 | 版本需求收集                                       |
| Change Review 1               | 2024/4/1  | 2024/4/12 | 25 | Review 软件包变更（升级/退役/淘汰），SP版本尽可能保持版本不变  |
| Herited features              | 2024/4/1  | 2024/4/30 | 30 | 继承特性合入（Branch前完成合入）    |
| Develop                       | 2024/3/1  | 2024/5/1 | 60 | 新特性开发，合入22.03 LTS Next/SP4 |
| Kernel freezing               | 2024/5/2   | 2024/5/10 | 10 | 内核冻结 |
| Branch 22.03 LTS SP4          | 2024/5/2  | 2024/5/15 | 15 | 22.03 LTS Next 拉取 22.03 LTS SP4 分支           |
| Build & Alpha                 | 2024/5/15  | 2024/5/21  | 7    | 新开发特性合入，Alpha版本发布                      |
| Test round 1                  | 2024/5/24   | 2024/5/30  | 7   | 22.03 LTS SP4 启动集成测试（因gitee lfs基础设施，延期2天）                          |
| Change Review 2               | 2024/5/31  | 2024/6/2 | 3    | 发起软件包淘汰评审                                 |
| Beta version release          | 2024/6/3  | 2024/6/5 | 2    | 22.03 LTS SP4 Beta版本发布                             |
| Test round 2                  | 2024/5/31  | 2024/6/5 | 6    | 全量验证 |
| Change Review 3               | 2024/5/29  | 2024/5/31 | 3    | 分支启动冻结，只允许bug fix                        |
| Test round 3                  | 2024/6/6  | 2024/6/12  | 7    | 分支冻结，只允许bug fix(跨端午节，预祝开发者端午节快乐)  |
| Test round 4                  | 2024/6/13  | 2024/6/19 | 7    | 回归测试 |
| Test round 5                  | 2024/6/20  | 2024/6/26 | 7    | 回归测试 |
| Release Review                | 2024/6/23  | 2024/6/26 | 2    | 版本发布决策/ Go or No Go |
| Release preparation           | 2024/6/27  | 2024/6/28 | 2    | 发布前准备阶段，发布件系统梳理 |
| Release                       | 2024/6/28  | 2024/6/29 | 2    | 社区Release评审通过正式发布 |



# Feature list

#### 状态说明：

- Discussion(方案讨论，需求未接受)
- Developing(开发中)
- Testing(测试中)
- Accepted(已验收)

| no   | feature | status | sig  | owner |
| :--- | :------ | :----- | :--- | :---- |
|[I9IHTX](https://gitee.com/openeuler/release-management/issues/I9IHTX)| 提交内核安全增强补丁 HAOC | Discussion | sig-kernel | [@amjac](https://gitee.com/amjac) |
|[I9PTJ9](https://gitee.com/openeuler/release-management/issues/I9PTJ9?from=project-issue)| 机密计算远程证明服务：远程证明TEE插件框架 | Discussion | sig-confidential computing | [@houmingyong](https://gitee.com/houmingyong) |
|[I9PUSQ](https://gitee.com/openeuler/release-management/issues/I9PUSQ?from=project-issue)| DPU场景vDPA新增支持磁盘，并支持配置vDPA网卡和磁盘的虚机热迁移 | Discussion | virt SIG | [@frankneo](https://gitee.com/frankneo) |
|[I96OAX](https://gitee.com/openeuler/release-management/issues/I96OAX?from=project-issue)| virtCCA机密虚机特性合入 | Discussion | SIG-Kernel/SIG-Virt | [@luoyukai](https://gitee.com/luoyukai) |
|[I9PSTH](https://gitee.com/openeuler/release-management/issues/I9PSTH?from=project-issue)| openSSL支持SM4-CE指令集，提升SM4运算速度 | Discussion | sig-security-facility | [@HuaxinLuGitee](https://gitee.com/HuaxinLuGitee) |
|[I9TI38](https://gitee.com/openeuler/release-management/issues/I9TI38?from=project-issue)| PowerAPI功耗管理统一API | Discussion | sig-power-efficient | [@heppen](https://gitee.com/heppen) |
|[I9THX9](https://gitee.com/openeuler/release-management/issues/I9THX9?from=project-issue)| eagle实现整机能耗管理 | Discussion | sig-power-efficient | [@heppen](https://gitee.com/heppen) |
|[I9SSLS](https://gitee.com/openeuler/release-management/issues/I9SSLS?from=project-issue)| gala-ragdoll支持实时监控文件变更信息 | Discussion | sig-ops | [@zhangdaolong](https://gitee.com/zhangdaolong) |
|[I9TNWE](https://gitee.com/openeuler/release-management/issues/I9TNWE?from=project-issue)| 支持sysSentry故障管理框架| Discussion | sig-Base-service | [@huangduirong](https://gitee.com/huangduirong) |

<br />
现启动版本需求收集，欢迎各sig maintainer和社区开发者们积极反馈和交流，<br />
<br />
需求反馈基本流程： <br />
1、开发者/sig在本贴的表格中填写要合入22.03 LTS SP4的需求/特性，并同时填写需求issue <br />
2、申请在版本release management例会上评审需求 
<br /><br />
