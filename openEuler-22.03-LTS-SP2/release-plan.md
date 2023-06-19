# Release plan
|Stage name|Begin time|End time|Days|Note|
|:----------|:---------|:-------|:---------|:-------|
|key feature collect|2023-03-24|2023-04-15|22|版本需求收集|
|Develop|2023-03-24|2023-05-09|46|特性完成开发，合入22.03 LTS-Next|
|Kernel freezing|2023-05-03|2023-05-09|6|内核冻结|
|变更检查&Build|2023-05-10|2023-05-16|6|22.03-LTS Next分支发起软件包淘汰评审&22.03-LTS SP2版本DailyBuild|
|Test round 1|2023-05-17|2023-05-23|7|开发自验证|
|Test round 2|2023-05-24|2023-06-02|7|22.03-LTS SP2 Beta版本发布|
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

|no|feture|status|sig|owner|
|:----|:---|:---|:--|:----|
|[I6UA7F](https://gitee.com/openeuler/release-management/issues/I6UA7F)|DDE组件更新|Testing|sig-DDE|[@HelloWorld_lvcongqing](https://gitee.com/HelloWorld_lvcongqing/)|
| [I6T8OP](https://gitee.com/openeuler/release-management/issues/I6T8OP) | 支持Lustre client软件包 | Testing | sig-SDS | [@xin3liang](https://gitee.com/xin3liang) |
|[I6V5AX](https://gitee.com/openeuler/release-management/issues/I6V5AX)|支持树莓派|Testing|sig-RaspberryPi|[@woqidaideshi](https://gitee.com/woqidaideshi/)|
|[I6VFA7](https://gitee.com/openeuler/release-management/issues/I6VFA7)|openEuler docker容器支持sysMaster管理sshd服务|Testing|dev-utils|[@overweight](https://gitee.com/overweight/)|
|[I6Y54B](https://gitee.com/openeuler/release-management/issues/I6Y54B)|支持ROS2-humble基础版|Testing|sig-ROS|[@anchuanxu](https://gitee.com/anchuanxu/)|
|[I6TEAB](https://gitee.com/openeuler/release-management/issues/I6TEAB)|支持OpenStack Train、Wallaby多版本|Testing|sig-openstack|[@xiyuanwang](https://gitee.com/xiyuanwang/)|
|[I6YL1H](https://gitee.com/openeuler/release-management/issues/I6YL1H)|内核支持容器资源可见性功能|Rejected|sig-kernel|[@wenzhiwei11](https://gitee.com/wenzhiwei11/)|
|[I6YL4A](https://gitee.com/openeuler/release-management/issues/I6YL4A)|内核新增UKFEF功能|Rejected|sig-kernel|[@wenzhiwei11](https://gitee.com/wenzhiwei11/)|
|[I6YLKL](https://gitee.com/openeuler/release-management/issues/I6YLKL)|内核支持Group identity功能|Rejected|sig-kernel|[@wenzhiwei11](https://gitee.com/wenzhiwei11/)|
|[I6WSXH](https://gitee.com/openeuler/release-management/issues/I6WSXH)|新增kunpengsecl软件包支持平台和TEE远程证明|Testing|sig-security-facility|[@gwei3](https://gitee.com/gwei3/)|
|[I71EFN](https://gitee.com/openeuler/release-management/issues/I71EFN)|secGear特性增强|Testing|sig-confidential-computing|[@houmingyong](https://gitee.com/houmingyong/)|
|[I71DTI](https://gitee.com/openeuler/release-management/issues/I71DTI)|支持embedded版本|Testing|sig-embedded||
|[I71TYY](https://gitee.com/openeuler/release-management/issues/I71TYY)|新增通用编译环境制作能力|Testing|sig-OS-Builder|[@chen-huihan](https://gitee.com/chen-huihan/)|
|[I71TEN](https://gitee.com/openeuler/release-management/issues/I71TEN)|支持qcow2格式镜像制作|Testing|sig-Gatekeeper|[@chen-huihan](https://gitee.com/chen-huihan/)|
|[I71TS7](https://gitee.com/openeuler/release-management/issues/I71TS7)|oemaker特性增强|Testing|sig-OS-Builder|[@zhuchunyi](https://gitee.com/zhuchunyi/)|
|[I71V5A](https://gitee.com/openeuler/release-management/issues/I71V5A)|回合bwm特性，支持面向容器的网络带宽调度策略|Testing|sig-high-performance-network|[@kwb0523](https://gitee.com/kwb0523/)|
|[I72C4A](https://gitee.com/openeuler/release-management/issues/I72C4A)|开发流水线打通构建/compass-ci/测试radiaTest 3大服务|Developing|sig-QA|[@disnight](https://gitee.com/disnight/)|
|[I729JF](https://gitee.com/openeuler/release-management/issues/I729JF)|发布kiran-desktop 2.5版本|Testing|sig-KIRAN-DESKTOP|[@tangjie02](https://gitee.com/tangjie02/)|
|[I727Q4](https://gitee.com/openeuler/release-management/issues/I727Q4)|iSulad支持K8S 1.24 /1.25版本|Testing|iSulad||
|[I727OZ](https://gitee.com/openeuler/release-management/issues/I727OZ)|CICD支持：实现热补丁流水线发布，用户可以通过补丁服务制作补丁|Testing|sig-ops|[@solarhu](https://gitee.com/solarhu/)|
|[I727OP](https://gitee.com/openeuler/release-management/issues/I727OP)|热补丁服务：热补丁流水线/管理框架，支持热补丁发布|Testing|sig-ops|[@solarhu](https://gitee.com/solarhu/)|
|[I727NW](https://gitee.com/openeuler/release-management/issues/I727NW)|Rubik混部支持精细化资源QoS感知和控制|Testing|sig-CloudNative|[@jing-rui](https://gitee.com/jing-rui/)|
|[I727H4](https://gitee.com/openeuler/release-management/issues/I727H4)|支持 sysmonitor 特性|Testing|sig-ops|[@cp3yeye](https://gitee.com/cp3yeye/)|
|[I727E2](https://gitee.com/openeuler/release-management/issues/I727E2)|Gazelle新增支持UDP协议|Testing|sig-high-performance-network|[@kircher](https://gitee.com/kircher/)|
|[I727A5](https://gitee.com/openeuler/release-management/issues/I727A5)|安全配置规范框架设计及核心内容构建|Testing|sig-ops|[@yunjia_w](https://gitee.com/yunjia_w/)|
|[I6YYUC](https://gitee.com/openeuler/release-management/issues/I6YYUC)|gala-gopher新增性能火焰图、线程级性能Profiling特性|Rejected|sig-ops|[@Vchanger](https://gitee.com/Vchanger/)|
|[I6YBPV](https://gitee.com/openeuler/release-management/issues/I6YBPV)|5.10内核hisi_sec2 hisi_hpre hisi_zip模块支持nosva特性|Testing|Kernel|[@realzhongkeyi](https://gitee.com/realzhongkeyi/)|
|[I6UAMM](https://gitee.com/openeuler/release-management/issues/I6UAMM)|新增NestOS K8S部署方案|Testing|SIG-K8s-Distro|[@duyiwei7w](https://gitee.com/duyiwei7w/)|
|[I6PXNE](https://gitee.com/openeuler/release-management/issues/I6PXNE)|Kernel新增星云智联板卡N1045XS网卡驱动|Testing|Kernel|[@nebula_matrix](https://gitee.com/nebula_matrix/)|
