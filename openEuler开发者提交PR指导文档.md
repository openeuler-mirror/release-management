<u>***openEuler社区工程构建及release-management版本基线管控流程优化上线里程碑：***</u>

<u>***1.master分支纳入release-management管控&分层构建——7/27***</u>

<u>***2.openEuler-22.09基线管控优化——7/27***</u>

<u>***3.multi-version分支、Next开发分支纳入release-management管控——7/30***</u>

<u>***Notes：***</u>

<u>***1.社区基于master分支工程做的分层project，如无特别需求，由CICD sig组主导软件包的分层，开发者如往常提交PR至openEuler:Mainlien***</u>

<u>***/openEuler:Epol即可。若开发者对于具体软件包的分层有新的建议，欢迎提交issue或者邮件交流！***</u>

<u>***2.7/27只上线master分层构建及openEuler-22.09基线管控优化（原有pckg-mgmt.yaml拆分为四个子目录下的pckg-mgmt.yaml），在7/30之前***</u>

<u>***其他版本分支的软件包变更还沿用原有流**程*</u>

## 1 基于master分层构建和2209分支开发者提交PR修改流程

#### 1.1 master下包的移动

<u>***操作实例***：</u>

***<u>修改对应目录下的pckg-mgmt.yaml，从openEuler-Mainline移动metis至openEuler-Qt，将包内容从openEuler-Mainline删除，并添加至openEuler-Qt</u>***

![0723maser_move](Pictures\0723maser_move.png)

***<u>note：记录本次PR的所有移动信息至master/release_change.yaml中（该动作为自动动作，无需开发者操作）</u>***

![0723master_move_record](Pictures\0723master_move_record.png)

#### 1.2 master下包的删除

<u>***操作实例***：</u>

***<u>修改master/delete目录下的pckg-mgmt.yaml，将要删除的包加入到yaml中，无需从原yaml中删除该包信息</u>***

![0723master_delete](Pictures/0723master_delete.png)

***<u>note：记录本次PR所所删除的包至master/release_change.yaml中，从原yaml中删除该包（该动作为自动动作，无需开发者操作）</u>***

![0723master_delete_record](Pictures/0723master_delete_record.png)

#### 1.3 master下包的新增

**note：master下包的新增均有后台任务完成，开发者不能操作**

#### 1.4 开发或者版本分支下包新增（pckg-mgmt.yaml已拆分）

<u>***操作实例***：</u>

***<u>新增python-watchdog至openEuler-2209/epol中，修改openEuler-2209/epol/pckg-mgmt.yaml，如下图</u>***

![0723_2209_add](Pictures/0723_2209_add.png)

***<u>note：记录本次PR的所有 新增包信息至openEuler-2209/release_change.yaml中（该动作为自动动作，无需开发者操作）</u>***

![0723_2209_add_record](Pictures/0723_2209_add_record.png)

#### 1.5 开发或者版本分支内包的移动（pckg-mgmt.yaml已拆分）

<u>***操作实例***：</u>

***<u>移动openEuler-2209/epol下的包openapi-schema-validator至openEuler-2209/baseos，如下图修改对应yaml</u>***

![internal_move_2209](Pictures/internal_move_2209.png)

***<u>note：记录本次PR的所有 新增包信息至openEuler-2209/release_change.yaml中（该动作为自动动作，无需开发者操作）</u>***

#### 1.6 开发或者版本分支内包的删除（pckg-mgmt.yaml已拆分）

<u>***操作实例***：</u>

***<u>删除openEuler-2209/everything-exclude-baseos下的python-pythonwebhdfs，将包名写入openEuler-2209/delete/pckg-mgmt.yaml,无需从原yaml中删除该包信息，如下图</u>***

![2209_delete](Pictures/2209_delete.png)

***<u>note：记录本次PR的所有 删除包信息至openEuler-2209/release_change.yaml中，并从原yaml中删除该包信息（该动作为自动动作，无需开发者操作）</u>***

![2209_delete_record](Pictures/2209_delete_record.png)

#### 1.7 一个PR同时提交包移动到两个分支

**Note：要在同一个PR完成不同分支的包引入或移动，分支需满足以下继承规则，停维分支暂不支持**

https://gitee.com/openeuler/release-management/blob/master/valid_release_branches.yaml

***<u>修改对应pckg-mgmt.yaml，如下图</u>***

![eagle_add](Pictures/eagle_add.png)

开发者想同时将包eagle 1.从openEuler:Factory移动至工程openEuler:Lua 2.同时从openEuler:Lua引入至openEuler-22.09，由于分支openEuler-22.09和master满足分支继承规则，因此可以用一个PR同时移动

***<u>Note：对于所有包的移动都会记录到对应得release_change.yaml中</u>***

![eagle](Pictures/eagle.png)