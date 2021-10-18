# Version Info
按openEuler社区生命周期策略定义，openEuler 20.03 LTS SP3是当前20.03-LTS最后一个SP版本，支撑长周期维护。<br />
需求纳入和特性开发策略上，以版本质量和稳定性优先。

# Release Plan

| Stage  name          | Begin time | End time   | Days | Note                                      |
| -------------------- | ---------- | ---------- | ---- | ----------------------------------------- |
| Collect key features | 2021/9/22  | 2021/10/15 | 24   | 版本需求收集                              |
| Develop              | 2021/10/8  | 2021/11/8  | 30   | 这个时间段内完成开发，合入20.03  LTS-Next |
| Kernel freezing      | 2021/11/3  | 2021/11/7  | 5    | 内核冻结                                  |
| Branch               | 2021/11/9  | 2021/11/9  | 1    | 从20.03 LTS-Next拉SP3版本分支            |
| Build & Alpha        | 2021/11/9  | 2021/11/14 | 6    | 版本DailyBuild  & 开发自验证              |
| Test round 1         | 2021/11/15 | 2021/11/19 | 5    | 版本启动测试                              |
| Beta Version release | 2021/11/22 | 2021/11/24 | 3    | Beta版本发布                              |
| Test round 2         | 2021/11/22 | 2021/11/26 | 5    |                                           |
| Test round 3         | 2021/11/29 | 2021/12/3  | 5    |                                           |
| Test round 4         | 2021/12/6  | 2021/12/10 | 5    |                                           |
| Test round 5         | 2021/12/15 | 2021/12/17 | 3    |                                           |
| Release              | 2021/12/30 | 2021/12/30 | 1    |                                           |


# Feature list
#### 状态说明：
- Discussion(方案讨论，需求未接受)
- Developing(开发中)
- Testing(测试中)
- Accepted(已验收)

|no|feature|status|sig|owner|
|:----|:---|:---|:--|:----|
|1|openEuler 20.03 LTS SP3 OpenStack Kolla supports openEuler OS |Discussion|sig-openstack|[xiyuanwang](https://gitee.com/xiyuanwang)|
|2|openEuler 20.03 LTS SP3 支持Kiran桌面环境 |Discussion|sig-KIRAN-DESKTOP|[tangjie02](https://gitee.com/tangjie02)|


现启动版本需求收集，欢迎社区开发者们反馈和交流，<br />
<br />
需求反馈基本流程： <br />
1、开发者/sig在本贴的表格中填写要合入SP3的需求/特性，并同时填写需求issue <br />
2、版本在release management例会上评审需求 
