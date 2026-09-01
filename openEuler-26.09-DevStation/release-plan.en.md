# Version Info
openEuler 26.09-DevStation is an innovation release for DevStation scenarios. For the release lifecycle, see [openEuler lifecycle](https://www.openeuler.org/en/other/lifecycle/). This release focuses on developer workstations, intelligent development tools, software store, mcpmarket, skillhub, agentStore, development environment management, and desktop development experience. It provides more features and capabilities, bringing developers and users a native openEuler AI-Native Operating System experience.<br>


# Release Plan

| Stage Name | Deadline for PR | Begin Time | End Time | Days | Note |
|------------|-----------------|------------|----------|------|------|
| Collect key features | - | 2026/06/01 | 2026/07/30 | 60 | Collect release requirements |
| Change Review 1 | - | 2026/07/01 | 2026/08/15 | 46 | Review package changes (upgrade, retirement, removal) |
| Inherited features | - | 2026/07/01 | 2026/08/15 | 46 | Merge inherited features (must be completed before Beta) |
| Development | - | 2026/07/01 | 2026/09/02 | 64 | Develop new features. Merge into Master before branching; after branching, merge into both 26.09‑DevStation and Master. The 6.6 kernel must be merged into the 26.09 branch before round 6 freeze. |
| Kernel freezing | - | 2026/07/01 | 2026/08/15 | 46 | Kernel freeze (aligned with the Beta version) |
| Branch 26.09‑DevStation | - | 2026/07/20 | 2026/07/31 | 12 | Create the 26.09‑DevStation branch from Master; additionally create a 26.09 kernel branch for the 6.6 version |
| Build & Alpha | 2026/08/05 | 2026/08/07 | 2026/08/13 | 07 | Merge new features, release Alpha version (focus on software selection and build issues) |
| Test round 1 | 2026/08/12 | 2026/08/14 | 2026/08/20 | 07 | 26.09‑DevStation module test |
| Test round 2 (Beta Version) | 2026/08/19 | 2026/08/21 | 2026/08/27 | 07 | 26.09‑DevStation Beta release (KABI baseline) |
| Change Review 2 | - | 2026/08/21 | 2026/08/26 | 06 | Initiate package removal review |
| Test round 3 | 2026/08/26 | 2026/08/28 | 2026/09/03 | 07 | 26.09‑DevStation module test |
| Test round 4 | 2026/09/02 | 2026/09/04 | 2026/09/10 | 07 | Full validation (full SIT) |
| Change Review 3 | - | 2026/09/04 | 2026/09/09 | 06 | Initiate package removal review |
| Test round 5 | 2026/09/09 | 2026/09/11 | 2026/09/17 | 07 | Branch freeze, only bug fixes allowed |
| Test round 6 | 2026/09/16 | 2026/09/18 | 2026/09/23 | 07 | Regression test |
| Release Review | - | 2026/09/21 | 2026/09/24 | 04 | Release decision / Go or No Go |
| Release preparation | - | 2026/09/23 | 2026/09/24 | 02 | Pre‑release preparation, organize release artifacts |
| Release | - | 2026/09/28 | 2026/09/30 | 03 | Official release after community Release review approval |

* ```Deadline for PR```: Build start time, which is also the time when PRs stop being accepted for this build. The build starts after 20:00 on that day.
* ```Begin Time```: Test handoff start time. Test images, AT smoke tests, and release preparation should be completed before 09:00 on that day.
* ```End Time```: Test handoff end time, which is one day before the next ```Begin Time```. The QA team should submit all issues found in this round before the end time.


# Code Merge Notes
The innovation release inherits code from the master branch.<br>
// Please merge and self-verify new feature code in time, following the overall plan and before the first test handoff.


# Feature List
Status description: Discussion (requirement under discussion and not accepted), Developing, Testing, Accepted.<br>
Release channels: ISO, Everything, EPOL, oepkgs, standalone release, and others.

|No.|Feature|Status|SIG|Owner|Release channel|Related packages|
|:----|:---|:---|:--|:----|:----|:----|
| [2561](https://atomgit.com/openeuler/release-management/issues/2561) | [openEuler 26.09 Innovation][Agent Infra][Agent Scheduling] Build a context management system with on‑demand loading via data referencing to reduce context length | Developing | sig-Intelligence | [@linpengcheng1994](https://gitcode.com/linpengcheng1994)     | EPOL | sccs |
| [2562](https://atomgit.com/openeuler/release-management/issues/2562) | [openEuler 26.09 Innovation][Agent Infra][Observability & Governance] Build a foundational framework for observability and governance that provides end-to-end full-link observability, security protection, and audit capabilities | Developing | sig-Intelligence | [@yaozhenhe](https://gitcode.com/yaozhenhe)     | EPOL | AcTrail |
| [2563](https://atomgit.com/openeuler/release-management/issues/2563) | [openEuler 26.09 Innovation][Agent Infra][Agent Scheduling] Collaborative Agent/KVC Scheduling: KVC scheduling that is aware of "Agent semantics" to reduce inference waiting latency for Agents | Developing | sig-Intelligence | [@xtchen](https://gitcode.com/xtchen)     | EPOL | RAM-A |
| [2564](https://atomgit.com/openeuler/release-management/issues/2564) | [openEuler 26.09 Innovation][AI Infra][Inference Acceleration] Hierarchical collaboration between DDR and HBM, aggregated transfer for KV swapping, and reduced average latency for long‑sequence (>64K) inference scenarios with multiple batch sizes | Developing | sig-Intelligence | [@zxstty](https://gitcode.com/zxstty)     | EPOL | sysHAX |
| [2565](https://atomgit.com/openeuler/release-management/issues/2565) | [openEuler 26.09 Innovation][Developer Ecosystem & Tools][skillhub] openEuler launches skillhub, bringing together the community's skill ecosystem | Developing | sig-Devstation | [@ftboy](https://gitcode.com/ftboy)     | Standalone release | wittyhub, wittyhub-cli |
| [2566](https://atomgit.com/openeuler/release-management/issues/2566) | [openEuler 26.09 Innovation][Developer Ecosystem & Tools][DevStation] openEuler DevStation: an innovative openEuler release that enables users and developers to quickly iterate and try out new features | Developing | sig-Devstation | [@w520203](https://gitcode.com/w520203) | Standalone release | gdm, gnome-shell,gnome-session,epkg,polymind |
| [2567](https://atomgit.com/openeuler/release-management/issues/2567) | [openEuler 26.09 Innovation][Developer Ecosystem & Tools][EPKG] Complete the default integration of EPKG into the openEuler DevStation release | Developing | sig-epkg | [@w520203](https://gitcode.com/w520203)     | Standalone release | epkg |
| [2568](https://atomgit.com/openeuler/release-management/issues/2568) | [openEuler 26.09 Innovation] oeaware: provides scenario‑based intelligent tuning skills | Developing | sig-Intelligence | [@cloudyyy1234](https://gitcode.com/cloudyyy1234)     | EPOL | witty-opentunex |
| [2569](https://atomgit.com/openeuler/release-management/issues/2569) | [openEuler 26.09 Innovation][AI][Model Acceleration] ModelFS userspace model loading optimization solution | Developing | sig-kernel | [@yubo-liu](https://gitcode.com/yubo-liu)     | ISO | kernel |
| [2570](https://atomgit.com/openeuler/release-management/issues/2570) | [openEuler 26.09 Innovation][AI Infra][Inference Acceleration] Multi‑level KV caching with direct SSD access, combined with UB‑accelerated cross‑node KV transfer, to reduce TTFT for long‑sequence inferenc | Developing | sig-kernel,sig-Long | [@qiao-yifan4](https://gitcode.com/qiao-yifan4),[@chloroethylene](https://gitcode.com/chloroethylene)     | ISO | kernel, LMCache,LMCache-Ascend |

# Requirement and Feature Feedback Process <br />
1. Developers or SIGs should add requirements and features to this table, including the requirement issue and link, before the collection deadline.<br>
2. Submit the requirement for review at the release management SIG meeting. The owner or SIG maintainer should attend the meeting.
<br><br>
