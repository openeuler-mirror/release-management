openEuler社区及其它第三方开发者共同提供了丰富易用的软件包，并根据这些软件包的来源、质量属性、维护方式等不同维度划分为先三类openEuler社区软件仓库，openEuler社区版本使用者可以根据自己的需求配置不同的软件仓库；

##  openEuler提供的基本软件仓库
-  **OS** --- openEuler LTS和创新版正式发布的基础软件包集合仓库，该仓库由linux操作系统常用软件包集合而成，包括基本OS必须的软件包和linux常用且提供重要功能的软件包，该集合内软件包依赖关系稳定，无须依赖其余仓库，均可正常安装使用；
-  **Everything** --- openEuler LTS和创新版本正式发布的全量软件包集合仓库，该仓库所有软件包根据openEuler社区软件质量属性规范，均完成了openEuler社区全流程质量保证。该集合内全量软件包依赖关系稳定，无须依赖其余仓库，均可正常编译、构建和安装使用；

##  openEuler提供的附加软件仓库
-  **update** --- openEuler LTS和创新版正式发布的OS和Everything仓库中软件包定期更新集合仓库，属于OS和Everything仓库的子集，用于解决软件包bugfix和CVE安全漏洞修复，update仓库通常同时存在一个软件的多个版本的更新；
-  **EPOL(Extra Packages for openEuler Linux )** --- 作为openEuler LTS和创新版本软件包仓库的补充，为openEuler社区提供尽可能丰富的软件包。该仓库软件包**源码均需要来源于openEuler社区**，同时因受社区软件包质量、技术成熟度、社区参与者投入等原因暂时无法完全满足openEuler社区软件包发布质量及维护支持要求，但openEuler社区从开源社区使用者角度来考虑，提供这类软件包供社区爱好者使用，同时明确无法为该类软件包提供bugfix和CVE安全漏洞修复；EPOL软件仓无法独立编译、构建和完整安装，该仓库需要结合OS、Everithing仓库一起使用；
-  **debuginfo** ---  openEuler LTS和创新版正式发布的OS和Everything仓库中软件包的debuginfo包，这些包中默认带着编译时所添加的调试符号信息，用于gdb调试使用。该软件仓库默认情况下不在系统yum配置文件中，使用者根据需要自行配置。
-  **source** --- openEuler LTS和创新版正式发布的全量软件包源码包集合仓库，提供给使用者重新构建自定义RPM包；同时请考虑重建 SRPM 将会为你带来的额外的工作负担，即每当该包有安全CVE漏洞更新发布时，你需要重新获取该包source包重新构建，已解决问题及安全漏洞；
-  **docker_img** --- openEuler LTS和创新版正式发布的基础容器镜像，供使用者快速创建一个基础容器工作环境；
-  **virtual_machine_img** ---  openEuler LTS和创新版正式发布的基础虚拟机镜像，供使用者快速创建一个基础linux操作系统工作环境；openEuler社区虚拟机镜像格式默认支持qcow2，其余格式敬请期待。
-  **netinstall** --- openEuler LTS和创新版提供的最小的CD镜像文件，供使用者通过网络安装方式快速安装一个基础linux操作系统；netinstall iso仅可用于匹配的openEuler发行版，例如，openEuler 20.03-LTS-SP1的netinstall仅可用来安装openEuler 20.03-LTS-SP1。
-  **raspi_img** --- openEuler创新版本针对树莓派硬件架构，提供基础树莓派虚拟机镜像，供使用者快速创建一个基础树莓派虚拟机工作环境；

##  openEuler提供的第三方软件仓库
-  **extras** --- 非openEuler社区提供编译、构建的软件包，可以兼容openEuler LTS和创新版本，并且不破坏openEuler各版本软件包原有兼容性和依赖关系，仅作为openEuler LTS和创新版本软件包仓库的第三方软件包补充，为openEuler社区使用者提供尽可能丰富的软件包选择。
-  **RISCV** --- 基于openEuler社区提供编译环境独立编译、构建的软件包，用于支持RISCV架构系统的软件包仓库结合，当前该架构处于技术快速开发阶段，openEuler社区当前不承诺正式商用及相关安全漏洞SLA达成；