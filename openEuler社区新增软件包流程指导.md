## 一、创建新软件仓库

新创建软件仓库分为两种：新创建**原创软件** upstream开源仓库，新创建**开源软件**制品源码仓库。

### **原创软件计划开源**，选择openEuler作为upstream托管仓库，对应的PR创建流程如下：
- a) 提交申请建仓PR，TC 及对应sig组review approve后既可自动创建gitee软件仓（CI脚本自动触发），同步在OBS下的factor编译工程中创建预验证仓（CI脚本自动触发）；
- PR示例：https://gitee.com/openeuler/community/pulls/1226/files

### **开源软件引入openEuler社区**，作为openEuler社区版本rebuild构建使用，对应的PR创建流程样例如下：
- a) 提交申请建仓PR，TC 及对应sig组review approve后既可自动创建gitee软件仓（CI脚本自动触发），同步在OBS下的factor编译工程中创建预验证仓（CI脚本自动触发）；
- PR示例：https://gitee.com/openeuler/community/pulls/975/files

## 二、代码上传到gitee社区

**建仓**完成后，根据[openEuler社区打包规范](https://gitee.com/openeuler/community/blob/master/zh/contributors/packaging.md),完成软件包spec撰写/适配，之后新建PR提交代码+spec等完整的包文件，通过门禁检查和单包编译检查
- PR示例：https://gitee.com/src-openeuler/isula-build/pulls/1 

## 三、代码编译构建二进制RPM包（OBS构建工程）

在第二步骤中新包在OBS的factor工程下编译成功且稳定后，就可以申请移仓到OBS mainline编译工程中来了，申请PR样例如下（openEuler社区是共主干开发，mainline是不受限新增包，编译成功稳定就可以申请加入mainline工程）


- PR示例：https://gitee.com/src-openeuler/obs_meta/pulls/388/files


## 四、纳入社区每日构建版本ISO中参与版本构建（jenkins构建工程）

申请该包被纳入各个版本开发主干的每日构建ISO交付件构建列表中；openEuler社区每日构建版本ISO文件根据包规模大小有两类：基础ISO（大约2300+ 二进制RPM包规模），全量ISO（everything ISO,大约10000+ 二进制RPM包）；

- 【PR样例】https://gitee.com/src-openeuler/mkeuleros/pulls/91
 

## 五、纳入relase发布版本ISO中正式对外发布
申请该包被纳入各个版本正式release发布的ISO交付件构建列表中，需要在版本分支拉出来之前的需求收集阶段，提需求给release sig，根据openEuler社区质量要求、版本需求接纳原则来评审；

ISO文件根据包规模大小有两类：基础ISO（大约2300+ 二进制RPM包规模），全量ISO（everything ISO,大约10000+ 二进制RPM包）。

- PR示例：https://gitee.com/openeuler/release-management/issues/I1O7RM?from=project-issue

 

## 六、需求纳入relase版本后，提交PR申请该包纳入release 分支对应的OBS和jenkins编译构建交付件列表

【OBS编译工程PR申请样例】

- PR样例：https://gitee.com/src-openeuler/obs_meta/pulls/135/files

【jenkins构建工程PR申请样例】
- PR样例： https://gitee.com/src-openeuler/mkeuleros/pulls/91

## 七、新增软件包流程图
![输入图片说明](https://images.gitee.com/uploads/images/2020/1117/190932_99e94b47_5603730.png "new_package.PNG")