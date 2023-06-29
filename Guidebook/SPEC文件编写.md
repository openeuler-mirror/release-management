# SPEC文件编写

## 一、SPEC文件的说明

## 1、SPEC文件说明

### 1.1 简要描述

```
.spec 文件，该文件包含软件打包的全部信息，修改完这个文件后执行 rpmbuild 命令，经过这一步，系统会按照步骤生成最终的 RPM 包。
```

### 1.2 SPEC涉及到的rpm一些基础介绍

```
[root@localhost ~]# tree rpmbuild
rpmbuild
├── BUILD
├── BUILDROOT
├── RPMS
├── SOURCES
├── SPECS
└── SRPMS

```
目录说明

| 目录      | 名称     | 功能                                                  |
| ---------- | -------------- | ------------------------------------------------------------ |
| ~/rpmbuild/BUILD      | 构建目录    | 源码被解压到此处并在该目录中的子目录完成编译 |
| ~/rpmbuild/RPMS    | RPM包目录    | 生成保存二进制RPM包 |
| ~/rpmbuild/SOURCES      | 源代码目录    | 保存源码包（.tar.gz）以及补丁和spec中源文件的目录 |
| ~/rpmbuild/SPECS      | spec文件目录    | 保存.spec文件目录 |
| ~/rpmbuild/SRPMS      | 源码包.src.rpm目录    | 生成保存源码的SRPM文件目录 |
| ~/rpmbuild/BUILDROOT      | 最终安装目录    | 保存%install阶段需要安装文件 |


一般情况，您应该把源代码包，比如由开发者发布的以 `.tar.gz` 结尾的文件，放入 `~/rpmbuild/SOURCES` 目录。将`.spec` 文件放入 `~/rpmbuild/SPECS` 目录，并命名为 "*软件包名*.spec" 。当然， *软件包名* 就是最终 RPM 包的名字。为了创建二进制（Binary RPM）和源码软件包（SRPM），您需要将目录切换至 `~/rpmbuild/SPECS` 并执行：

```
 $ rpmbuild -ba NAME.spec
```

当执行此命令时，`rpmbuild` 会自动读取 `.spec` 文件并按照2.2.1 章节中表列出的步骤完成构建。

## 2、SPEC中相关字段的说明

### 2.1 一个简易的SPEC模板，根据模板的相关字段说明

```
Name:
Version:
Release:	1
Summary:
License:
URL:
Source0:
BuildArch： 

Patch0：

BuildRequires:
Requires:

%description

%prep
%setup -q

%build
%configure
make %{?_smp_mflags}

%install
rm -rf %{buildroot}
make install DESTDIR=%{buildroot}

%clean
rm -rf %{buildroot}

%files
%defattr(-,root,root,-)
%doc

%changelog
```

