# 软件包分层策略
|分层|特征|举例|
|:-|:-----|:-|
|L1|运行在数据面的关键软件；运行在控制面、管理面，可能会导致现网事故的组件（如升级相关软件等）；处于攻击路径的开源软件|openssh、dpdk|
|L2|运行在控制面、管理面，常驻系统或高频执行的软件，且社区活跃|systemd|
|L3|社区成熟，运行在管理面，使用频率低且功能稳定|bash、vim|
|L4|不在生产环境运行的软件。如：工具类软件|make|

# 软件包分层质量策略
|分层|维护要求|发布目录要求|兼容性要求|测试要求|
|:-|:----|:--|:---|:----|
| L1 | 1. 例行<font color="#0000dd">按周</font>同步社区补丁/按<font color="#0000dd">牵引SLA</font>进行修复<br>2. maintainer/committer梳理代码关键流程，有自维护自演进能力；回馈上有社区，建立上游影响力 | <font color="#dd0000">BaseOS</font> | 软件包及API、ABI在某个LTS版本的生命周期保持不变，<font color="#0000dd">跨LTS版本不保证兼容性</font> | 1. 基于开源测试套开展测试<br>2. 补充专项/DFX测试 |
| L2 | 1. 例行<font color="#0000dd">按双周</font>同步社区补丁<br>2. 漏洞按<font color="#0000dd">牵引SLA</font> | <font color="#dd0000">BaseOS</font> | 软件包及API、ABI在某个SP版本的生命周期保持不变，<font color="#0000dd">跨SP版本不保证兼容性</font> | 1. 基于开源测试套开展测试<br>2. 结合使用场景测试 |
| L3 | 1. 例行<font color="#00000dd">按月</font>同步社区补丁<br>2. 漏洞按<font color="#0000dd">牵引SLA</font> | <font color="#dd00000">BaseOS</font> | 不做兼容性保证 | 1. 基于开源测试套开展测试 |
| L4 | 1. 例行<font color="#00000dd">按月</font>同步社区高危漏洞/关键BUG | <font color="#0000dd">Everything</font> | 不做兼容性保证 | 1. 基于开源测试套开展测试 |
| 不涉及 | 1. 被动响应社区漏洞BUG | EPOL | 不做兼容性保证 | 1. 保障RPM维度功能可用 |

若对以上策略存在疑问，欢迎在RM-sig的双周例会进行讨论。