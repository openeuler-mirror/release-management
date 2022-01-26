# Version Info
openEuler 22.03 LTS是基于5.10内核的长周期LTS版本（参见[版本生命周期](https://www.openeuler.org/zh/other/lifecycle/)），面向服务器、云、边缘计算和嵌入式场景，提供更多新特性和功能，给开发者和用户带来全新的体验，服务更多的领域和更多的用户。<br />

# Release Plan

| Stage  name          | Begin time | End time   | Days | Note                                      |
| -------------------- | ---------- | ---------- | ---- | ----------------------------------------- |
| Collect key features | 2021/11/1  | 2021/12/30 | 60   | 版本需求收集                              |
| Develop              | 2021/11/8  | 2022/2/7   | 90   | 特性完成开发和自验证，代码提交合入22.03 LTS-Next    |
| Kernel freezing      | 2022/1/20  | 2022/1/24  | 5    | 内核冻结                                  |
| Branch 22.03-LTS     | 2022/1/24  | 2022/1/24   | 1    | 拉版本分支：21.09(决议) -> 22.03 LTS-Next -> 22.03 LTS |
| Build & Alpha        | 2022/1/25   | 2022/1/31  | 5    | 版本启动构建  & 开发自验证              |
| Test round 1         | 2022/2/14 | 2022/2/18 | 5    | 版本启动测试                              |
| Beta Version release | 2022/2/21 | 2022/2/23 | 3    | Beta版本发布                              |
| Test round 2         | 2022/2/22 | 2022/2/25 | 5    |                                           |
| Test round 3         | 2022/2/28 | 2022/3/4  | 5    |                                           |
| Test round 4         | 2022/3/7  | 2022/3/11 | 5    |                                           |
| Test round 5         | 2022/3/15 | 2022/3/17 | 3    |                                           |
| Release              | 2022/3/30 | 2022/3/30 | 1    |                                           |


# 代码合入说明
2022/1/24拉取22.03版本分支后，后续在22.03版本上变更的代码请同步合入 22.03 LTS、22.03 LTS-Next、Master三个分支。


# Feature list
#### 状态说明：
- Discussion(方案讨论，需求未接受)
- Developing(开发中)
- Testing(测试中)
- Accepted(已验收)

|no|feature|status|sig|owner|
|:----|:---|:---|:--|:----|
|[I4H9BC](https://gitee.com/openeuler/release-management/issues/I4H9BC)|新增支持RISC-V 镜像|Discussion|RISC-V|[@xuzhou zhang](https://gitee.com/whoisxxx), [@xijing](https://gitee.com/xijing666)|
|[I4IM2L](https://gitee.com/openeuler/release-management/issues/I4IM2L)|GCC自动反馈优化相关软件包引入及优化效果增强|Discussion|Compiler|[@ma-mingze](https://gitee.com/ma-mingze), [@Haijian.Zhang](https://gitee.com/haijianzhang), [@eastb233](https://gitee.com/eastb233)|
|[I4N83C](https://gitee.com/openeuler/release-management/issues/I4N83C)|openGauss默认集成到openEuler操作系统中|Discussion|DB|[@zhang_xubo](https://gitee.com/zhang_xubo), [@bzhaoop](https://gitee.com/bzhaoop)|
|[I4O21W](https://gitee.com/openeuler/release-management/issues/I4O21W)|新增支持容器场景在离线混合部署|Developing|CloudNative|[@Vanient](https://gitee.com/Vanient)|
|[I4PM21](https://gitee.com/openeuler/release-management/issues/I4PM21)|StratoVirt安全容器支持直通设备热插拔|Developing|Virt|[@frankyj915](https://gitee.com/frankyj915), [@imxcc](https://gitee.com/imxcc)|
|[I4PMNN](https://gitee.com/openeuler/release-management/issues/I4PMNN)|libcareplus提供Qemu热补丁能力|Developing|Virt|[@mdsc](https://gitee.com/mdsc), [@imxcc](https://gitee.com/imxcc)|
|[I4PLVR](https://gitee.com/openeuler/release-management/issues/I4PLVR)|IO智能多流|Developing|Kernel|[@hongrongxuan](https://gitee.com/barbo)|
|[I4PMYT](https://gitee.com/openeuler/release-management/issues/I4PMYT)|新增支持gazelle高性能用户态协议栈|Developing|sig-high-performance-network|[@wu-changsheng](https://gitee.com/wu-changsheng)|
|[I4QL70](https://gitee.com/openeuler/release-management/issues/I4QL70)|支持树莓派|Developing|RaspberryPi|[@woqidaideshi](https://gitee.com/woqidaideshi)|
|[I4S7C0](https://gitee.com/openeuler/release-management/issues/I4S7C0)|支持OpenStack Train/Wallaby版本|Developing|SIG-OpenStack| [@joec88](https://gitee.com/joec88) [@huangtianhua](https://gitee.com/huangtianhua) [@xiyuanwang](@https://gitee.com/xiyuanwang)  [@zh-f](https://gitee.com/zh-f)  [@liksh](https://gitee.com/liksh) [@zhangy1317](https://gitee.com/zhangy1317) |
|I4S8D3](https://gitee.com/openeuler/release-management/issues/I4S8D3)|支持xfce|Developing|xfce|[@zhang__3125](https://gitee.com/zhang__3125) [@dwl301](https://gitee.com/dwl301)|
<br />
现启动版本需求收集，欢迎各sig maintainer和社区开发者们积极反馈和交流，<br />
<br />
需求反馈基本流程： <br />
1、开发者/sig在本贴的表格中填写要合入22.03-LTS的需求/特性，并同时填写需求issue <br />
2、申请在版本release management例会上评审需求 
<br /><br />


# master部分代码需要回合到22.03-LTS-Next的提示（已邮件公告）
11月在release sig会议上多方讨论和投票、及咨询TC意见，RM团队综合决议：<br />
22.03-LTS-Next基线改从21.09分支拉取（2021/11/17），并已在openEuler release微信群做了同步知会。<br />
<br />
由于openEuler 21.09版本是在8月11号从Master拉分支（https://gitee.com/openeuler/community/pulls/2567）<br />
因此2021/8/11这个时间点之后的Master PR，可能需要回合到22.03-LTS-Next分支。<br />
请各sig maintainer、开发者们知悉此情况，做好相关代码的回合（可利用/sync命令做分支代码同步），确保22.03-LTS-Next分支上的代码版本符合预期（最新？）。
<br /><br />
