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
| Test round 1         | 2021/11/25 | 2021/11/30 | 5    | 版本启动集成测试                              |
| Beta Version release | 2021/12/2 | 2021/12/4 | 3    | Beta版本发布                              |
| Test round 2         | 2021/12/2 | 2021/12/8 | 5    |                                           |
| Test round 3         | 2021/12/10 | 2021/12/15  | 5    |                                           |
| Test round 4         | 2021/12/17  | 2021/12/23 | 5    |                                           |
| Test round 5         | 2021/12/25 | 2021/12/27 | 3    |                                           |
| Release              | 2021/12/30 | 2021/12/30 | 1    |                                           |


# Feature list
#### 状态说明：
- Discussion(方案讨论，需求未接受)
- Developing(开发中)
- Testing(测试中)
- Accepted(已验收)

|no|feature|status|sig|owner|
|:----|:---|:---|:--|:----|
|1|openEuler 20.03 LTS SP3 OpenStack Kolla supports openEuler OS |Accepted|sig-openstack|[xiyuanwang](https://gitee.com/xiyuanwang)|
|2|openEuler 20.03 LTS SP3 支持Kiran桌面环境 |Accepted|sig-KIRAN-DESKTOP|[tangjie02](https://gitee.com/tangjie02)|
|3|openEuler 20.03 LTS SP3 Supports OpenStack Train |Accepted|sig-openstack|[huangtianhua](https://gitee.com/huangtianhua)|
|4|openEuler 20.03-LTS SP3 新增容器OS支持|Accepted|sig-CloudNative|[liyuanrong](https://gitee.com/li-yuanrong)|
|5|openEuler 20.03-LTS SP3 新增轻量级安全容器支持|Accepted|sig-CloudNative|wujing|
|6|[openEuler 20.03 LTS SP3 eggo支持k8s在X86和ARM64双平面部署](https://e.gitee.com/open_euler/issues/list?issue=I4G9ZJ)|Accepted|sig-CloudNative|[liuhao](https://gitee.com/duguhaotian)|
|7|openEuler 20.03-LTS SP3 新增内存分级扩展|Accepted|Storage|[louhongxiang](https://gitee.com/louhongxiang)|
|8|[openEuler 20.03-LTS SP3 新增定制裁剪工具套件oemaker](https://e.gitee.com/open_euler/issues/list?issue=I4GA13)|Accepted|sig-OS-Builder|zhuchunyi|
|9|openEuler 20.03-LTS SP3 智能调优A-tune扩展增强|Accepted|A-Tune|[hanxinke](https://gitee.com/hanxinke)|
|10|[openEuler 20.03 LTS SP3 内核特性增强](https://e.gitee.com/open_euler/issues/list?issue=I4GAUL) |Accepted|sig-kernel|[gatieme](https://gitee.com/gatieme)|
|11|[openEuler 20.03 LTS SP3 官网上线北向兼容性清单](https://e.gitee.com/open_euler/issues/list?issue=I4GATR) |Accepted|sig-Compatibility-Infra|[lovelijunyi](https://gitee.com/lovelijunyi)|
|12|[openEuler 20.03 LTS SP3 支持intel ice lake](https://e.gitee.com/open_euler/issues/list?issue=I4GASF) |Accepted|sig-kernel|[gatieme](https://gitee.com/gatieme)|
|13|[openEuler 20.03 LTS SP3 支持树莓派](https://gitee.com/openeuler/release-management/issues/I4HRUR)|Accepted|sig-RaspberryPi|[woqidaideshi](https://gitee.com/woqidaideshi)|

现启动版本需求收集，欢迎社区开发者们反馈和交流，<br />
<br />
需求反馈基本流程： <br />
1、开发者/sig在本贴的表格中填写要合入SP3的需求/特性，并同时填写需求issue <br />
2、版本在release management例会上评审需求 