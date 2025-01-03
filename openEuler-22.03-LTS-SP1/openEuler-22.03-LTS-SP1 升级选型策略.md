# openEuler-22.03-LTS-SP1 升级选型策略

## openEuler-22.03-LTS-SP1 选型时间

当前社区已启动22.03-LTS-Next 分支，根据release plan，计划于11/8 完成社区选型升级。

| Stage name    | Begin time | End time  | Days | Note                               |
| ------------- | ---------- | --------- | ---- | ---------------------------------- |
| 变更检查阶段1 | 2022/10/8  | 2022/11/8 | 30   | Review软件包变更（升级/退役/淘汰） |

## openEuler-22.03-LTS-SP1 选型策略：

### 软件包基线范围

| 软件范围         | 基线策略                                                     |
| ---------------- | ------------------------------------------------------------ |
| 标准ISO          | 标准ISO 范围软件内软件包将基线范围保持不变，仅对必要cve及缺陷修复进行修改。 |
| everything、Epol | 非强制保持稳定，可选型升级，需解决联动依赖关系。             |

### 软件兼容性

openEuler 对软件包的兼容性进行分级管理，其中：

- level1: 软件包及软件包 API、ABI 在某个 LTS 版本的生命周期保持不变，跨 LTS 版本不保证。
- level2: 软件包及软件包 API、ABI 在某个 SP 版本的生命周期保持不变，跨 SP 版本不保证。
- level3: 版本升级兼容性不做强制保证。

|              |                                                              |
| ------------ | ------------------------------------------------------------ |
| 一级列表定义 | API和ABI在主版本的生命周期内保持稳定，并且在接下来的一个主版本中也尽量保持稳定。<br />1、主版本从openEuler LTS 20.3开始。<br />2. 如果更改导致与现有二进制文件不兼容，则应考虑补丁或特性回滚来保持兼容性，而不是粗暴的升级。<br />3、或提供该库的新旧两个版本等消减措施，以消除对上层软件的影响。 |
| 一级列表范围 | glibc、gcc（libstdc++, libgcc, libgomp, libatomic）、libxml2、zlib、libvirt、elfutils、pam、krb5 |
| 二级列表定义 | API和ABI在单个主版本的生存期内保持稳定，依赖的应用程序在单个主版本生命周期内原则上无需做重大修改。 |
| 二级列表范围 | Kernel KABI、dbus、openssl、bzip2、curl、xz、systemd、libssh、alsa-lib、libmodulemd、motif、libacl、libattr、nss |
| 三级列表定义 | API和ABI在单个主版本的生存期内不强制保持稳定，存在依赖关系的应用程序保持联动升级。 |
| 三级列表范围 | 一级列表与二级列表范围外                                     |

### openEuler软件包退出原则

#### openEuler对软件包的退出情况：

1. 随着技术演进与发展，软件因技术陈旧或架构落后，不能满足现有的应用场景被其他更优秀的软件所取代。
2. openEuler 已经集成的版本过于老旧，且软件新版本License 或其他法律法规限制导致openEuler 不能升级新版本。
3. 软件来自知名社区或组织，社区或组织通过发布公告、修改软件仓库状态、将仓库放到特定目录下等方式告知停止维护的。
4. 软件来自个人、小型社区或组织，两年内未发布版本（含正式版本与测试版本），无明确版本计划，社区提交了有效的Bug或PR，社区半年以上未响应的。
5. 社区运营状态不明确，通过Issue 或者邮件等方式询问社区是否继续维护，社区半年以上未响应或者答复停止维护的。

#### openEuler对需退出软件包的处理：

如果软件符合以上任何一条退出条件，技术委员会与相应SIG的maintainer将首先分析该软件在当前 openEuler 社区中被依赖、被使用的情况。

1. 如果 openEuler 中存在依赖关系，且短时间内不能解除，我们建议 SIG 在 github(或其他主流代码托管平台，例如gitee，gitlab等) 上新建分支代码仓，并主动进行社区维护动作。
2. 如果开源软件因为License或其他法律限制导致不能升级新版本，并且该软件被大规模使用，对应SIG组愿意继续维护老版本，参考自行维护策略

## 社区生命周期辅助管理工具

openEuler-Advisor：https://gitee.com/openeuler/openEuler-Advisor/

