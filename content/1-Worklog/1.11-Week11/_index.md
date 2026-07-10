---
title: "Week 11 Worklog"
date: 2026-06-29
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Week 11 Objectives:

* Conduct user testing and responsive testing in the production environment.
* Identify and resolve UI/UX bugs and frontend logic issues.
* Improve component stability and overall user experience.
* Prepare the User Guide and demo script for final presentation.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2   | - Plan testing scope: features, devices, browsers, and user roles (Host, Player) <br> - Prepare test cases covering: signup, login, quiz creation, room creation, joining room, gameplay, leaderboard, and results <br> - Set up testing devices: desktop, tablet, and mobile | 06/29/2026 | 06/29/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3   | - **Production testing:** Host user flow <br>&emsp; + Test signup → login → quiz creation → room creation → game start → question control → game end <br>&emsp; + Verify Host can control game flow without errors <br>&emsp; + Test responsive behavior on desktop and tablet <br>&emsp; + Document all bugs and unexpected behaviors found during testing | 06/30/2026 | 06/30/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - **Production testing:** Player user flow <br>&emsp; + Test join room → waiting room → gameplay → answer submission → leaderboard → results <br>&emsp; + Test with multiple simultaneous Player sessions <br>&emsp; + Test responsive behavior on mobile devices <br>&emsp; + Test WebSocket reconnection behavior when connection drops mid-game | 07/01/2026 | 07/01/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - **Bug fixing and UX improvement:** <br>&emsp; + Fix UI misalignment and layout issues on smaller screens <br>&emsp; + Fix frontend logic bugs: answer submission edge cases, timer sync issues <br>&emsp; + Improve error messages for better user guidance <br>&emsp; + Improve loading states and transitions between game phases <br>&emsp; + Verify all fixes in production environment after deployment | 07/02/2026 | 07/02/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - **Documentation preparation:** <br>&emsp; + Write User Guide: describe how to sign up, create a quiz, host a game, and join as a player <br>&emsp; + Add screenshots to User Guide for each major step <br>&emsp; + Prepare demo script: define the flow and talking points for stakeholder presentation <br>&emsp; + Review documentation for clarity, accuracy, and completeness | 07/03/2026 | 07/03/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Week 11 Achievements:

* Conducted comprehensive user testing in the production environment covering Host and Player user flows.

* Tested responsive behavior on desktop, tablet, and mobile devices — issues were identified and resolved.

* Fixed UI/UX bugs including layout misalignment, error message inconsistency, and loading state gaps.

* Fixed frontend logic issues related to answer submission edge cases and timer synchronization.

* Improved component stability and user experience across all major game phases.

* Completed the User Guide with screenshots and prepared the demo script for the final presentation.