- **Name**: 软件包名，应与 SPEC 文件名一致。
- **Version**: 上游版本号。
- **Release**: 发行编号。初始值为 1
- **Summary**: 一行简短的软件包介绍。
- **License**: 授权协议，必须是开源许可证。
- **URL**: 该软件包的项目主页。***注意：源码包 URL 请使用 Source0 指定。***
- **Source0**: 软件源码包的 URL 地址。"`Source`" 与 "`Source0`" 相同。**强烈建议**提供完整 URL 地址，文件名用于查找 `SOURCES` 目录。如果可能，建议使用 `%{name}` 和 `%{version}` 替换 URL 中的名称/版本，这样更新时就会自动对应。如果有多个源码包，请用 `Source1`，`Source2` 等依次列出。如果你需要添加额外文件，请将它们列在后面。
- **Patch0**: 用于源码的补丁名称。如果你需要在源码包解压后对一些代码做修改，你应该修改代码并使用 diff 命令生成 patch 文件，然后放在 `~/rpmbuild/SOURCES` 目录下。一个 Patch 应该只做一种修改，所以可能会包含多个 patch 文件。
- **BuildArch**: 如果你要打包的文件不依赖任何架构（例如 shell 脚本，数据文件），请使用 "`BuildArch: noarch`"。RPM 架构会变成 "`noarch`"。
- **BuildRequires**: 编译软件包所需的依赖包列表，以逗号分隔。此标签可以多次指定。编译依赖 *不会* 自动判断，所以需要列出编译所需的*所有*依赖包。如果有必要，你可以指定需要的最低版本（例："`ocaml >= 3.08`"）。
- **Requires**: 安装软件包时所需的依赖包列表，以逗号分隔。请注意， BuildRequires 标签是编译所需的依赖，而 Requires 标签是安装/运行程序所需的依赖。大多数情况下，`rpmbuild` 会自动探测依赖，所以可能不需要 Requires 标签。然而，你也可以明确标明需要哪些软件包，或由于未自动探测所需依赖而需要手动标明。
- **%description**: 程序的详细/多行描述，请使用美式英语。每行必须小于等于 80 个字符。
- **%prep**: 打包准备阶段执行一些命令（如，解压源码包，打补丁等），以便开始编译。一般仅包含 "`%autosetup`"；如果源码包需要解压并切换至 `NAME` 目录，则输入 "`%autosetup -n NAME`"。查看 %prep 部分了解更多信息。
- **%build**: 包含构建阶段执行的命令，构建完成后便开始后续安装。程序应该包含有如何编译的介绍。查看 %build 部分了解更多信息。
- **%install**: 包含安装阶段执行的命令。命令将文件从 `%{_builddir}` 目录安装至 `%{buildroot}` 目录。查看 %install 部分了解更多信息。
- **%check**: 包含测试阶段执行的命令。此阶段在 %install 之后执行，通常包含 "`make test`" 或 "`make check`" 命令。此阶段要与 %build 分开，以便在需要时忽略测试。

- **%files**: 需要被打包/安装的文件列表。查看 %files 部分了解更多信息。
- **%changelog**: RPM 包变更日志。
- **ExcludeArch**: 排除某些架构。如果该软件不能在某些架构上正常编译或工作，通过该标签列出。
- **ExclusiveArch**: 列出该软件包独占的架构。

### 2.2 rpmbuild涉及的spec各阶段说明

#### 2.2.1 各阶段主要的动作说明

| 阶段       | 读取的目录     | 写入的目录     | 具体动作                                                     |
| ---------- | -------------- | -------------- | ------------------------------------------------------------ |
| %prep      | %_sourcedir    | %_builddir     | 读取位于  %_sourcedir 目录的源代码和 patch 。之后，解压源代码至 %_builddir 的子目录并应用所有 patch。 |
| %build     | %_builddir     | %_builddir     | 编译位于 %_builddir  构建目录下的文件。通过执行类似 ./configure && make 的命令实现。 |
| %install   | %_builddir     | %_buildrootdir | 读取位于 %_builddir  构建目录下的文件并将其安装至 %_buildrootdir 目录。这些文件就是用户安装 RPM 后，最终得到的文件。 |
| %check     | %_builddir     | %_builddir     | 检查软件是否正常运行。通过执行类似  make test 的命令实现。   |
| %files     | %_buildrootdir | %_rpmdir       | 读取位于  %_buildrootdir 最终安装目录下的文件，以便最终在 %_rpmdir 目录下创建 RPM 包。在该目录下，不同架构的 RPM  包会分别保存至不同子目录， noarch 目录保存适用于所有架构的 RPM 包。这些 RPM 文件就是用户最终安装的 RPM 包 |
| %changelog | NA             | NA             | 记录spec的修改日志                                           |

#### 2.2.2 各阶段刨析

1、%prep 部分 描述了解压源码包的方法。

一般而言，其中包含 "`%autosetup`" 命令。另外，还可以使用 "`%setup`" 和 "`%patch`" 命令来指定操作 Source0 等标签的文件。

 a) %autosetup命令：命令用于解压源码包。可用选项包括：

