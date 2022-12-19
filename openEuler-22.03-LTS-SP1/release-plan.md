# Version Info
openEuler 22.03 LTS SP1 是22.03-LTS版本增强扩展版本（参见[版本生命周期](https://www.openeuler.org/zh/other/lifecycle/)），面向服务器、云、边缘计算和嵌入式场景，持续提供更多新特性和功能扩展，给开发者和用户带来全新的体验，服务更多的领域和更多的用户。<br>


# Release Plan

| Stage  name            | Begin time | End time   | Days | Note                                                       |
| --------------------   | ---------- | ---------- | ---- | -----------------------------------------                  |
| Collect key features   | 2022/9/16  | 2022/10/15 | 30   | 版本需求收集                                                |
| 变更检查阶段1           | 2022/10/8  | 2022/11/8  | 30   | Review软件包变更（升级/退役/淘汰）                            |
| 变更检查阶段2           | 2022/10/16 | 2022/10/16 | 1    | Review基础设施相关变更                                       |
| Develop                | 2022/10/8  | 2022/11/8  | 30   | 这个时间段内完成开发，合入22.03  LTS-Next                     |
| Kernel freezing        | 2022/11/3  | 2022/11/8  | 6    | 内核冻结                                                    |
| LTS-Next mass rebuild  | 2022/11/9  | 2022/11/10 | 2    | 22.03-LTS Next分支大规模编译构建                              |
| 变更检查阶段3           | 2022/11/11 | 2022/11/12 | 3    | 22.03-LTS Next分支发起软件包淘汰（持续编译/构建失败）评审        |
| Branch                 | 2022/11/13 | 2022/11/15 | 3    | 从22.03 LTS-Next拉SP1版本分支                                 |
| Build & Alpha          | 2022/11/16 | 2022/11/22 | 7    | 22.03-LTS SP1版本DailyBuild  & 开发自验证                      |
| Test round 1           | 2022/11/23 | 2022/11/29 | 7    | 22.03-LTS SP1版本启动集成测试                                  |
| 变更检查阶段4           | 2022/11/30 | 2022/11/30 | 1    | 22.03-LTS SP1版本分支发起软件包淘汰（持续编译/构建失败）评审      | 
| Beta Version release   | 2022/12/1  | 2022/12/2  | 2    | 22.03-LTS SP1 Beta版本发布                                    |
| Test round 2           | 2022/12/2  | 2022/12/8  | 7    | 全量SIT验证                                                   |
| 变更检查阶段5           | 2022/12/9  | 2022/12/9  | 1    | 22.03-LTS SP1版本分支代码冻结：受限合入，原则上仅允许bug fix     | 
| Test round 3           | 2022/12/9  | 2022/12/15 | 7    | 全量SIT验证，版本分支代码冻结：管控合入，原则上只允许bug fix      |
| Test round 4           | 2022/12/16 | 2022/12/22 | 7    | 回归测试                                                      |
| Test round 5           | 2022/12/23 | 2022/12/29 | 7    | 回归测试                                                      |
| Release                | 2022/12/30 | 2022/12/30 | 1    | 社区Release版本发布评审                                        |

# 代码合入说明
- 22.03 LTS SP1版本代码继承自22.03 LTS NEXT分支 <br>
- 新特性代码请及时合入版本&自验证，跟随整体计划赶在第一轮转测试



# Feature list
状态说明：Discussion(方案讨论，需求未接受)、 Developing(开发中)、 Testing(测试中)、 Accepted(已验收) <br>
发布方式：ISO、EPOL、oepkgs、独立发布等

|no|feature|status|sig|owner|发布方式|涉及软件包列表|
|:----|:---|:---|:--|:----|:----|:----|
|[I5RDEG](https://gitee.com/openeuler/release-management/issues/I5RDEG) | DDE组件更新支持服务器场景优化 | Accepted | sig-DDE | [@weidongkl](https://gitee.com/weidongkl) [@panchenbo](https://gitee.com/panchenbo) | EPOL |     |
|[I5RDGW](https://gitee.com/openeuler/release-management/issues/I5RDGW)|新增软件更新工具支持|Accepted|sig-DDE|[@weidongkl](https://gitee.com/weidongkl) [@panchenbo](https://gitee.com/panchenbo)|EPOL|deepin-upgrade-tool|
|[I5RDJS](https://gitee.com/openeuler/release-management/issues/I5RDJS)|新增备份还原功能支持|Accepted|sig-Migration|[@blueblue](https://gitee.com/blublue)|EPOL|ubackup|
|[I5T3MB](https://gitee.com/openeuler/release-management/issues/I5T3MB)|新增ROS基础版和ROS2基础版|Accepted|sig-ROS|[@anchuanxu](https://gitee.com/anchuanxu) [@xiao_yun_wang](https://gitee.com/xiao_yun_wang) [@wuwei_plct](https://gitee.com/wuwei_plct)|EPOL|[ros_comm](https://gitee.com/src-openeuler/ros_comm) [ros2_base](https://gitee.com/src-openeuler/ros2_base)|
|[I5TT8E](https://gitee.com/openeuler/release-management/issues/I5TT8E)|发布kiran-desktop 2.4版本|Accepted|sig-KIRAN-DESKTOP|[@tangjie02](https://gitee.com/tangjie02)|EPOL|kiran-control-panel,kiran-cc-daemon,kiran-qt5-integration,kiran-session-manager,kiran-log|
|[I5U6JV](https://gitee.com/openeuler/release-management/issues/I5U6JV)|支持树莓派|Accepted|sig-RaspberryPi|[@woqidaideshi](https://gitee.com/woqidaideshi)|EPOL|raspberrypi-firmware,raspberrypi-bluetooth,raspi-config,pigpio,raspberrypi-userland,raspberrypi-eeprom|
|[I5Y11K](https://gitee.com/openeuler/release-management/issues/I5Y11K)|openEuler 22.03 LTS SP 南向兼容：支持intel SPR|Accepted|||ISO|kernel,gcc|
|[I5Y16U](https://gitee.com/openeuler/release-management/issues/I5Y16U)|兼容HG2号和3号|Accepted|sig-Compatibility-Infra||ISO||
|[I5Y18K](https://gitee.com/openeuler/release-management/issues/I5Y18K)|支持openstack Train版本|Accepted|sig-openstack||EPOL||
|[I5Y1CR](https://gitee.com/openeuler/release-management/issues/I5Y1CR)|KubeOS支持一体机|Accepted|Kernel||EPOL||
|[I5Y1DS](https://gitee.com/openeuler/release-management/issues/I5Y1DS)|基于A-ops现有CVE管理能力扩展|Accepted|sig-ops||EPOL||
|[I5Y1HK](https://gitee.com/openeuler/release-management/issues/I5Y1HK)|降低secGear在空载下的CPU占用率|Accepted|Kernel||ISO||
|[I5Y1I8](https://gitee.com/openeuler/release-management/issues/I5Y1I8)|HybridSched虚拟机在离线混部|Accepted|Virt||EPOL||
|[I5Y1J1](https://gitee.com/openeuler/release-management/issues/I5Y1J1)|实时非实时系统混合部署支持树莓派|Accepted|sig-embedded||embedded||
|[I5Y1K3](https://gitee.com/openeuler/release-management/issues/I5Y1K3)|分布式软总线生态互通互联|Accepted|sig-Edge||EPOL||
|[I5YL35](https://gitee.com/openeuler/release-management/issues/I5YL35)|支持embedded版本|Accepted|sig-embedded||embedded||
|[I605QY](https://gitee.com/openeuler/release-management/issues/I605QY)|支持generic vDPA Device|Accepted|sig-Kernel,sig-Virt||ISO|kernel,qemu|
|[I609I2](https://gitee.com/openeuler/release-management/issues/I609I2)|Tensorflow中Intel AMX支持|Accepted|ai|[@Jincheng](https://gitee.com/wisespreading) [@yefeng](https://gitee.com/YeFeng_24) [@Sinever](https://gitee.com/Sinever)|EPOL|python3-tensorflow,python3-absl-py,flatbuffers,python3-flatbuffers,python3-keras, libclang, python3-tensorflow-estimator, python3-tensorboard|
|[I61CMT](https://gitee.com/openeuler/release-management/issues/I61CMT)|openEuler WSL package支持|Accepted|sig-Infrastructure|[@mywaaagh_admin](https://gitee.com/mywaaagh_admin)|Microsoft Store appx bundle||
|[I61DRR](https://gitee.com/openeuler/release-management/issues/I61DRR)|Gazelle支持ceph client和rpc框架|Accepted|sig-high-performance-network|[@wu-changsheng](https://gitee.com/wu-changsheng)|oepkgs|Gazelle,dpdk,lwip| 

现启动版本需求/特性收集，欢迎各sig maintainer和社区开发者们积极反馈和交流。


# 需求/特性反馈基本流程 <br />
1、开发者/sig在本贴的表格中填写要合入22.03 LTS SP1的需求/特性，并同时填写需求issue及链接 （请在收集截止时间前提交）      <br>
2、申请在版本release management sig例会上评审需求 （owner或者SIG maintainer参会）
<br><br>
