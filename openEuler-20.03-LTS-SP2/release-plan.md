# Release plan
|Stage name|Begin time|End time|
|:----------|:---------|:-------|
|key feature collect|2021-03-16|2021-03-31|
|Develop|2021-03-16|2021-04-26|
|Kernel freezing|2021-04-16|2021-04-16|
|Build|2021-04-26|2021-04-30|
|Test round 1|2021-05-6|2021-05-12|
|Test round 2|2021-05-17|2021-05-21|
|Test round 3|2021-05-24|2021-05-31|
|Test round 4|2021-06-03|2021-06-07|
|Test round 5|2021-06-09|2021-06-11|
|release|2021-06-28|2021-06-30|

# Feture list
#### 状态说明：
- Discussion(方案讨论，需求未接受)
- Developing(开发中)
- Testing(测试中)
- Accepted(已验收)

|no|fetur|status|sig|owner|
|:----|:---|:---|:--|:----|
|1|[【openEuler 20.03 LTS SP2】【虚拟化】回合openEuler 21.03，vmtop支持x86](https://gitee.com/openeuler/release-management/issues/I3NLWF?from=project-issue)|Accepted|virt|@alexchen|
|2|[openEuler 20.03-LTS-SP2支持内存分级扩展特性](https://gitee.com/openeuler/release-management/issues/I2C2NI?from=project-issue)|Accepted|storage|[liuzhiqiang26](https://gitee.com/liuzhiqiang26)|
|3|[openEuler 20.03-LTS-SP2版本集成secgear组件](https://gitee.com/openeuler/release-management/issues/I3JE3U?from=project-issue)|Accepted|sig-confidential-computing|[chenmaodong](https://gitee.com/chenmaodong)|
|4|openEuler 20.03 LTS SP2 supports OpenStack Rocky and Queens|Accepted|sig-openstack|[joec88](https://gitee.com/joec88) [zh-f](https://gitee.com/zh-f) [huangtianhua](https://gitee.com/huangtianhua) [xiyuanwang](https://gitee.com/xiyuanwang) [liksh](https://gitee.com/liksh) [zhangy1317](https://gitee.com/zhangy1317) [sean-lau](https://gitee.com/sean-lau)|
|5|[openEuler 20.03 LTS SP2支持osinfo软件包](https://gitee.com/openeuler/release-management/issues/I3N30H?from=project-issue)|Accepted|packaging|	@solarhu|
|6|[openEuler 20.03 LTS SP2开源openEuler-rpm-config宏定义文件](https://gitee.com/openeuler/release-management/issues/I3N30J?from=project-issue)|Accepted|Base-service|@overweight|
|7|[openEuler 20.03 LTS SP2 支持 compat-openssl10、libzip等](https://gitee.com/openeuler/release-management/issues/I3N30L?from=project-issue)|Accepted|packaging|@solarhu|
|8|[openEuler 20.03 LTS SP2 支持libwbxml、hyperscan](https://gitee.com/openeuler/release-management/issues/I3N30N?from=project-issue)|Accepted|	Desktop|@small_leek|
|9|[openEuler 20.03 LTS SP2支持microcode_ctl](https://gitee.com/openeuler/release-management/issues/I3N30S?from=project-issue)|Accepted|packaging|@solarhu|
|10|[openEuler 20.03 LTS SP2支持bcc软件包](https://gitee.com/openeuler/release-management/issues/I3N30Q?from=project-issue)|Accepted|packaging|@solarhu|
|11|[openEuler 20.03 LTS SP2支持树莓派](https://gitee.com/openeuler/release-management/issues/I3N30P?from=project-issue)|Accepted|RaspberryPi|@jianminw|
|12|[openEuler 20.03 LTS SP2支持1822 HBA卡](https://gitee.com/openeuler/release-management/issues/I3N30V?from=project-issue)|Accepted|kernel|	@xiexiuqi|
|13|[openEuler 20.03 LTS SP2支持飞腾2000+/64](https://gitee.com/openeuler/release-management/issues/I3N30W?from=project-issue)|Accepted|kernel|@xiexiuqi|
|14|[openEuler 20.03 LTS SP2支持maildrop和proftpd](https://gitee.com/openeuler/release-management/issues/I3N30X?from=project-issue)|Accepted|Application|@solarhu|
|15|[openEuler 20.03 LTS SP2支持 iSulad 2.0](https://gitee.com/openeuler/release-management/issues/I3N312?from=project-issue)|Accepted|isulad|@lifeng2221dd1|
|16|[openEuler 20.03 LTS SP2 A-tune 2.0](https://gitee.com/openeuler/release-management/issues/I3N314?from=project-issue)|Accepted|A-Tune|@xiezhipeng1|
|17|[openEuler 20.03 LTS SP2 支持网络安装](https://gitee.com/openeuler/release-management/issues/I3N315?from=project-issue)|Accepted|sig-OS-Builder|@t_feng|
|18|[openEuler 20.03 LTS SP2 支持 criu组件](https://gitee.com/openeuler/release-management/issues/I3N319?from=project-issue)|Accepted|ops|@luanjianhai|
|19|[openEuler 20.03 LTS SP2支持config_acpi_nfit](https://gitee.com/openeuler/release-management/issues/I3N31B?from=project-issue)|Accepted|kernel|@xiexiuqi|
|20|[openEuler 20.03 LTS SP2 虚拟化增强](https://gitee.com/openeuler/release-management/issues/I3N31E?from=project-issue)|Accepted|virt|@KuhnChen|
|21|[openEuler 20.03 LTS SP2 支持 UKUI桌面](https://gitee.com/openeuler/release-management/issues/I3N31F?from=project-issue)|Accepted|sig_UKUI|@dou33|
|22|[openEuler 20.03 LTS SP2 支持DDE桌面](https://gitee.com/openeuler/release-management/issues/I3N31J?from=project-issue)|Accepted|sig-DDE|@panchenbo|
|23|[openEuler 20.03 LTS SP2 编译器支持openjdk](https://gitee.com/openeuler/release-management/issues/I3N31M?from=project-issue)|Accepted|compiler|		@jdkboy|
|24|[openEuler 20.03 LTS SP2支持HA](https://gitee.com/openeuler/release-management/issues/I3N31O?from=project-issue)|Accepted|sig-HA|@yangzhao_kl|
|25|[openEuler 20.03 LTS SP2 加速库版本同步](https://gitee.com/openeuler/release-management/issues/I3N31Q?from=project-issue)|Accepted|kae|	@wuliaokanke|
|26|[openEuler 20.03 LTS SP2支持金融领域软件包](https://gitee.com/openeuler/release-management/issues/I3N311?from=project-issue)|Accepted|packaging|@solarhu|
|27|[openEuler 20.03 LTS SP2支持kmod功能](https://gitee.com/openeuler/release-management/issues/I3N30C?from=project-issue)|Accepted|packaging|@solarhu|
|28|[openEuler 20.03 LTS SP2 CPU核故障在线隔离解决方案](https://gitee.com/openeuler/release-management/issues/I3N36L?from=project-issue)|Accepted|kernel|@xiexiuqi|
|29|[openEuler 20.03 LTS SP2 支持多应用版本构建和发布](https://gitee.com/openeuler/release-management/issues/I3N36K?from=project-issue)|Accepted|Gatekeeper|@solarhu|
|30|[openEuler 20.03 LTS SP2 内存UCE故障降级，用户数据保持一致，业务可持续运行](https://gitee.com/openeuler/release-management/issues/I3N36H?from=project-issue)|Accepted|kernel|@xiexiuqi|
|31|[openEuler 20.03 LTS SP2 故障预测框架](https://gitee.com/openeuler/release-management/issues/I3N36F?from=project-issue)|Accepted|kernel|@xiexiuqi|
|32|[openEuler 20.03 LTS SP2 IO_URING全栈使能](https://gitee.com/openeuler/release-management/issues/I3N36C?from=project-issue)|Testing|kernel|@xiexiuqi|
|33|[openEuler 20.03 LTS SP2 Qemu：虚拟化可靠性和可维护性增强](https://gitee.com/openeuler/release-management/issues/I3N369?from=project-issue)|Accepted|sig-virt|@KuhnChen|
|34|[openEuler 20.03 LTS SP2 Qemu：热迁移pro，提升热迁移性能+安全](https://gitee.com/openeuler/release-management/issues/I3N368?from=project-issue)|Accepted|sig-virt|@KuhnChen|
|35|[openEuler 20.03 LTS SP2支持StratoVirt：下一代轻量化虚拟化平台](https://gitee.com/openeuler/release-management/issues/I3N364?from=project-issue)|Accepted|sig-virt|@KuhnChen|
|36|[【openEuler 20.03 LTS SP2】继承xfce 4.14](https://gitee.com/openeuler/release-management/issues/I3NC3I?from=project-issue)|Accepted|xfce|[@dillon_chen](https://gitee.com/dillon_chen)|
|37|[【openEuler 20.03 LTS SP2】继承Kubernetes 1.18](https://gitee.com/openeuler/release-management/issues/I3NC5H?from=project-issue)|Accepted|sig-cloudnative|[@jingxiaolu](https://gitee.com/jingxiaolu)|
|38|[【openEuler 20.03 LTS SP2】继承门禁检查功能](https://gitee.com/openeuler/release-management/issues/I3O08F?from=project-issue)|Accepted|Gatekeeper|@solarhu|
|39|[openEuler 20.03-LTS-SP2 集成 kubernetes 及其依赖组件](https://gitee.com/openeuler/release-management/issues/I2BHF4?from=project-issue)|Accepted|sig-cloudnative|@jingxiaolu|
|40|[openEuler 20.03-LTS-SP2 arm虚拟机支持NMI watchdog](https://gitee.com/openeuler/release-management/issues/I2B4WL?from=project-issue)|Accepted|virt|@alexchen|
|41|[openEuler 20.03-LTS-SP2 集成 coredns 及其依赖组件](https://gitee.com/openeuler/release-management/issues/I3MXLJ?from=project-issue)|Accepted|sig-cloudnative|@jingxiaolu|
|42|[【openEuler 20.03 LTS SP2】虚拟机热迁移支持TLS](https://gitee.com/openeuler/release-management/issues/I3IE57?from=project-issue)|Accepted|virt|@alexchen|
|43|[【kernel-4.19】openEuler kernel nvme 驱动增强](https://gitee.com/openeuler/release-management/issues/I1WGZE?from=project-issue)|Accepted|kernel|@xiexiuqi|
|44|[openEuler 20.03-LTS-SP2 集成 etcd 及其依赖组件](https://gitee.com/openeuler/release-management/issues/I3MXGJ?from=project-issue)|Accepted|sig-cloudnative|@jingxiaolu|
