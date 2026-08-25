# 版本信息
openEuler 26.09-DevStation 是面向 DevStation 场景的创新版本（参见[版本生命周期](https://www.openeuler.org/zh/other/lifecycle/)），面向开发者工作站、智能化开发工具、软件商店、mcpmarket、skillhub、agentStore、开发环境管理和桌面开发体验等场景，提供更多新特性和功能，给开发者和用户带来原生openEuler AI-Native Operating System 体验。<br>


# 发布计划

| 阶段名称                      | PR截止时间 | 开始时间   | 结束时间   | 天数 | 说明                                     |
| ----------------------------- | --------------- | ---------- | ---------  | ---- | ---------------------------------------- |
| 关键特性收集                  |        -        | 2026/06/01 | 2026/07/30 | 60 | 版本需求收集                              |
| 变更评审 1                    |        -        | 2026/07/01 | 2026/08/15 | 46 | 评审软件包变更（升级/退役/淘汰）  |
| 继承特性合入                  |        -        | 2026/07/01 | 2026/08/15 | 46 | 继承特性合入（Beta前完成合入） |
| 开发阶段                      |        -        | 2026/07/01 | 2026/09/02 | 64 | 新特性开发，Branch前合入Master，Branch后合入26.09-DevStation及Master，6.6内核合入26.09分支(round 6冻结前合入) |
| 内核冻结                      |        -        | 2026/07/01 | 2026/08/15 | 46 | 内核冻结（随Beta版本，内核冻结） |
| 拉取 26.09-DevStation 分支     |        -        | 2026/07/20 | 2026/07/31 | 12 | Master拉取26.09-DevStation分支，内核额外拉取26.09分支用于6.6版本 |
| 构建与 Alpha                  |    2026/08/05   | 2026/08/07 | 2026/08/13 | 07 | 新开发特性合入，Alpha版本发布（重点关注软件选型&构建问题） |
| 测试轮次 1                    |    2026/08/12   | 2026/08/14 | 2026/08/20 | 07 | 26.09-DevStation 模块测试           |
| 测试轮次 2（Beta版本）        |    2026/08/19   | 2026/08/21 | 2026/08/27 | 07 | 26.09-DevStation Beta版本发布（KABI基线）    |
| 变更评审 2                    |        -        | 2026/08/21 | 2026/08/26 | 06 | 发起软件包淘汰评审 |
| 测试轮次 3                    |    2026/08/26   | 2026/08/28 | 2026/09/03 | 07 | 26.09-DevStation 模块测试       |
| 测试轮次 4                    |    2026/09/02   | 2026/09/04 | 2026/09/10 | 07 | 全量验证（全量SIT）  |
| 变更评审 3                    |        -        | 2026/09/04 | 2026/09/09 | 06 | 发起软件包淘汰评审      |
| 测试轮次 5                    |    2026/09/09   | 2026/09/11 | 2026/09/17 | 07 | 分支冻结，只允许bug fix          |
| 测试轮次 6                    |    2026/09/16   | 2026/09/18 | 2026/09/23 | 07 | 回归测试                         |
| 发布评审                      |        -        | 2026/09/21 | 2026/09/24 | 04 | 版本发布决策/ Go or No Go, 中秋快乐        |
| 发布准备                      |        -        | 2026/09/23 | 2026/09/24 | 02 | 发布前准备阶段，发布件系统梳理    |
| 发布                          |        -        | 2026/09/28 | 2026/09/30 | 03 | 社区Release评审通过正式发布       |

* ```PR截止时间```: 构建启动（即PR停止接收构建）时间，当天晚8点后启动构建；
* ```开始时间```: 转测开始时间，即在当天早9点前，完成转测镜像的构建、AT冒烟及发布；
* ```结束时间```: 转测结束时间，下一轮 ```开始时间``` -1天，测试团队需完成本轮次所有问题的提交;


# 代码合入说明
创新版本代码继承master分支 <br>
// 新特性代码请及时合入版本&自验证，跟随整体计划赶在第一轮转测试


# 特性清单
状态说明：Discussion(方案讨论，需求未接受)、 Developing(开发中)、 Testing(测试中)、 Accepted(已验收) <br>
发布方式：ISO、Everything、EPOL、oepkgs、独立发布等

|编号|特性|状态|SIG|责任人|发布方式|涉及软件包列表|
|:----|:---|:---|:--|:----|:----|:----|
| [2561](https://atomgit.com/openeuler/release-management/issues/2561) | 【openEuler 26.09创新】【Agent Infra】【Agent调度】通过数据引用方式按需加载构建上下文管理系统，减少上下文长度 | Developing | sig-Intelligence | [@linpengcheng1994](https://gitcode.com/linpengcheng1994)     | EPOL | sccs |
| [2562](https://atomgit.com/openeuler/release-management/issues/2562) | 【openEuler 26.09创新】【Agent Infra】【可观测&治理】构建可观测+治理框架底座，穿刺全链路观测+安全防护+审计能力 | Developing | sig-Intelligence | [@yaozhenhe](https://gitcode.com/yaozhenhe)     | EPOL | AcTrail |
| [2563](https://atomgit.com/openeuler/release-management/issues/2563) | 【openEuler 26.09创新】【Agent Infra】【Agent调度】Agent/KVC协同调度：感知“Agent语义”的KVC调度，降低Agent推理等待时延 | Developing | sig-Intelligence | [@xtchen](https://gitcode.com/xtchen)     | EPOL | RAM-A |
| [2564](https://atomgit.com/openeuler/release-management/issues/2564) | 【openEuler 26.09创新】【AI Infra】【推理加速】DDR+HBM 分级协同，KV swap聚合传输，长序列>64K 推理场景多BS降低平均时延 | Developing | sig-Intelligence | [@zxstty](https://gitcode.com/zxstty)     | EPOL | sysHAX |
| [2565](https://atomgit.com/openeuler/release-management/issues/2565) | 【openEuler 26.09创新】【开发者生态及工具】【skillhub】openEuler上线skillshub，汇聚社区skill生态 | Developing | sig-Devstation | [@ftboy](https://gitcode.com/ftboy)     | 独立发布 | wittyhub, wittyhub-cli |
| [2566](https://atomgit.com/openeuler/release-management/issues/2566) | 【openEuler 26.09创新】【开发者生态及工具】【DevStation】openEuler DevStation：面向用户和开发者快速迭代尝鲜的openEuler创新版本 | Developing | sig-Devstation | [@w520203](https://gitcode.com/w520203)     | 独立发布 | gdm, gnome-shell,gnome-session,epkg,polymind |
| [2567](https://atomgit.com/openeuler/release-management/issues/2567) | 【openEuler 26.09创新】【开发者生态及工具】【EPKG】完成EPKG默认集成到openEuler DevStation版本 | Developing | sig-epkg | [@w520203](https://gitcode.com/w520203)     | 独立发布 | epkg |
| [2568](https://atomgit.com/openeuler/release-management/issues/2568) | 【openEuler 26.09创新】oeaware：提供场景化智能调优skills | Developing | sig-Intelligence | [@cloudyyy1234](https://gitcode.com/cloudyyy1234)     | EPOL | witty-opentunex |
| [2569](https://atomgit.com/openeuler/release-management/issues/2569) | 【openEuler 26.09创新】【AI】【模型加速】ModelFS用户态模型加载优化方案 | Developing | sig-kernel | [@yubo-liu](https://gitcode.com/yubo-liu)     | ISO | kernel |
| [2570](https://atomgit.com/openeuler/release-management/issues/2570) | 【openEuler 26.09创新】【AI Infra】【推理加速】多级KV缓存+SSD直访，结合UB加速跨节点KV传输，长序列降低TTFT | Developing | sig-kernel,sig-Long | [@qiao-yifan4](https://gitcode.com/qiao-yifan4,[@chloroethylene](https://gitcode.com/chloroethylene)     | ISO | kernel, LMCache,LMCache-Ascend |



# 需求/特性反馈基本流程 <br />
1、开发者/sig在本贴的表格中填写要合入该版本的需求/特性，并同时填写需求issue及链接 （请在收集截止时间前提交）      <br>
2、申请在版本release management sig例会上评审需求 （owner或者SIG maintainer参会）
<br><br>
