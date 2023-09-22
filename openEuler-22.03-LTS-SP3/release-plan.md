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
| [I80F3Y](https://gitee.com/openeuler/release-management/issues/I80F3Y) | 支持Lustre server软件包 | Discussion | sig-SDS | [@xin3liang](https://gitee.com/xin3liang) | EPOL | lustre, lustre-release, e2fsprogs |
| [I83JRC](https://gitee.com/openeuler/release-management/issues/I83JRC) | eNFS特性合入 | Discussion | sig-kernel | [@mingqian218472](https://gitee.com/mingqian218472) | ISO | nfs,sunrpc |

现启动版本需求/特性收集，欢迎各sig maintainer和社区开发者们积极反馈和交流。


# 需求/特性反馈基本流程 <br />
1、开发者/sig在本贴的表格中填写要合入22.03 LTS SP3的需求/特性，并同时填写需求issue及链接 （请在收集截止时间前提交）      <br>
2、申请在版本release management sig例会上评审需求 （owner或者SIG maintainer参会）
<br><br>
