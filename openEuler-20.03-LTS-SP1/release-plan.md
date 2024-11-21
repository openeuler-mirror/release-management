# Release plan
|Stange name|Begin time|End time|
|:----------|:---------|:-------|
|Develop|2020-10-12|2020-11-7|
|Compatibility|2020-11-8|2020-11-18|
|Build|2020-11-19|2020-11-21|
|Test round 1|2020-11-23|2020-11-28|
|Test round 2|2020-11-30|2020-12-5|
|Test round 3|2020-12-7|2020-12-12|
|Test round 4|2020-12-15|2020-12-17|
|Test round 5|2020-12-18|2020-12-22|
|release|2020-12-21|2020-12-22|

# Feture list
## 状态说明：discussion(方案讨论，需求未接受)，developing(开发中)，Testing(测试中)，Accepted(已验收)
|no|feature|status|sig|owner|
|:----|:---|:---|:--|:----|
|1|[openEuler 20.03 LTS SP1支持高可用pacemaker](https://gitee.com/openeuler/release-management/issues/I23GH2?from=project-issue)|Accepted|sig-HA|yangzhao_kl|
|2|[openEuler 20.03 LTS SP1支持openGauss版本](https://gitee.com/openeuler/release-management/issues/I23GGW?from=project-issue)|Accepted| | |
|3|[openEuler 20.03 LTS SP1支持1822 HBA卡驱动](https://gitee.com/openeuler/release-management/issues/I23GGR?from=project-issue)|Accepted| | |
|4|[openEuler 20.03 LTS SP1支持华为多路径](https://gitee.com/openeuler/release-management/issues/I23GGO?from=project-issue)|Accepted| | |
|5|[openEuler 20.03 LTS SP1支持openStack](https://gitee.com/openeuler/release-management/issues/I23GGJ?from=project-issue)|Accepted|sig-python-modules |[@small_leek](https://gitee.com/small_leek) [@hht8](https://gitee.com/hht8) |
|6|[openEuler 20.03 LTS SP1支持金融领域软件包](https://gitee.com/openeuler/release-management/issues/I23GG1?from=project-issue)|Accepted|DB |[@small_leek](https://gitee.com/small_leek) [@hht8](https://gitee.com/hht8) |
|7|[openEuler 20.03 LTS SP1支持大数据管理组件Ambari的依赖组件](https://gitee.com/openeuler/release-management/issues/I23GFY?from=project-issue)|Accepted|sig-release-management |[@small_leek](https://gitee.com/small_leek) [@hht8](https://gitee.com/hht8) |
|8|[openEuler 20.03 LTS SP1新增DDE组件](https://gitee.com/openeuler/release-management/issues/I23GFR?from=project-issue)|Accepted|sig-DDE|[@panchenbo](https://gitee.com/panchenbo)|
|9|[openEuler 20.03-LTS版本新增criu组件](https://gitee.com/openeuler/release-management/issues/I23GFP?from=project-issue)|Accepted| | |
|10|[openEuler 20.03 LTS SP1支持libxml，hyperscan](https://gitee.com/openeuler/release-management/issues/I23GFL?from=project-issue)|Accepted|Desktop |[@small_leek](https://gitee.com/small_leek) [@hht8](https://gitee.com/hht8) |
|11|[openEuler 20.03 LTS SP1同时支持openjdk多个版本](https://gitee.com/openeuler/release-management/issues/I23GFC?from=project-issue)|Accepted| | |
|12|[openEuler 20.03 SP1 虚拟化支持内存，cpu热添加](https://gitee.com/openeuler/release-management/issues/I23GF7?from=project-issue)|Accepted| Virt | [@alexchen](https://gitee.com/zhendongchen) |
|13|[openEuler 20.03 SP1 “支持vmtop”](https://gitee.com/openeuler/release-management/issues/I23GF2?from=project-issue)|Accepted| Virt | [@alexchen](https://gitee.com/zhendongchen) |
|14|[openEuler 20.03 LTS SP1虚拟化支持安全启动](https://gitee.com/openeuler/release-management/issues/I23GEY?from=project-issue)|Accepted| Virt | [@alexchen](https://gitee.com/zhendongchen) |
|15|[openEuler 20.03 LTS SP1虚拟化支持custom模式](https://gitee.com/openeuler/release-management/issues/I23GEU?from=project-issue)|Accepted| Virt | [@alexchen](https://gitee.com/zhendongchen) |
|16|[openEuler 20.03 LTS SP1回合20.09 Atune](https://gitee.com/openeuler/release-management/issues/I23GEM?from=project-issue)|Accepted| | |
|17|[openEuler 20.03 LTS SP1补充SONY使用的依赖包](https://gitee.com/openeuler/release-management/issues/I23GEG?from=project-issue)|Accepted| | |
|18|[openEuler 20.03 LTS SP1补齐pts安装依赖](https://gitee.com/openeuler/release-management/issues/I23GEC?from=project-issue)|Accepted| | |
|19|[openEuler 20.03 LTS SP1回合20.09 iSular新版本特性](https://gitee.com/openeuler/release-management/issues/I23GE8?from=project-issue)|Accepted| | |
|20|[openEuler 20.03 LTS SP1开源openEuler-rpm-config宏](https://gitee.com/openeuler/release-management/issues/I23GDZ?from=project-issue)|Accepted|Base-service |[@small_leek](https://gitee.com/small_leek) [@hht8](https://gitee.com/hht8) |
|21|[openEuler 20.03 LTS SP1支持abrt组件](https://gitee.com/openeuler/release-management/issues/I23GDU?from=project-issue)|Accepted|Application |[@small_leek](https://gitee.com/small_leek) [@hht8](https://gitee.com/hht8) |
|22|[openEuler 20.03 LTS SP1支持osinfo](https://gitee.com/openeuler/release-management/issues/I23GDP?from=project-issue)|Accepted|Base-service |[@small_leek](https://gitee.com/small_leek) [@hht8](https://gitee.com/hht8) |
|23|[microcode_ctl需要回合支持x86](https://gitee.com/openeuler/release-management/issues/I1RFVK?from=project-issue)|Accepted|System-tool |[@small_leek](https://gitee.com/small_leek) |
|24|[openEuler 20.03 LTS SP1新增 raspberrypi 版本](https://gitee.com/openeuler/release-management/issues/I1RMC1?from=project-issue)|Accepted|RaspberryPi|[@woqidaideshi](https://gitee.com/woqidaideshi)|
|25|[openEuler 20.03 LTS SP1新增UKUI组件](https://gitee.com/openeuler/release-management/issues/I1R54N?from=project-issue)|Accepted|sig_UKUI|[@dou33](https://gitee.com/dou33)|
|26|[openEuler 20.03 LTS SP1新增netinstall组件](https://gitee.com/openeuler/release-management/issues/I1Y26A?from=project-issue)|Accepted|sig-OS-Builder|[@t_feng](https://gitee.com/t_feng)|
|27|[openEuler20.03 LTS SP1版本支持飞腾 arm64架构CPU](https://gitee.com/openeuler/release-management/issues/I1RXGT?from=project-issue)|Accepted|||
|28|[openEuler 20.03-LTS版本升级新增bcc的软件包](https://gitee.com/openeuler/release-management/issues/I1O7RM?from=project-issue)|Accepted|||
|29|[openEuler 20.03 LTS SP1申请新增maildrop和proftpd软件包](https://gitee.com/openeuler/release-management/issues/I1TWXG?from=project-issue)|Accepted|Application|[@small_leek](https://gitee.com/small_leek)|
|30|[openEuler 20.03 LTS SP1内核开启config_acpi_nfit内核选项](https://gitee.com/openeuler/release-management/issues/I26KWQ?from=project-issue)|Accepted|||
