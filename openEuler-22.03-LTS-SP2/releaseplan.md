# Release plan
|Stage name|Begin time|End time|Days|Note|
|:----------|:---------|:-------|:---------|:-------|
|key feature collect|2023-03-24|2023-04-15|22|版本需求收集|
|Develop|2023-03-24|2023-05-09|46|特性完成开发，合入22.03 LTS-Next|
|Kernel freezing|2023-05-03|2023-05-09|6|内核冻结|
|变更检查&Build|2023-05-10|2023-05-16|6|22.03-LTS Next分支发起软件包淘汰评审&22.03-LTS SP2版本DailyBuild|
|Alpha|2023-05-17|2023-05-23|7|开发自验证|
|Beta|2023-05-24|2023-06-02|7|22.03-LTS SP2 Beta版本发布|
|Test round 3|2023-06-03|2023-06-09|7|全量SIT验证|
|Test round 4|2023-06-10|2023-06-16|7|全量SIT验证，版本分支代码冻结：管控合入，原则上只允许bug fix|
|Test round 5|2023-06-17|2023-06-23|7|回归测试|
|Test round 6|2023-06-24|2023-06-30|7|回归测试|
|release|2023-06-30|2023-06-30|1|社区Release版本发布评审|

# Feture list
#### 状态说明：
- Discussion(方案讨论，需求未接受)
- Developing(开发中)
- Testing(测试中)
- Accepted(已验收)

|no|fetur|status|sig|owner|
|:----|:---|:---|:--|:----|
|[I6UA7F](https://gitee.com/openeuler/release-management/issues/I6UA7F)|DDE组件更新|Discussion|sig-DDE|[@HelloWorld_lvcongqing](https://gitee.com/HelloWorld_lvcongqing/)|
| [I6T8OP](https://gitee.com/openeuler/release-management/issues/I6T8OP) | 支持Lustre client软件包 | Discussion | sig-SDS | [@xin3liang](https://gitee.com/xin3liang) |
|[I6V5AX](https://gitee.com/openeuler/release-management/issues/I6V5AX)|支持树莓派|Discussion|sig-RaspberryPi|[@woqidaideshi](https://gitee.com/woqidaideshi/)|
|[I6VFA7](https://gitee.com/openeuler/release-management/issues/I6VFA7)|sysMaster软件商用|Discussion|dev-utils|[@overweight](https://gitee.com/overweight/)|
|[I6Y54B](https://gitee.com/openeuler/release-management/issues/I6Y54B)|支持ROS2-humble基础版|Discussion|sig-ROS|[@anchuanxu](https://gitee.com/anchuanxu/)|
