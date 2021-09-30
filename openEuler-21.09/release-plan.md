# Release plan
|Stage name|Begin time|End time|
|:----------|:---------|:-------|
|Collect key features |2021-05-18|2021-06-04|
|Develop|2021-06-04|2021-08-13|
|Kernel freezing|2021-07-19|2021-07-23|
|Build|2021-08-09|2021-08-15|
|Performance test round 1|2021-08-16|2021-08-27|
|Test round 2|2021-08-30|2021-09-03|
|Test round 3|2021-09-06|2021-09-10|
|Test round 4|2021-09-13|2021-09-18|
|Test round 5|2021-09-22|2021-09-26|
|Release|2021-09-30|2021-09-30|

# Feature list
## 状态说明：

- Discussion(方案讨论，需求未接受)
- Developing(开发中)
- Testing(测试中)
- Accepted(已验收)

|No|Feature|Status|SIG|Owner|
|:----|:---|:---|:--|:----|
| [#I3U85C](https://gitee.com/openeuler/release-management/issues/I3U85C) | 【openEuler 21.09】GCC升级到10.3.0版本 | Accepted| Compiler | [@Haijian.Zhang](https://gitee.com/open_euler/dashboard/members/haijianzhang) ,[@eastb233](https://gitee.com/open_euler/dashboard/members/eastb233) |
| [#I3VFAU](https://gitee.com/openeuler/release-management/issues/I3VFAU) | 【openEuler 21.09】openEuler 21.09 支持 KubeSphere 3.1.0 | Accepted| SIG-KubeSphere | [@Feynman](https://gitee.com/feynmanzhou) ,[@Calvin](https://gitee.com/calvinyu), [@Joey](https://gitee.com/imjoey) |
| [#I3ZN4J](https://gitee.com/openeuler/release-management/issues/I3ZN4J) | 【openEuler 21.09】openEuler 21.09 支持 OpenStack Wallaby | Accepted| SIG-OpenStack | [@joec88](https://gitee.com/joec88) [@huangtianhua](https://gitee.com/huangtianhua) [@xiyuanwang](@https://gitee.com/xiyuanwang)  [@zh-f](https://gitee.com/zh-f)  [@liksh](https://gitee.com/liksh) [@zhangy1317](https://gitee.com/zhangy1317) |
| [#I41F6S](https://gitee.com/openeuler/release-management/issues/I41F6S) | [openEuler 21.09]交付secPaver| Accepted| SIG-Security_facility | [@HuaxinLuGitee](https://gitee.com/HuaxinLuGitee) |
| [#I41F61](https://gitee.com/openeuler/release-management/issues/I41F61) | [openEuler 21.09]eggo：一键式、轻量化、可配置集群部署 | Accepted| SIG-CloudNative | [@jingwoo](https://gitee.com/jingwoo) |
| [#I41F5Z](https://gitee.com/openeuler/release-management/issues/I41F5Z) | [openEuler 21.09]kubOS：运行内存消耗<150M,重启时间<15s；| Accepted| SIG-CloudNative | [@radeon92](https://gitee.com/radeon92) |
| [#I41F5A](https://gitee.com/openeuler/release-management/issues/I41F5A) | [openEuler 21.09]内存分级扩展框架增强，新增用户态swap及策略框架，性能降低<15%| Accepted| SIG-Storage  | [@whoisxxx](https://gitee.com/whoisxxx) |
| [#I427HO](https://gitee.com/openeuler/release-management/issues/I427HO) | [openEuler 21.09] openEuler 21.09 支持 OpenResty 1.19.3.1 | Accepted| SIG-OpenResty | [@Joey](https://gitee.com/imjoey) [@fukiki](https://gitee.com/fukiki) [@fuchangjie](https://gitee.com/fu_changjie) [@Jacean](https://gitee.com/Jacean) |
| [#I44CJS](https://gitee.com/openeuler/release-management/issues/I44CJS) | 【openEuler 21.09】openEuler 21.09 支持 架构感知、配置溯源服务 | Accepted| SIG-ops | [@luanjianhai](https://gitee.com/luanjianhai)   [@solarhu](https://gitee.com/solarhu)  [@Gongc](https://gitee.com/Gongchen)  [@yaqiangchen](https://gitee.com/yaqiangchen)   [@cmss_dx](https://gitee.com/cmss_dx) [@MrRlu](https://gitee.com/MrRlu) |
| [#I3VBFP](https://gitee.com/open_euler/dashboard?issue_id=I3VBFP) | 【openEuler 21.09】openEuler 21.09 支持树莓派| Accepted|RaspberryPi|@jianminw|
| [#I3VCTS](https://gitee.com/open_euler/dashboard?issue_id=I3VCTS) | 【openEuler 21.09】openEuler 21.09 支持UKUI| Accepted|sig_UKUI|@dou33|
| [#I3VD4H](https://gitee.com/open_euler/dashboard?issue_id=I3VD4H) | 【openEuler 21.09】openEuler 21.09 支持HA| Accepted|sig-HA|@yangzhao_kl|
| [#I3VE7L](https://gitee.com/open_euler/dashboard?issue_id=I3VE7L) | 【openEuler 21.09】openEuler DDE版本升级| Accepted|sig-DDE|@panchenbo|
| [#I3VE7A](https://gitee.com/open_euler/dashboard?issue_id=I3VE7A) | 【openEuler 21.09】openEuler 21.09 DDE支持画板，音乐和影院应用| Accepted|sig-DDE|@panchenbo|
| [#I41F6X](https://gitee.com/open_euler/dashboard?issue_id=I41F6X) | 【openEuler 21.09】Stratovirt 2.0支持最小集|Accepted|sig-virt|@cellfaint|
| [#I3VCZG](https://gitee.com/open_euler/dashboard?issue_id=I3VCZG) | 【openEuler 21.09】openEuler 21.09 支持XFCE|Accepted|xfce|@dillon_chen|
| [#I41AUQ](https://gitee.com/open_euler/dashboard?issue_id=I41AUQ) | 【openEuler 21.09】支持飞腾FT2500双路服务器|Accepted|kernel|@xiexiuqi|
| [#I40QDN](https://gitee.com/open_euler/dashboard?issue_id=I40QDN) | 【openEuler-21.09】支持兆芯处理器平台 |Accepted|kernel|@xiexiuqi|
| [#I3Z80Y](https://gitee.com/open_euler/dashboard?issue_id=I3Z80Y) | 【openEuler-21.09】arm64: Add config switch and kernel parameter for CPU0 hotplug |Accepted|kernel|@xiexiuqi|
| [#I3ZFV2](https://gitee.com/open_euler/dashboard?issue_id=I3ZFV2) | 【openEuler-21.09】 add options to tuning the prefetch prolicy for HIP08|Accepted|kernel|@xiexiuqi|
| [#I3ZX4D](https://gitee.com/open_euler/dashboard?issue_id=I3ZX4D) | 【openEuler-21.09】introduce qos scheduler for co-location|Accepted|kernel|@xiexiuqi|
| [#I3ZXKY](https://gitee.com/open_euler/dashboard?issue_id=I3ZXKY) | 【openEuler-21.09】memcg: enable memcg oom-kill for __GFP_NOFAIL|Accepted|kernel|@xiexiuqi|
| [#I3ZN72](https://gitee.com/open_euler/dashboard?issue_id=I3ZN72) | [openEuler-21.09] stnp 加速 clear_page|Accepted|kernel|@xiexiuqi|
| [#I48FQT](https://gitee.com/open_euler/dashboard?issue_id=I48FQT) | [openEuler-21.09] 21.09继承secGear、虚拟化、容器等特性|Accepted|||
| [#I4CHBP](https://gitee.com/openeuler/release-management/issues/I4CHBP) | 【openEuler-21.09】openEuler支持嵌入式镜像|Accepted|sig-embedded||
| [#I4CHRO](https://gitee.com/openeuler/release-management/issues/I4CHRO) | 【openEuler-21.09】openEuler支持边缘协同框架（kubeedge）|Accepted|sig-edge||
