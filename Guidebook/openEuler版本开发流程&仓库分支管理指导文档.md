# openEuler版本开发流程 & 仓库分支管理指导文档

修订记录

| 日期 | 修订版本 | 修改章节 | 修改描述 |
| ---- | -------- | -------- | -------- |
| 2024/05/13 | 0.0.1 | 初稿全文框架 | 初稿框架 |

## 一、概述

### 1.1 文档目的与适用范围

本文档面向 openEuler 社区的**软件包维护者(committer/maintainer)** 与**版本管理人员**，旨在系统性地介绍 openEuler 社区基于 [atomgit](https://atomgit.com) 平台的仓库分支管理流程。文档聚焦于**仓库、分支、发布管理**与以下两类**配置仓库**的操作：

- `openeuler/community` 仓库 —— 管理软件包仓库的创建、分支定义及SIG组归属
- `openeuler/release-management` 仓库 —— 管理版本分支的工程纳管、软件包分层管控

本文档**不涉及**具体的软件包代码开发（如spec编写、源码编译、本地验证等），相关内容请参阅关联文档：

- [软件包引入流程](./软件包引入流程.md)
- [软件包升级流程](./软件包升级流程.md)
- [SPEC文件编写](./SPEC文件编写.md)


## 二、社区软件分支管理规则

### 2.1 openEuler/src-openEuler组织介绍

openEuler 社区采用**共主干(Master) + 多版本分支**的开发模式。根据组织的不同职能定位，两大组织遵循不同的分支管理规范：

| 组织 | 分支管控策略 | 说明 |
|------|-------------|------|
| **[源码仓openeuler](https://atomgit.com/openeuler)** | **不强管控** | 以源码类项目为主（kernel、iSulad、A-Tune、stratovirt等），辅以配置治理类（community、release-management）和工具/基础设施类仓库（mugen、安全工具等），均通过常规 PR 评审机制管理，不设置版本粒度的分支冻结与锁库约束 |
| **[制品仓src-openeuler](https://atomgit.com/src-openeuler)** | **版本级强管控** | 软件包源码仓库依据版本生命周期，对各分支实施严格的代码合入规则、锁库冻结、ABI 兼容等管控策略 |

### 2.2 制品仓src-openEuler版本分支管理规则介绍

`src-openeuler` 组织下包含四类分支：

| 分支类型 | branch from | 简述 |
|---------|------|------|
| **master** | — | 持续滚动开发主干，接纳所有软件包的新增、升级与变更 |
| **创新版本** |  master | 快速迭代的创新发行版，聚焦自由和开源软件的持续创新 |
| **LTS-Next** | master | LTS 版本线的持续开发主干，所有特性开发、bugfix/CVE 修复和版本升级先行合入 |
| **LTS及LTS-SP** | LTS-Next | LTS 为长期支持稳定版本，LTS-SP 为基于 LTS 的迭代更新补丁版本 |
| **其余特殊分支** | - | 特殊分支一事一议审视，**TODO** |

分支总体策略图如下：

![src-openeuler分支规范策略图](../Goverance/Pictures/src-openEuler-branch.png)

> **CASE 1:**
> **原始需求：** 作为一个开发者，我有一个新的软件包引入(src-openeuler组织)想创建24.03-LTS-SP3的分支^①^，该如何创建分支？
> **执行方案：** 需要完整依次序创建 master -> 24.03-LTS-Next -> 24.03-LTS-SP3，3个分支均需要存在，保证后续**软件/特性不丢失^②^**。具体如何创建新分支，可参考[仓库分支创建指导](https://atomgit.com/openeuler/community/blob/master/zh/contributors/create-package.md)。
> 
> **注释：**
> **①** 创建版本分支不代表软件会随版本正式发布，还依赖版本工程配置见[TODO]()
> **②** 基于branch from的关联，社区RM/CICD团队会基于版本发布节奏定期自动拉取创建**创新/LTS&LTS-SP/LTS版本**分支，若分支引入时创建不完整则会被该机制跳过，导致后续版本**软件/特性丢失**。

### 2.3 分支管理配置文件解读

配置文件地址：[openEuler/community/sig](https://atomgit.com/openeuler/community/tree/master/sig)

参考PR：[申请建立golang-1.24制品仓，增加相应committer角色](https://atomgit.com/openeuler/community/pull/7158)

```shell
## 目录结构（以 sig-YOURSIG 为例）
community/
└── sig/
    └── sig-YOURSIG/               # SIG名称
        ├── sig-info.yaml          # SIG组维护者与仓库归属清单
        └── openEuler              # 源码仓软件包配置目录(首字母/包名)
            └── <包名首字母>        # 包名首字母文件夹
                └── pkg-name.yaml  # 软件包分支声明文件
        └── src-openEuler          # 制品仓软件包配置目录(首字母/包名)
            └── <包名首字母>        # 包名首字母文件夹
                └── pkg-name.yaml  # 软件包分支声明文件

## 配置文件实例解读（软件包分支声明 pkg-name.yaml）
name: pkg-name
description: this is an example package for openEuler
upstream: https://github.com/example/example-pkg.git
branches:
- name: master
  type: protected
- name: openEuler-24.03-LTS-Next
  type: protected
  create_from: master
- name: openEuler-24.03-LTS-SP3
  type: protected
  create_from: openEuler-24.03-LTS-Next
type: public

## 配置文件实例解读（SIG组仓库归属 sig-info.yaml）
- repo:                    # 仓库归属声明（配合 pkg-name.yaml 使用）
  - src-openeuler/pkg-name
  committers:              # committer 列表（可选填）
  - gitee_id: committer-id
    name: Committer Name
    organization: Org Name
    email: committer@example.com
```

## 三、社区版本工程管理规则

### 3.1 版本工程分层规则介绍

openEuler 社区在 EulerMaker 构建平台上将软件包按**质量属性、依赖关系、发布范围**划分为四个工程分层：

| 分层 | EulerMaker 工程名示例 | 属性 | 质量要求 | 说明 |
|------|----------------------|------|----------|------|
| **Factory** | `openEuler-master:factory` | 新包预验证 | 编译通过即可 | 所有新建软件包首次编译的默认入口工程，包在此验证编译稳定性后移入其他分层 |
| **EPOL** | `openEuler-master:epol`</br>`openEuler-24.03-LTS-Next:epol`</br>`openEuler-24.03-LTS-SP1:epol` | 附加补充 | 暂无质量要求 | 社区爱好者贡献的附加包，无法独立编译安装，需配合 OS + Everything 使用，社区不承诺 bugfix/CVE 修复 |
| **Everything** | `openEuler-master:everything`</br>`openEuler-24.03-LTS-Next:everything`</br>`openEuler-24.03-LTS-SP1:everything` | 全量正式发布 | 社区全流程质量保证 | 正式发布的全量软件包集合，包依赖关系稳定，可独立编译、构建和安装 |
| **baseos** | （包含于 Everything 工程内，通过奖项构建控制） | 基础OS必选 | 社区全流程质量保证 | Everything 的子集，linux 操作系统必需的核心软件包集合，依赖关系自闭环 |

**分层关系说明：**
- **master分支**：factory是入口层，包编译稳定后按分层引入 epol、everything，由对应目录的`pkcg-mgmt.yaml`配置管理；
- **版本分支(LTS-Next/LTS-SP/创新版本等)**：每个版本分支由 epol、everything组成(参考2.2章节分支依赖关系保持分层一致)，由对应目录的`pkcg-mgmt.yaml`配置管理；baseos 作为 Everything 的子集,由镜像构建工具(oemaker)的`normal_<arch>.xml`进行配置管理；

> **CASE 2:**
> **原始需求：** 作为一个开发者，我有一个新的软件包已经创建完master/LTS-Next/LTS-SP分支，我如何才能随LTS-SP版本正式发布？
> **执行方案^①^：** 
> 1. master开发分支申请加入版本发布范围：在保证开发分支代码通过门禁，完成基本功能验证后，在[release](https://atomgit.com/openeuler/release-management)仓库申请由**factory调整**至epol/everything(提交通过将对应`pckg-mgmt.yaml`软件信息进行迁移即可)
> 2. 版本分支(LTS-Next/LTS-SP)同步申请加入版本发布范围：在完成步骤1，或进行步骤1的同时，在[release](https://atomgit.com/openeuler/release-management)仓库**新增**软件信息至epol/everything(提交通过将对应`pckg-mgmt.yaml`软件信息进行迁移即可)
> 
> **注释：**
> **①** 当前流程描述基于SP版本未发布的场景，若SP版本已发布仍需要新增软件包，需要在完成以上步骤后参考[update版本新增需求流程](todo)
> **②** 基于branch from的关联，社区RM/CICD团队会基于版本发布节奏定期自动拉取创建**创新/LTS&LTS-SP/LTS版本**分支，若分支引入时创建不完整则会被该机制跳过，导致后续版本**软件/特性丢失**。

> 扩展阅读：[openEuler社区软件包质量分级](https://atomgit.com/openeuler/TC/blob/master/oEEP/oEEP-0017%20openEuler%E8%BD%AF%E4%BB%B6%E8%B4%A8%E9%87%8F%E5%88%86%E7%BA%A7&%E6%89%A7%E8%A1%8C%E7%AD%96%E7%95%A5.md)

### 3.2 版本分层管理配置文件解读

配置文件地址：[openEuler/release-management](https://atomgit.com/openeuler/release-management)

参考PR：[add golang-1.24 to openEuler-24.03-LTS-SP3/Next ](https://atomgit.com/openeuler/release-management/pull/2553)

```shell
## 目录结构
release-management/
├── valid_release_branches.yaml   # 分支继承关系定义
├── master/                       # master工程分层配置
│   ├── factory/
│   │   └── pckg-mgmt.yaml        # factory工程软件包清单(仅master涉及)
│   ├── epol/
│   │   └── pckg-mgmt.yaml        # epol分层软件包清单
│   ├── everything/
│   │   └── pckg-mgmt.yaml        # everything分层软件包清单(包含BaseOS)
│   ├── delete/
│   │   └── pckg-mgmt.yaml        # master分支下待删除包接口
│   ├── image-setting/            # 标准交付件
│   │   └── iso                   # ISO镜像配置文件
│   │   │   └── ...
│   │   └── vm                    # 虚机镜像qcow2镜像配置文件
│   │   │   └── ...               
│   │   └── docker                # 容器镜像(dockerfile)配置文件
│   │   │   └── ...
│   │   └── wsl                   # wsl镜像配置文件
│   │   │   └── ...
│   │   └── rasp-img              # 树莓派镜像配置文件
│   │   │   └── ...
│   └── release_change.yaml       # master变更记录
├── openEuler-24.03-LTS-SP3/      # 版本工程分层配置
│   ├── epol/
│   │   └── pckg-mgmt.yaml        # epol分层软件包清单
│   ├── everything/
│   │   └── pckg-mgmt.yaml        # everything分层软件包清单
│   ├── delete/
│   │   └── pckg-mgmt.yaml        # 该分支下待删除包清单
│   ├── image-setting/
│   │   └── ...
│   └── release-change.yaml       # 该分支变更记录
├── openEuler-24.03-LTS-Next/      # （同上结构，各版本分支独立目录）
├── ...                           # 其余版本分支目录
└── multi_version/                # 多版本场景纳管（如 OpenStack 多版本）

## 配置文件实例解读（pckg-mgmt.yaml，以版本分支新增包为例）
- name: pkg-name                 # 软件包名
  source_dir: openEuler-24.03-LTS-SP3    # 来源分支（可选填）
  destination_dir: openEuler-24.03-LTS-SP3 # 目标分支（可选填）
  obs_from: openEuler:Factory    # 包来源工程名（必填）
  obs_to: openEuler:24.03:LTS:SP3:everything  # 包目标工程名（必填）
  date: '2025-06-15'             # 修改日期，须与提交日期一致（必填）

```

## 四、 软件包版本发布操作指导实例

> 详见[软件包引入指导](https://atomgit.com/openeuler/community/blob/master/zh/contributors/create-package.md)

