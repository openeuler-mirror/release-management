# 补丁回合相关指导

## 1.  查找补丁
### 1.1  通过其他网站查找补丁
NVD:  https://nvd.nist.gov/vuln/search

![漏洞数据库](./Pictures/patch%E5%9B%9E%E5%90%88/%E6%BC%8F%E6%B4%9E%E6%95%B0%E6%8D%AE%E5%BA%93.png)

### 1.2  通过代码托管仓查找补丁
当软件包编译或者功能出现错误时，可以在代码托管仓查看提交记录，查找问题修复补丁。
以 trafficserver 软件包的编译报错为例，报错日志:
```
traffic_top/traffic_top.cc: In function 'void prettyPrint(int, int, double, int)':
traffic_top/traffic_top.cc:129:18: error: format not a string literal and no format arguments [-Werror=format-security]
  129 |   mvprintw(y, x, buffer);
      |                  ^~~~~~
traffic_top/traffic_top.cc: In function 'void makeTable(int, int, const std::__cxx11::list<std::__cxx11::basic_string<char> >&, Stats&)':
traffic_top/traffic_top.cc:146:41: error: format not a string literal and no format arguments [-Werror=format-security]
  146 |     mvprintw(my_y, x, prettyName.c_str());
      |                                         ^
```
可以看到报错的文件是 **traffic_top/traffic_top.cc**，trafficserver的代码托管仓是`https://github.com/apache/trafficserver`，在代码托管仓提交对traffic_top关键字进行搜索。

![trafficserver-github查找补丁](./Pictures/patch%E5%9B%9E%E5%90%88/trafficserver-github%E6%9F%A5%E6%89%BE%E8%A1%A5%E4%B8%81.png)

从截图可以看到，搜索traffic_top出现的结果有很多，traffic_top在提交标题出现的有三处，我们可以逐个排查；也可以通过发布版本的时间去逐步缩小范围，比如 trafficserver 出现问题的版本是9.1.0，发布时间是2021年8月14号，那我们排查就可以排查2021年8月14号的之后的提交。
最终我们定位到提交记录是`https://github.com/apache/trafficserver/pull/8437`, 
通过提交记录里面的描述和日志贴图，也确定本次提交可以修复我们的问题。

#### 1.2.3  通过官网查找补丁信息
软件包官网一般会有changlog，可以根据changlog里的说明信息，推测可能的修改版本，然后在托管仓查看对应版本里面的修改，逐步排查可能的修复提交。

## 2.  制作补丁
### 2.1  github网页制作补丁
1. github网页找到对应修复问题的commit，例如https://github.com/sergey-dryabzhinsky/python-zstd/commit/428a31edcde94d2908aa8ca3439ca01a797de3a4 ，上述commit链接末尾添加**.patch** : https://github.com/sergey-dryabzhinsky/python-zstd/commit/428a31edcde94d2908aa8ca3439ca01a797de3a4.patch ，网页访问添加.patch的链接，即是一个补丁

![ github网页制作补丁](./Pictures/patch%E5%9B%9E%E5%90%88/github%E7%BD%91%E9%A1%B5%E5%88%B6%E4%BD%9C%E8%A1%A5%E4%B8%81.png)


### 2.2  git命令制作补丁
适配补丁文件的目录 
https://gitee.com/src-openeuler/mysql/pulls/99/files

git命令制作补丁步骤：
1. 获取mysql的源码包，进入源码包目录
2. 初始化git仓： git init
3. 添加当前git仓： git add -A
4. 将初始化的git仓作为一次提交： git commit -m “init”
5. 在源码目录下修改对应补丁文件的内容，修改完成后保存退出
6. 再次添加修改后的git仓： git add -A
7. 再次将修改后的git仓进行提交： git commit -m “Fix YYYY XXXX”
8. 将上次的提交生成patch： git format-patch -n1
9. 修改patch的commit信息，将上游补丁链接地址作为origin添加到commit信息中

### 2.3  diff命令制作补丁
适配补丁文件的目录 
https://gitee.com/src-openeuler/mysql/pulls/99/files

