# Version Info
openEuler 26.09-DevStation is an innovation release for DevStation scenarios. For the release lifecycle, see [openEuler lifecycle](https://www.openeuler.org/en/other/lifecycle/). This release focuses on developer workstations, intelligent development tools, software store, mcpmarket, skillhub, agentStore, development environment management, and desktop development experience. It provides more features and capabilities, bringing developers and users a native openEuler AI-Native Operating System experience.<br>


# Release Plan

| Stage Name                    | Deadline for PR | Begin Time | End Time   | Days | Note                                     |
| ----------------------------- | --------------- | ---------- | ---------  | ---- | ---------------------------------------- |
| Collect key features          |        -        | 2026/06/01 | 2026/07/30 | 60 | Collect release requirements                              |
| Change Review 1               |        -        | 2026/07/01 | 2026/08/13 | 44 | Review package changes, including upgrade, retirement, and removal  |
| Herited features              |        -        | 2026/07/01 | 2026/08/13 | 44 | Merge inherited features before Beta |
| Develop                       |        -        | 2026/07/01 | 2026/09/03 | 65 | Develop new features. Merge into Master before branching, and merge into Master plus 26.09-DevStation after branching before round 6 freeze |
| Kernel freezing               |        -        | 2026/07/01 | 2026/08/13 | 44 | Kernel freeze, aligned with the Beta version |
| Branch 26.09-DevStation        |        -        | 2026/07/16 | 2026/07/22 | 07 | Create the 26.09-DevStation branch from Master |
| Build & Alpha                 |    2026/07/23   | 2026/07/25 | 2026/08/07 | 14 | Merge new features and release Alpha. Focus on software selection and build issues |
| Test round 1                  |    2026/08/06   | 2026/08/08 | 2026/08/14 | 07 | 26.09-DevStation module test |
| Test round 2 (Beta Version)   |    2026/08/13   | 2026/08/15 | 2026/08/21 | 07 | 26.09-DevStation Beta release and KABI baseline |
| Change Review 2               |        -        | 2026/08/15 | 2026/08/20 | 06 | Start package removal review |
| Test round 3                  |    2026/08/20   | 2026/08/22 | 2026/08/28 | 07 | 26.09-DevStation module test |
| Test round 4                  |    2026/08/27   | 2026/08/29 | 2026/09/04 | 07 | Full validation, including full SIT |
| Change Review 3               |        -        | 2026/08/29 | 2026/09/03 | 06 | Start package removal review |
| Test round 5                  |    2026/09/03   | 2026/09/05 | 2026/09/11 | 07 | Branch freeze. Only bug fixes are allowed |
| Test round 6                  |    2026/09/10   | 2026/09/12 | 2026/09/18 | 07 | Regression test |
| Test round 7 (reserved)       |    2026/09/17   | 2026/09/19 | 2026/09/24 | 06 | Regression test |
| Release Review                |        -        | 2026/09/22 | 2026/09/26 | 05 | Release decision: Go or No Go |
| Release preparation           |        -        | 2026/09/24 | 2026/09/26 | 03 | Prepare release deliverables |
| Release                       |        -        | 2026/09/28 | 2026/09/30 | 03 | Official release after community Release review |

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
|TBD|Collect key features for the DevStation release|Discussion|sig-intelligence|TBD|Everything|TBD|

# Requirement and Feature Feedback Process <br />
1. Developers or SIGs should add requirements and features to this table, including the requirement issue and link, before the collection deadline.<br>
2. Submit the requirement for review at the release management SIG meeting. The owner or SIG maintainer should attend the meeting.
<br><br>
