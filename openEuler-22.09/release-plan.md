# Version Info
openEuler 22.09 是基于5.10内核的创新版本（参见[版本生命周期](https://www.openeuler.org/zh/other/lifecycle/)），面向服务器、云、边缘计算和嵌入式场景，提供更多新特性和功能，给开发者和用户带来全新的体验，服务更多的领域和更多的用户。<br>


# Release Plan

| Stage  name          | Begin time | End time   | Days | Note                                      |
| -------------------- | ---------- | ---------- | ---- | ----------------------------------------- |
| Collect key features | 2022/4/15  | 2022/6/15 | 60   | 收集22.09版本关键特性（各SIG自行录入release-plan）   |
| 变更检查阶段1 | 2022/4/29 | 2022/4/29 | 1 | Review基础设施相关变更 |
| 变更检查阶段2 | 2022/5/20 | 2022/5/30 | 10 | Review软件包变更（升级/退役/淘汰） |
| Develop              | 2022/4/15  | 2022/7/31   | 105   | 特性完成开发和自验证，代码提交合入master    |
| Master Pre-build      | 2022/5/1  | 2022/6/30  | 30    | Master滚动构建，修复构建问题     |
| Master mass rebuild      | 2022/7/1  | 2022/7/10  | 10    | Master主线大规模编译构建     |
| 变更检查阶段3      | 2022/7/10  | 2022/7/12  | 3    | Master主线发起软件包淘汰（持续编译/构建失败）评审     |
| Branch 22.09 & Build   | 2022/7/13  | 2022/7/20   | 16    | 22.09版本从Master分支拉取（版本范围的包），构建版本 |
| Kernel freezing    | 2022/7/16   | 2022/7/20  | 15   | 内核代码冻结，管控合入   |
|版本分支更新|2022/7/21|2022/7/31| 11 |组件补丁更新（漏洞、缺陷、编译、构建），软件包自验证（alpha测试）|
|Beta冻结| 2022/8/1|2022/8/1| 0 |Bata版本冻结|
| Test round 1         | 2022/8/1 | 2022/8/7 | 7    | Beta版本测试                           |
| 变更检查阶段4| 2022/8/8   | 2022/8/8  | 1    | 版本分支发起软件包淘汰（持续编译/构建失败）评审 | 
|Final冻结|2022/8/9|2022/8/9|1|Release版本基线冻结，启动全量编译构建|   
| Test round 2         | 2022/8/11 | 2022/8/17 | 7    | 版本全量集成测试                         |
| 变更检查阶段5| 2022/8/18   | 2022/8/22  | 4    | 版本分支代码冻结：受限合入，原则上仅允许bug fix | 
| Test round 3         | 2022/8/23 | 2022/8/29  | 7    |  版本分支代码冻结：管控合入，原则上只允许bug fix   |
| Test round 4         | 2022/9/2  | 2022/9/8 | 7    |   回归测试      |
| Test round 5         | 2022/9/12 | 2022/9/18 | 7    |  回归测试 (9.20~9.29预留buffer)     |
| Release              | 2022/9/30 | 2022/9/30 | 1    |          社区Release版本发布评审                                 |


# 代码合入说明
创新版本代码继承master分支 <br>
// 新特性代码请及时合入版本&自验证，跟随整体计划赶在第一轮转测试


# Feature list
状态说明：Discussion(方案讨论，需求未接受)、 Developing(开发中)、 Testing(测试中)、 Accepted(已验收) <br>
发布方式：ISO、EPOL、oepkgs、独立发布等

|no|feature|status|sig|owner|发布方式|涉及软件包列表|
|:----|:---|:---|:--|:----|:----|:----|
|[I5BIHV](https://gitee.com/openeuler/release-management/issues/I5BIHV)|支持OpenStack Yoga版本，并且引入Helm组件|Developing|SIG-OpenStack|[@joec88](https://gitee.com/joec88) [@huangtianhua](https://gitee.com/huangtianhua) [@xiyuanwang](@https://gitee.com/xiyuanwang)  [@zh-f](https://gitee.com/zh-f)  [@liksh](https://gitee.com/liksh) [@zhangy1317](https://gitee.com/zhangy1317)|     |     |
|[I5BIM9](https://gitee.com/openeuler/release-management/issues/I5BIM9)|正式发布联通开源的OpenStack部署工具opensd，支持OpenStack基本部署|Developing|SIG-OpenStack|[@joec88](https://gitee.com/joec88) [@huangtianhua](https://gitee.com/huangtianhua) [@xiyuanwang](@https://gitee.com/xiyuanwang)  [@zh-f](https://gitee.com/zh-f)  [@liksh](https://gitee.com/liksh) [@zhangy1317](https://gitee.com/zhangy1317)|     |     |
|[I5ASLE](https://gitee.com/openeuler/release-management/issues/I5ASLE?from=project-issue)|发布kiran-desktop 2.3版本|Developing|sig-KIRAN-DESKTOP|[@tangjie02](https://gitee.com/tangjie02)|EPOL|kiran-cpanel-xxx,kiran-control-panel,kiran-qt5-integration,kiran-widgets-qt5|
|[I5BJ7W](https://gitee.com/openeuler/release-management/issues/I5BJ7W)|支持树莓派|Developing|sig-RaspberryPi|[@woqidaideshi](https://gitee.com/woqidaideshi)|EPOL|raspberrypi-kernel,raspberrypi-firmware,raspberrypi-bluetooth,raspi-config,pigpio,raspberrypi-userland,raspberrypi-eeprom|
|[I5BL1G](https://gitee.com/openeuler/release-management/issues/I5BL1G)|支持 RK3399|Developing|sig-RaspberryPi|[@woqidaideshi](https://gitee.com/woqidaideshi) [@tideao](https://gitee.com/tideao)|     |     |
|[I5BMO2](https://gitee.com/openeuler/release-management/issues/I5BMO2)|DDE组件更新支持服务器场景优化|Developing|sig-DDE|[@weidongkl](https://gitee.com/weidongkl) [@panchenbo](https://gitee.com/panchenbo)|EPOL| |
|[I5BMNH](https://gitee.com/openeuler/release-management/issues/I5BMNH)|新增软件更新工具支持|Developing|sig-DDE|[@weidongkl](https://gitee.com/weidongkl) [@panchenbo](https://gitee.com/panchenbo)|EPOL|deepin-upgrade-tool|
|[I5BMMP](https://gitee.com/openeuler/release-management/issues/I5BMMP)|新增备份还原功能支持|Developing|sig-Migration|[@blueblue](https://gitee.com/blublue)|EPOL|ubackup|
|[I545LZ](https://gitee.com/openeuler/release-management/issues/I545LZ)|openEuler 22.09和22.03 SP1支持鲲鹏底软IO能力（存储、usb、SPI、Pcie、IIC、CXL、GPU和GPIO等）|Developing||[@kongzizaixian](https://gitee.com/kongzizaixian)|iso||
|[I545LT](https://gitee.com/openeuler/release-management/issues/I545LT)|openEuler 22.09和22.03 SP1支持鲲鹏性能调优和调测调优（Rasdaemon、Ras、etm、perf、wayca-SC、Mem-kind、HCCS、Hikptool等）|Developing||[@kongzizaixian](https://gitee.com/kongzizaixian)|iso||
|[I545LP](https://gitee.com/openeuler/release-management/issues/I545LP)|openEuler 22.09和22.03 SP1支持鲲鹏高速网络功能（DPDK、UB、RDMA-core、ROH、Roce、NIC等）|Developing||[@kongzizaixian](https://gitee.com/kongzizaixian)|iso||
|[I545LH](https://gitee.com/openeuler/release-management/issues/I545LH)|openEuler 22.09和22.03 SP1支持鲲鹏加速器功能（UADK、UADK_engine、starS、SDMA、ACC等）|Developing||[@kongzizaixian](https://gitee.com/kongzizaixian)|iso||
|[I545M5](https://gitee.com/openeuler/release-management/issues/I545M5)|openEuler 22.09和22.03 SP1 测试工具能力（pktgen）|Developing||[@kongzizaixian](https://gitee.com/kongzizaixian)|EPOL||
|[I59BQI](https://gitee.com/openeuler/release-management/issues/I59BQI)|【openEuler 22.09】openEuler 22.09 支持 pod带宽管理特性|Developing||[@wo_cow](https://gitee.com/wo_cow)|iso||
|[I5BM96](https://gitee.com/openeuler/release-management/issues/I5BM96)|[openEuler 22.09]StratoVirt 2.0支持标准虚拟化|Developing|||iso||
|[I5BMD4](https://gitee.com/openeuler/release-management/issues/I5BMD4)|[openEuler 22.09]集成k3s边缘解决方案|Developing|||EPOL||
|[I5BMFH](https://gitee.com/openeuler/release-management/issues/I5BMFH)|[openEuler 22.09]智能多流技术，延长ssd磁盘寿命|Developing|||iso||
|[I5BMGZ](https://gitee.com/openeuler/release-management/issues/I5BMGZ)|[openEuler 22.09]国密算法适配|Developing|||iso||
|[I5BMI3](https://gitee.com/openeuler/release-management/issues/I5BMI3)|[openEuler 22.09]libstorage高性能用户态IO|Developing|||iso||
|[I5H6DI](https://gitee.com/openeuler/release-management/issues/I5H6DI)|增强embedded版本分布式软总线及混合部署能力|Discussion|sig-yocto|[@linzichang](https://gitee.com/linzichang) [@beiling.xie](https://gitee.com/beilingxie) [@zhengjunling](https://gitee.com/junling_zheng) [@ilisimin](https://gitee.com/open_euler/dashboard/members/ilisimin) [@任慰](https://gitee.com/open_euler/dashboard/members/vonhust)|embedded|yocto-meta-openeuler,dsoftbus_standard, yocto-embedded-tools, OpenAMP|

<br>
现启动版本需求/特性收集，欢迎各sig maintainer和社区开发者们积极反馈和交流，<br>
<br>

# 需求/特性反馈基本流程 <br />
1、开发者/sig在本贴的表格中填写要合入22.09的需求/特性，并同时填写需求issue及链接 （请在收集截止时间前提交）      <br>
2、申请在版本release management sig例会上评审需求 （owner或者SIG maintainer参会）
<br><br>