diff命令制作补丁步骤：
1. 获取mysql的源码包，把mysql源码包拷贝两份，名字任意命名
2. 进入两份源码包中的一份，修改对应补丁文件的内容，修改完成后保存退出
3. 执行`diff -Nur 修改前文件  修改后文件  > patch-name.patch`，即可制作一份补丁

### 2.4 补丁引入前检查
1. CVE补丁，补丁以CVE-补丁编号命令
2. 参考上游的补丁，通过Reference标注补丁来源

![输入图片说明](./Pictures/patch%E5%9B%9E%E5%90%88/%E9%80%9A%E8%BF%87Reference%E6%A0%87%E6%B3%A8%E8%A1%A5%E4%B8%81%E6%9D%A5%E6%BA%90.png)

## 3.  回合补丁
### 3.1  验证补丁是否能正常回合
1. 补丁添加到spec文件<br>
(1) 通过Patch字段标记补丁，例如`Patch2:    CVE-2023-25950.patch`<br>
(2) 注意spec %prep阶段是否是自动回合补丁。%prep阶段一般有%autosetup和%setup两种方式<br>

- %autosetup为自动解源码包和打补丁方式，一般使用`-p1`参数忽略一层目录对解压后的源码包进行打补丁，也可以添加`-S git`参数使用git方式进行自动回合补丁，会识别到spec文件中定义的patch进行打补丁
autosetup 打补丁相关截图:

![autosetup](./Pictures/patch%E5%9B%9E%E5%90%88/autosetup.png)

- %setup仅解压源码包，需要打补丁时需要使用`%patch<number> -p1`，将spec中定义的patch进行打补丁

setup 打补丁接相关截图:

![setup](./Pictures/patch%E5%9B%9E%E5%90%88/setup.png)


2. 验证补丁是否可以正常打入到源码
根据上述查找补丁的方式，可确定补丁链接为：https://git.haproxy.org/?p=haproxy-2.7.git;a=commit;h=3ca4223c5e1f18a19dc93b0b09ffdbd295554d46
下载补丁到本地环境：

![输入图片说明](./Pictures/CVE/%E8%A1%A5%E4%B8%81%E9%AA%8C%E8%AF%81-%E6%9C%AC%E5%9C%B0%E9%AA%8C%E8%AF%811.png)

(1) 下载haproxy-2.6.6版本代码： git clone https://gitee.com/src-openeuler/haproxy<br>
(2) 切换到要验证的分支：git checkout -b openEuler-22.03-LTS-SP1<br>
(3) 下载补丁wget https://git.haproxy.org/?p=haproxy-2.7.git;a=commit;h=3ca4223c5e1f18a19dc93b0b09ffdbd295554d46
(4) 执行rpmdev-setuptree命令创建本地rpmbuild目录 <br>
(5) 复制对应分支下的文件到rpmbuild目录下：cp * ~/rpmbuild/SOURCES/，cp haproxy.spec ~/rpmbuild/SPEC/<br>
(6) 切换到rpmbuild目录下：cd ~/rpmbuild/<br>
(7) 将（3）下载的补丁添加到 ~/rpmbuild/SPEC/haproxy.spec文件<br>
(8) 执行命令rpmbuild -bp SPEC/haproxy.spec，查看日志，补丁是否正常回合<br>

![输入图片说明](./Pictures/patch%E5%9B%9E%E5%90%88/rpmbuild-bp.png)

由图知补丁修改的两处位置仅有行差，可正常回合。 

### 3.2  回合补丁前检查
1. 适配的补丁与原补丁文件对比是否有缺失，错改情况
2. 版本跨度较大的补丁，需关注高低版本补丁代码逻辑是否合理且一致，再考虑能否进行适配
3. 本地验证patch是否生效

## 4.  验证补丁是否修复漏洞
通过补丁修复漏洞后，需要验证问题是否被修复。验证步骤分为**复现问题-------> 补丁修复 ------> 继续复现问题查看问题是否复现**。