```
-n name : 如果源码包解压后的目录名称与 RPM 名称不同，此选项用于指定正确的目录名称。例如，如果 tarball 解压目录为 FOO，则使用 "%autosetup -n FOO"。
-P1 ：用于打补丁
```

举例：

```
%autosetup -n FOO-%version -p1
```

b) %setup 命令： 命令用于解压源码包。并切换到目录，一般与%patch命令搭配使用，可用选项包括：

```
-q 抑止不必要的输出。
```

举例：

```
%prep
%setup -q
%patch0 -p1
```

c) 该阶段未修改文件，如下：

```
%prep
cp %{SOURCE0} .
```

2、 %build 部分 可以配置，并编译用于安装的文件。

`a) configure` 进行配置。

默认情况下，文件会安装到前缀为 "`/usr/local`" 的路径下，对于手动安装很合理。然而，打包时需要修改前缀为 "`/usr`"。

共享库路径视架构而定，安装至 `/usr/lib` 或 `/usr/lib64` 目录。

由于 GNU `configure` 很常见，可使用 "`%configure`" 宏来自动设置正确选项（例如，设置前缀为 `/usr`）。一般用法如下：

```
 %configure
 make %{?_smp_mflags}
```

b) make 需要覆盖 makefile 变量，请将变量作为参数传递给 `make`：

```
make %{?_smp_mflags} CFLAGS="%{optflags}" BINDIR=%{_bindir}
```

3、 %install 部分包含安装阶段需要执行的命令，即从 `%{_builddir}` 复制相关文件到 `%{buildroot}` 目录（通常表示从 `~/rpmbuild/BUILD` 复制到 `~/rpmbuild/BUILDROOT`) 目录，并根据需要在 `%{buildroot}` 中创建必要目录。

举例

```
%install
rm -rf %{buildroot} 
%make_install
```

该阶段容易混淆的说法

- "build 目录"，也称为 `%{_builddir}`，实际上与 "build root"，又称为 `%{buildroot}`，是不同的目录。在前者中进行编译，并将需要打包的文件从前者复制到后者。
- 在 %build 阶段，当前目录为 `%{buildsubdir}`，是 %prep 阶段中在 `%{_builddir}` 下创建的子目录。这些目录通常名为 `~/rpmbuild/BUILD/%{name}-%{version}`。
- %install 阶段的命令**不会**在用户安装 RPM 包时执行，此阶段仅在打包时执行。

4、%check 部分：用于运行测试用例

一般写为

```
make test
or
make check
```

5、%files 部分是文件段，主要用来说明会将 `%{buildroot}` 目录下的哪些文件和目录最终打包到rpm包里。

这里会在虚拟根目录下进行，千万不要写绝对路径，而应用宏或变量表示相对路径。

一般写为如下：

```
%files
%defattr (-,root,root,0755)                         ← 设定默认权限
%config(noreplace) /etc/my.cnf                      ← 表明是配置文件，noplace表示替换文件
%doc %{src_dir}/Docs/ChangeLog                      ← 表明这个是文档
%attr(644, root, root) %{_mandir}/man8/mysqld.8*    ← 分别是权限，属主，属组
%attr(755, root, root) %{_sbindir}/mysqld
%exclude %{_libdir}/debug
```

注意

a）%exclude 列出不想打包到 rpm 中的文件。注意：如果 `%exclude` 指定的文件不存在，也会出错的。

b）打包时候一般遵守文件系统层次标准

```
可执行文件保存在 /usr/bin，配置文件保存在 /etc， 共享库保存在 /usr/lib（或 /usr/lib64）等等。只有一个例外：不需要用户或管理员直接执行的可执行文件，应保存至 /usr/libexec 子目录，子目录通过 %{_libexecdir}/%{name} 宏来引用。不要将文件安装到 /opt 或 /usr/local 目录中。
```

6、%changelog 部分，本段是修改日志段，记录 spec 的修改日志段。你可以将软件的每次修改记录到这里，保存到发布的软件包中，以便查询之用。

相关格式

