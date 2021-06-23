openEuler 创新版本大约每6个月发布一次新版本，并在发布后的6个月内持续为该发行版提供软件包更新维护（bugfix、CVE漏洞修复），开发者和社区爱好者可尝鲜该创新版本，第一时间获得自由和开源软件项目的最新stable版本；
oepnEuler创新版本经过社区sig组和QA团队充分测试，推荐给开发者、openEuler社区贡献者和Linux爱好者使用。

### 开发时间表
openEuler创新版本大约每6个月发布一次，但不排除受版本质量、社区关键组件构建进度影响到导致的严格的发布时间执行，且创新版本的里程碑发行版均需要由各个sig和QA团队的充分测试验证，已达到openEuler社区版本质量发行标准的情况下允许发布，关于具体的发布计划和发布进展，请关注openEuler社区relase management sig [版本计划](https://gitee.com/openeuler/release-management/tree/master/openEuler-20.09)

### 开发流程
openEuler创新版本是基于openEuler社区master主干中“分支”出来的，master主干持续不断的向前滚动开发。在openEuler创新版本发布计划中拉分支点阶段且该时间点之前各关键任务项均已完成，将拉出创新版本分支，master主线继续向前开发；
创新分支拉出来之后，在里程碑（测试版，最终版）发布之前的一段时间内，分支冻结持续有效，这可以保证软件包经过迭代测试验证后质量逐渐趋于稳定。



| 任务/里程碑 |开始时间| 周期 |
---|:--:|---:
| 规划与发展 | 上*一版本的**分支点*确定之后的一周内 | ~ |
| 变更检查点：需要*大量重建的*变更的提案截止日期| *大规模重建*减去**3周** | ~ |
| 更改检查点：系统范围更改的建议截止日期 | *大规模重建*减去**1周** | ~ |
| **大规模重建** | *分支点数*减去**5周** | 直到*分支点* |
| 变更检查点：自包含变更的提案截止日期 | *分支点数*减去**3周** | ~ |
| **分支点** | *Beta 版本Go_No_Go_Meeting*减去**5周** | ~ |
| 更改检查点：完成截止日期（可测试）| **当天**为*分支点* | ~ |
| 内核冻结 |*分支点*加**1周** | 在*最终版本（GA）之前有效* |
| 更改检查点 | **当天**的*测试版冻结* | 要求一直有效，直到*EOL* |
| Beta冻结 | *首选Beta目标*减去**3周** |QA转测试开始有效，直到*Beta发布* |
| 更改检查点：100％代码完成期限 | **当天**的*测试版冻结* | ~ |
| Beta版本候选 | *Beta冻结*后的任何时间 | 直到*Beta发布* |
| **Beta 版本Go_No_Go_Meeting**| 计划的*首选Beta目标* **减去五天**（如果不执行，则重复） | ~ |
| 最终冻结 | *首选最终目标*减去**2周** | 直到*最终版本（GA）* |
| 最终版本候选 | *最终冻结*后的任何时间 | 直到*最终版本（GA）* |
| **发布版本[Go_No_Go_Meeting** | 计划的*最终发布（GA）* **减去五天**（如果不执行则重复） | ~ |
| 维护周期 | 以*最终发行（GA）时间为准* | 6**个月** |
| 停止维护时间（EOL） | 下一个创新版的最终发行版（GA）时间的当天 | 不适用 |



### 版本计划管理方式
openEuler社区版本计划及关键里程碑时间表由release management sig提出，并收集TC委员会、包管理委员会、QA团队、工程团队意见，最终确定openEuler各个正式发布版本的关键任务及其对应的时间表，各个sig和团队围绕该时间表指定自己团队的计划；
### 版本计划
[openEuler 20.09 版本计划](https://gitee.com/openeuler/release-management/blob/master/openEuler-20.09/openEuler-20.9%20Release%20plan.md)

### 版本应急计划
如果版本大规模构建未能按照[版本计划](https://gitee.com/openeuler/release-management/tree/master/openEuler-20.09)完成，则从该分支点开始的所有后续里程碑都将顺延一周，直到大规模构建完成。
如果openEuler 创新版本Beta Go_No_Go_Meeting结果为“不同意”，则重新计划里程碑，其后续里程碑将遵循以下规则：
*  Beta从首选目标到目标延期不影响最终发行（GA）日期，最终发布日期扔保留在“首选最终目标”
*  如果最终的Go_No_Go_Meeting结果为“不发布”，则该里程碑和随后的里程碑将推迟一周。
*   Go_No_Go_Meeting从relase management sig [版本计划](https://gitee.com/openeuler/release-management/tree/master/openEuler-20.09)和[质量保证](https://gitee.com/openeuler/QA)"质量检查")团队处获取详细信息。


### 版本维护时间表
openEuler 20.09版本已于2020.09.30正式发布，该版本将维护到2021.3.30截止；
openEuler 21.03版本信息详见relase management sig [版本计划](https://gitee.com/openeuler/release-management/tree/master/openEuler-20.09)
### 版本维护周期策略
openEuler创新版本聚集于自由和开源软件的持续创新，版本开发、发布节奏高效且快速。如果您希望使用系统功能稳定且版本生命周期更长的发行版，推荐您使用openEuler LTS版本，有关openEuler LTS版本详细信息，请参考页面

### 版本生命周期管理
openEuler创新版本开发周期大约为6个月，该版本正式发布后的6个月内持续维护（EOL），6个月维护周期结束后，oepnEuler社区将不再持续为该版本提供更新维护服务，该版本中的各个软件包版本也同步将停止更新；
![openEuler创新版本生命周期管理](https://images.gitee.com/uploads/images/2021/0511/195939_e8491942_5603730.png "openEuler社区创新版本生命周期管理.png")
### 历史版本发布信息
历史发行版本（EOL停止维护）