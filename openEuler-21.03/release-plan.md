# Release plan
|Stange name|Begin time|End time|
|:----------|:---------|:-------|
|Kernel update 5.10|2020-10-20|2020-10-30|
|Key feature collect|2020-10-10|2020-12-15|
|Kernel freezing|2020-12-21|2020-12-30|
|Key feature freezing|2021-1-22|2021-1-22|
|Build beta branch|2021-2-1|2022-2-22|
|Beta test round 1|2021-2-24|2021-3-2|
|Beta test round 2|2021-3-5|2021-3-11|
|Beta test round 3|2021-3-15|2021-3-19|
|Beta test round 4|2021-3-20|2021-3-20|
|release|2021-3-25|2021-3-26|

# Feture list
状态说明：discussion(方案讨论，需求未接受)，Reject(未纳入版本)，developing(开发中)，Testing(测试中)，Accepted(已验收)
|no|fetur|status|sig|owner|
|:----|:---|:---|:--|:----|
|1|[openEuler 21.03 support openStack](https://gitee.com/openeuler/release-management/issues/I25Y6B?from=project-issue)|Testing|sig-openstack|[@joec88](https://gitee.com/joec88) [@liksh](https://gitee.com/liksh) |
|2|[openEuler 21.03 support virtualization live migration pro](https://gitee.com/openeuler/release-management/issues/I25ZB1?from=project-issue)|Testing|sig-virt|[@alexchen](https://gitee.com/zhendongchen)|
|3|[openEuler 21.03 support StratoVirt function enhancement](https://gitee.com/openeuler/release-management/issues/I25ZH0?from=project-issue)|Testing|sig-virt|[@alexchen](https://gitee.com/zhendongchen)|
|4|[openEuler 21.03 support Risc-v virt live migration](https://gitee.com/openeuler/release-management/issues/I25ZF1?from=project-issue)|Testing|sig-virt|[@alexchen](https://gitee.com/zhendongchen)|
|5|[openEuler 21.03 support DDE](https://gitee.com/openeuler/release-management/issues/I27TT4?from=project-issue)|developing|sig-DDE|[@panchenbo](https://gitee.com/panchenbo)|
|6|[openEuler 21.03 kernel update to version 5.10](https://gitee.com/openeuler/release-management/issues/I27YGU?from=project-issue)|Testing|sig-kernel|[@XieXiuQi](https://gitee.com/xiexiuqi)|
|7|[openEuler 21.03 remove python 2 from release](https://gitee.com/openeuler/release-management/issues/I29EV9?from=project-issue)|Testing|sig-python-modules|[@yaqiangchen](https://gitee.com/yaqiangchen)|
|8|[openEuler 21.03 support xfce 4.14](https://gitee.com/openeuler/release-management/issues/I29LTB?from=project-issue)|developing|xfce|[@dillon_chen](https://gitee.com/dillon_chen)|
|9|[openEuler 21.03 support GNOME 3.38.1](https://gitee.com/openeuler/release-management/issues/I29LTT?from=project-issue)|Reject|GNOME|[@dillon_chen](https://gitee.com/dillon_chen)|
|10|[openEuler 21.03 Increase the dependency library of ROS-base](https://gitee.com/openeuler/release-management/issues/I2D19V?from=project-issue)|Reject|sig-ROS|[@anchuanxu](https://gitee.com/anchuanxu)|
|11|[openEuler 21.03 support memig](https://gitee.com/openeuler/release-management/issues/I2C2NY?from=project-issue)|Testing|memig|[@liuzhiqiang26](https://gitee.com/liuzhiqiang26)|
|12|[openEuler 21.03 support replace vender info](https://gitee.com/openeuler/release-management/issues/I2C2JJ?from=project-issue)|Testing|Builder|[@t.feng](https://gitee.com/t.feng)|
|13|[openEuler 21.03 support nvwa](https://gitee.com/openeuler/release-management/issues/I2B057?from=project-issue)|Testing|sig-ops|[@EulerOSWander](https://gitee.com/EulerOSWander)|
|14|[openEuler 21.03 support secGear](https://gitee.com/openeuler/release-management/issues/I2B0KY?from=project-issue)|Testing|sig-confidential-computing|[@chenmaodong](https://gitee.com/chenmaodong)|
|15|[openEuler 21.03 support RaspberryPi](https://gitee.com/openeuler/release-management/issues/I2CVE3)|developing|sig-RaspberryPi|[@woqidaideshi](https://gitee.com/woqidaideshi)|
|16|[openEuler 21.03 support UKUI](https://gitee.com/openeuler/release-management/issues/I2E61C)|developing|sig-UKUI|[@dou33](https://gitee.com/dou33)|
|17|[openEuler 21.03 support HA](https://gitee.com/openeuler/release-management/issues/I2E5R3?from=project-issue)|developing|sig-HA|[@yangzhao_kl](https://gitee.com/yangzhao_kl)|
|18|[openEuler 21.03 support StratoVirt microvm image](https://gitee.com/openeuler/release-management/issues/I2P83D?from=project-issue)|Testing|sig-virt|[@alexchen](https://gitee.com/zhendongchen)|
|19|[openEuler 21.03 support Kubernetes](https://gitee.com/openeuler/release-management/issues/I2CMA0?from=project-issue)|Testing|sig-cloudnative|[@jingxiaolu](https://gitee.com/jingxiaolu)|
|20|[openEuler 21.03 support KubeSphere](https://gitee.com/openeuler/release-management/issues/I34L4L)|Reject|sig-kubesphere|[@feynmanzhou](https://gitee.com/feynmanzhou)|
|21|[openEuler 21.03 update SPDK](https://gitee.com/openeuler/release-management/issues/I35A62)|Testing|Storage|[@liuzhiqiang](https://gitee.com/liuzhiqiang26)|
|22|[openEuler 21.03 update some software](https://gitee.com/openeuler/release-management/issues/I35BTA)|Testing|release-management|[@chenyaqiang](https://gitee.com/yaqiangchen)|
|23|[openEuler 21.03 slim container base image](https://gitee.com/openeuler/release-management/issues/I35D25)|Testing|sig-cloudnative|[@jingxiaolu](https://gitee.com/jingxiaolu)|
