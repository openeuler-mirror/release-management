# openEuler 维护版本特性管理规范

Update版本发布更新基于 openEuler 各个生命周期内的 LTS 版本分支的CVE漏洞修复和BUGFIX。版本计划、需求管理、特性开发及代码检测等均通过release-manangement SIG 完成。

## 新引入特性

openEuler LTS（长周期支持）版本旨在为社区用户提供稳定、高质量的版本体验。因此对维护版本新特性合入采取强质量管理策略，特性引入需满足以下条件，方可获准引入openEuler LTS 版本

![update](./Pictures/update流程.png)

### 新特性引入checklist

| 检查项              | 关键动作                                                     |
| ------------------- | ------------------------------------------------------------ |
| 意见收集            | 在自己的sig组内收集意见,获得本组成员同意；                   |
| 代码提交            | 1、在community上提对应分支的pr，建立仓库：https://gitee.com/openeuler/community/ ；2、确认新特性代码合入src-openEuler下对应仓库； |
| 获取QA测试报告      | 获取测试报告模板：https://gitee.com/openeuler/QA/tree/master/Test_Result ，可在该仓库在的Test_Result文件夹中找到对应分支的update测试报告模板，Test_Strategy 文件夹下找到对应分支的测试策略文档。 |
| 会议准备            | 到release sig申报议题，申报方式：将议题邮件发送release@openeuler.org；准备申报材料，材料内容可包含：新特性介绍，对社区的影响，包的依赖关系，构建结果，质量验证情况等； |
| 参加Release SIG会议 | 参加release sig会议，并获得sig组成员同意即可纳入update流程。 |

### update发布流程

目前在维护的版本有openEuler-20.03-LTS-SP1、openEuler-20.03-LTS-SP3、openEuler-22.03-LTS、openEuler-22.03-LTS-SP1。

到发布issue: https://gitee.com/openeuler/release-management/issues/I6G5JO?from=project-issue 相应的分支issue下评论标题、issue、pr链接。需要注意，如果需要在该周发布，则需要在当周的周三中午前完成评论。一般会在周五晚完成发布。

- 开发者基于src-openEuler 组织下各软件包issue提交pr完成CVE漏洞修复和BUGFIX，并在OBS编译出包

- 版本经理基于cve-manager工具以及开发者反馈确定Update版本发布范围

- 版本开发人员完成将待测软件包放入测试仓，进行开发者自验证及ISO构建

- AT测试、软件包测试

- 软件包发布至发布仓、安全公告等发布件整理同步

#### 版本发布时间表

openEuler Update版本约每1周发布一次，但不排除受版本质量、CVE漏洞修复进度影响到导致的未严格地执行发布时间，且Update版本的里程碑发行版均需要由各个sig和QA团队的充分测试验证，已达到openEuler社区版本质量发行标准的情况下允许发布，关于具体的发布流程如下：

| 任务/里程碑         | 开始时间           | 周期 |
| ------------------- | ------------------ | ---- |
| Update 需求收集     | 每周一，节假日顺延 | ~    |
| Update 需求冻结     | 每周三中午 12:00   | ~    |
| Update 自验证及转测 | 2-3 Days           | ~    |
| Update 发布         | 周五               | ~    |

###  

#### Update版本计划管理方式

经Release management  SIG 确定后，每周依照版本发布流程例行发布Update版本，同时社区安全委员会如有紧急修复漏洞需要，Release SIG 会配合发布紧急修复版本。

#### Update版本应急计划

如因节假日关系未能足够时间运作Update版本发布流程，则从Update版本需求收集点开始后续里程碑都将顺延。 如 Release SIG 评估无需发布本次Update，将在下一周重新启动Update版本发布流程。



 

