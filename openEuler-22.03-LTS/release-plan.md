# Version Info
openEuler 22.03 LTS是基于5.10内核的长周期LTS版本（参见[版本生命周期](https://www.openeuler.org/zh/other/lifecycle/)），面向服务器、云、边缘计算和嵌入式场景，提供更多新特性和功能，给开发者和用户带来全新的体验，服务更多的领域和更多的用户。<br />

# Release Plan

| Stage  name          | Begin time | End time   | Days | Note                                      |
| -------------------- | ---------- | ---------- | ---- | ----------------------------------------- |
| Collect key features | 2021/11/1  | 2021/12/30 | 60   | 版本需求收集                              |
| Develop              | 2021/11/8  | 2022/2/7   | 90   | 特性完成开发和自验证，代码提交合入Master    |
| Kernel freezing      | 2022/1/25  | 2022/1/30  | 5    | 内核冻结                                  |
| Branch               | 2022/2/7   | 2022/2/7   | 1    | 拉版本分支：Master -> 22.03 LTS-Next -> 22.03 LTS |
| Build & Alpha        | 2022/2/7   | 2022/2/11  | 5    | 版本DailyBuild  & 开发自验证              |
| Test round 1         | 2022/2/14 | 2022/2/18 | 5    | 版本启动测试                              |
| Beta Version release | 2022/2/21 | 2022/2/23 | 3    | Beta版本发布                              |
| Test round 2         | 2022/2/22 | 2022/2/25 | 3    |                                           |
| Test round 3         | 2022/2/28 | 2022/3/4  | 5    |                                           |
| Test round 4         | 2022/3/7  | 2022/3/11 | 5    |                                           |
| Test round 5         | 2022/3/15 | 2022/3/17 | 3    |                                           |
| Release              | 2022/3/30 | 2022/3/30 | 1    |                                           |


# Feature list
#### 状态说明：
- Discussion(方案讨论，需求未接受)
- Developing(开发中)
- Testing(测试中)
- Accepted(已验收)

|no|feature|status|sig|owner|
|:----|:---|:---|:--|:----|
|[I4H9BC](https://gitee.com/openeuler/release-management/issues/I4H9BC)|新增支持RISC-V 镜像|Discussion|RISC-V|[@xuzhou zhang](https://gitee.com/whoisxxx), [@xijing](https://gitee.com/xijing666)|



现启动版本需求收集，欢迎各sig maintainer和社区开发者们积极反馈和交流，<br />
<br />
需求反馈基本流程： <br />
1、开发者/sig在本贴的表格中填写要合入22.03-LTS的需求/特性，并同时填写需求issue <br />
2、申请在版本release management例会上评审需求 