- 第一行是：`* 星期 月 日 年 修改人 电子信箱`。其中：星期、月份均用英文形式的前 3 个字母，用中文会报错。后面-加对应的版本
- 接下来的行写的是修改了什么地方，可写多行。一般以减号开始，便于后续的查阅。

```
%changelog
* Tue Jun 20 2023 xu_ping <707078654@qq.com> - 1.0.0-1
- init package
```

## 3、常见宏介绍

宏通常以 `%{string}` 格式出现，以下介绍常见的宏：

| 宏名称             | 典型扩展               | 意义                                                         |
| :----------------- | :--------------------- | :----------------------------------------------------------- |
| `%{_bindir}`       | `/usr/bin`             | 二进制目录：保存可执行文件                                   |
| `%{_builddir}`     | `~/rpmbuild/BUILD`     | 构建目录：软件在 build 的子目录被编译。参考 `%buildsubdir`   |
| `%{buildroot}`     | `~/rpmbuild/BUILDROOT` | Build root：`%install` 阶段中，将 `%{_builddir}` 子目录下的文件复制到 `%{buildroot}` 的子目录（之前，`%{buildroot}` 使用的位置为 "/var/tmp/"） |
| `%{buildsubdir}`   | `%{_builddir}/%{name}` | 构建子目录：`%build` 阶段中，文件会在 `%{_builddir}` 的子目录中编译。此宏在 `%autosetup` 之后设置 |
| `%{_datadir}`      | `/usr/share`           | 共享数据目录                                                 |
| %{_defaultdocdir}  | `/usr/share/doc`       | 默认文档目录                                                 |
| `%{_includedir}`   | `/usr/include`         | 程序头文件目录                                               |
| `%{_infodir}`      | `/usr/share/info`      | info 手册目录                                                |
| `%{_initrddir}`    | `/etc/rc.d/init.d`     | init 脚本目录                                                |
| `%{_libdir}`       | `/usr/lib`             | 共享库目录                                                   |
| `%{_libexecdir}`   | `/usr/libexec`         | 仅由系统调用执行该目录中的命令                               |
| %{_localstatedir}  | `/var`                 | 保存缓存/日志/lock等信息的目录                               |
| `%{_mandir}`       | `/usr/share/man`       | man 手册目录                                                 |
| `%{name}`          |                        | 软件包名称，通过 Name: tag 设置                              |
| `%{_sbindir}`      | `/usr/sbin`            | 保存管理员可执行命令                                         |
| %{_sharedstatedir} | `/var/lib`             | 保存程序运行所处理的文件                                     |
| `%{_sysconfdir}`   | `/etc`                 | 配置文件目录                                                 |
| `%{version}`       |                        | 软件包版本，通过 Version: tag 设置                           |

RPM 内建宏定义在 `/usr/lib/rpm//macros` 文件中，这些宏基本上定义了目录路径或体系结构等等；同时也包含了一组用于调试 spec 文件的宏。

```
通过 rpm --eval "%{macro}" 来查看具体对应路径。
```

譬如

```
rpm --eval "%{ _bindir}"
```

还可以通过解压spec文件来查看spec中宏的定义

譬如：

```
rpmspec -P FOO.spec
```

## 4、spec编写openEuler常用场景

1、软件包升级

参考文档：[软件包升级流程](http://gitee.com/cherry530/doc/blob/master/%E8%BD%AF%E4%BB%B6%E5%8C%85%E5%8D%87%E7%BA%A7%E6%B5%81%E7%A8%8B.md)

2、软件包引入

参考文档：[软件包引入流程](http://gitee.com/cherry530/doc/blob/master/%E8%BD%AF%E4%BB%B6%E5%8C%85%E5%BC%95%E5%85%A5%E6%B5%81%E7%A8%8B.md)

3、补丁回合

参考文档：[patch回合相关指导](http://gitee.com/cherry530/doc/blob/master/patch%E5%9B%9E%E5%90%88%E7%9B%B8%E5%85%B3%E6%8C%87%E5%AF%BC.md)