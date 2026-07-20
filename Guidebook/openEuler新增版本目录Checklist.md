# openEuler新增版本目录Checklist

本文档用于指导在release-management仓库中新增openEuler版本目录，避免遗漏版本计划、RPM基线、分支继承关系、分支管理状态和变更记录等必要信息。

## 一、新增版本目录前检查

新增版本目录前，请先确认以下事项：

| 检查项 | 说明 |
| :--- | :--- |
| 版本名称 | 确认版本名称、大小写和后缀拼写，例如 `openEuler-26.09-DevStation` |
| 版本类型 | 确认是创新版本、LTS、LTS-Next、LTS-SP，还是专项版本 |
| 继承来源 | 确认从 `master`、`openEuler-xx.xx-LTS-Next` 或其他版本分支继承 |
| 生命周期 | 确认版本是否需要发布计划、维护周期、冻结策略和EOL说明 |
| 责任人 | 确认release owner、分支 owner、相关SIG和QA联系人 |

## 二、版本目录必备文件

新增版本目录建议至少包含以下内容：

```text
openEuler-xx.xx[-suffix]/
├── baseos/
│   └── pckg-mgmt.yaml
├── delete/
│   └── pckg-mgmt.yaml
├── epol/
│   └── pckg-mgmt.yaml
├── everything-exclude-baseos/
│   └── pckg-mgmt.yaml
├── release-change.yaml
└── release-plan.md 或 release-plan.zh.md / release-plan.en.md
```

### 2.1 RPM基线目录

| 目录 | 说明 |
| :--- | :--- |
| `baseos/` | BaseOS软件包基线 |
| `epol/` | EPOL软件包基线 |
| `everything-exclude-baseos/` | Everything中排除BaseOS后的软件包基线 |
| `delete/` | 当前版本待删除软件包清单 |

每个目录下必须包含 `pckg-mgmt.yaml`。如果基于已有版本复制基线，请同步检查以下字段：

```yaml
source_dir: master
destination_dir: openEuler-xx.xx[-suffix]
```

`destination_dir` 必须与新增版本目录名称一致。

### 2.2 release-change.yaml

新增版本目录必须包含 `release-change.yaml`。初始内容如下：

```yaml
release-change: []
```

该文件用于记录版本分支下软件包变更历史。后续新增、移动、删除软件包时，应保持该文件可追溯。

### 2.3 release-plan

版本计划文件用于记录版本节奏、里程碑、需求/特性清单和反馈流程。

如果只维护单语言版本，使用：

```text
release-plan.md
```

如果维护双语版本，建议使用：

```text
release-plan.zh.md
release-plan.en.md
```

同时建议提供 `release-plan.md` 作为入口文件，链接到中英文版本，兼容历史流程和外部引用。

## 三、全局配置同步

新增版本目录后，需要同步检查以下全局配置文件。

### 3.1 valid_release_branches.yaml

`valid_release_branches.yaml` 用于维护版本分支继承关系。新增版本目录后，应将该版本加入对应继承来源下。

例如从 `master` 继承：

```yaml
branch:
  master:
  - openEuler-xx.xx[-suffix]
```

如果版本从 LTS-Next 继承，应加入对应 LTS-Next 节点。

### 3.2 release-management.yaml

`release-management.yaml` 用于维护分支管理状态和owner信息。新增版本目录后，应补充分支记录：

```yaml
- branch: openEuler-xx.xx[-suffix]
  community:
  - src-openeuler
  frozen: false
  owner_atomgit:
  - owner_id
```

字段说明：

| 字段 | 说明 |
| :--- | :--- |
| `branch` | 版本分支名称，应与目录名一致 |
| `community` | 通常为 `src-openeuler` |
| `frozen` | 分支冻结状态，发布流程中按需调整 |
| `owner` / `owner_atomgit` | 分支维护人账号。迁移到AtomGit后，建议新分支优先使用 `owner_atomgit` |

## 四、提交前自检

提交前建议执行以下检查：

| 检查项 | 检查方式 |
| :--- | :--- |
| 目录名拼写一致 | 搜索版本名，确认无旧拼写、大小写错误 |
| `destination_dir` 一致 | 搜索 `destination_dir:`，确认全部指向新增版本 |
| 分支继承关系存在 | 检查 `valid_release_branches.yaml` |
| 分支管理记录存在 | 检查 `release-management.yaml` |
| 变更记录文件存在 | 检查 `release-change.yaml` |
| 发布计划存在 | 检查 `release-plan.md` 或双语release plan |
| 空目录问题 | Git不跟踪空目录，目录下必须有实际文件 |

常用检查命令示例：

```bash
rg "openEuler-xx.xx"
rg "destination_dir:" openEuler-xx.xx
git status --short
git diff --stat
```

## 五、推荐MR拆分

为降低评审风险，新增版本目录建议按问题拆分MR：

| MR | 内容 |
| :--- | :--- |
| MR 1 | 新增版本目录和release plan |
| MR 2 | 新增RPM基线目录和 `pckg-mgmt.yaml` |
| MR 3 | 新增 `release-change.yaml` |
| MR 4 | 更新 `valid_release_branches.yaml` |
| MR 5 | 更新 `release-management.yaml` |
| MR 6 | 修正版本命名、双语入口或其他兼容性问题 |

每个MR应只解决一个明确问题，避免将版本计划、RPM基线、分支继承、owner配置和命名修正混在同一次提交中。

## 六、常见问题

### 6.1 新增了目录但Git没有识别

Git不跟踪空目录。请确认目录下至少存在 `pckg-mgmt.yaml`、`release-change.yaml` 或其他实际文件。

### 6.2 版本目录已存在，但分支继承校验缺失

请检查 `valid_release_branches.yaml` 是否已经登记该版本。如果未登记，后续跨分支软件包变更可能缺少继承依据。

### 6.3 release plan采用双语文件后外部链接找不到

历史流程通常默认查找 `release-plan.md`。如果采用 `release-plan.zh.md` 和 `release-plan.en.md`，建议增加 `release-plan.md` 作为索引入口。

### 6.4 分支冻结状态何时修改

新建版本分支初始通常为：

```yaml
frozen: false
```

进入冻结阶段后，应由release management SIG根据版本计划单独提交MR调整。