以 trafficserver 编译失败为例具体说明：
1. 复现问题 <br>
(1) 下载trafficserver版本代码： git clone https://gitee.com/src-openeuler/trafficserver.git <br>
(2) 切换到要验证的分支：git checkout -b openEuler-20.03-LTS-SP1 <br>
(3) 执行rpmdev-setuptree命令创建本地rpmbuild目录 <br>
(4) 复制对应分支下的文件到rpmbuild目录下：cp * ~/rpmbuild/SOURCES/，cp trafficserver.spec   ~/rpmbuild/SPEC/ <br>
(5) 切换到rpmbuild目录下：cd ~/rpmbuild/ <br>
(6) 执行rpmbuild编译命令rpmbuild -ba SPEC/trafficserver.spec  <br>

![trafficserver-编译失败复现](./Pictures/patch%E5%9B%9E%E5%90%88/trafficserver-%E7%BC%96%E8%AF%91%E5%A4%B1%E8%B4%A5%E5%A4%8D%E7%8E%B0.png)

由截图可以看到编译报错。

2. 问题已复现，现在就需要查找补丁，制作补丁以及回合补丁。按照1.2的步骤查找补丁，按照2.1的步骤制作补丁，按照3.1的步骤回合补丁<br>
3. 执行rpmbuild编译命令rpmbuild -ba SPEC/trafficserver.spec 继续编译复现问题 <br>

![trafficserver编译成功截图](./Pictures/patch%E5%9B%9E%E5%90%88/trafficserver%E7%BC%96%E8%AF%91%E6%88%90%E5%8A%9F%E6%88%AA%E5%9B%BE.png)

由截图可以看到，trafficserver已编译成功，证明补丁可以修复出现的问题。

## 5. pr提交
1. 首先，需要将gitee平台的src-openeuler/haproxy 仓库fork到个人仓库

![输入图片说明](./Pictures/CVE/%E6%8F%90%E4%BA%A4pr%E4%BF%AE%E5%A4%8D-1.png)

2. 将远程 fork的haproxy仓库clone到本地环境
git clone https://gitee.com/starlet-dx/haproxy.git

3. 本地环境拉取需要提交pr的分支
git checkout -b openEuler-22.03-LTS-SP1

4. 修改验证后的补丁和spec到haproxy的目录下
git add -A & git commit -m “Fix CVE-2023-25950”

5. 推送到码云的个人仓库对应分支： git push

6. 在个人仓库点击“+pull request”按钮进入创建PR页面。

![输入图片说明](./Pictures/CVE/%E6%8F%90%E4%BA%A4pr%E4%BF%AE%E5%A4%8D-2.png)

7. 提交PR时，标题一般与changelog一致，说明里需要贴上CVE的issue链接、补丁链接，然后点击“创建 pull request”按钮创建PR。

![输入图片说明](./Pictures/CVE/%E6%8F%90%E4%BA%A4pr%E4%BF%AE%E5%A4%8D-3.png)

8. 需关注“提交记录”和“文件改动”状态。若存在多条提交记录，需合并成一条；若文件改动跟实际修改存在差异，本地修改后重新提交到个人仓库，再创建提交pr。

9. Pr提交后，关注门禁构建结果。若出现报错情况，需确认是否提交存在问题，针对报错现象进行修改；若门禁报错属于正常构建结果，需在评论区解释报错原因，方便maintainer检视。

10. 门禁编译通过，出现“ci_successful”标签且无门禁报错后，添加“审查人员”后等待代码合入。

11. 跟踪pr直到出现“已合入”标签，则说明此CVE的修复patch已回合到最新代码仓库，完成修复。

![输入图片说明](./Pictures/CVE/%E6%8F%90%E4%BA%A4pr%E4%BF%AE%E5%A4%8D-4.png)

## 6. 个人checklist
| 涉及阶段  | 检查项   |
|---|---|
| 自验证  |1. CVE的补丁，补丁以CVE-编号命名<br /> 2. 参考上游的补丁，标注补丁来源链接<br /> 3. spec中需关注prep阶段是否为自动回合方式，确保patch打入<br /> 4. 适配的补丁与原补丁文件对比是否有缺失，错改情况，并在补丁commit信息中标注参考链接地址<br /> 5. 版本跨度较大的补丁，需关注高低版本补丁代码逻辑是否合理且一致，再考虑能否进行适配<br /> 6. 本地验证patch是否生效<br />   |

