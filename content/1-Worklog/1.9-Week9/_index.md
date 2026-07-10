---
title: "Week 9 Worklog"
date: 2026-06-15
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---
### Week 9 Objectives:

* Develop the Host gameplay page with question control functionality.
* Develop the Player gameplay page with answer submission.
* Integrate a real-time leaderboard and score updates during gameplay.
* Build the final Game Results page and test the complete game flow.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2   | - Design gameplay state machine: waiting → in-progress → question → answer → leaderboard → ended <br> - Plan WebSocket message types for gameplay: startGame, showQuestion, submitAnswer, showLeaderboard, endGame <br> - Design Host and Player gameplay page wireframes | 06/15/2026 | 06/15/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3   | - **Practice:** Develop Host gameplay page <br>&emsp; + Display current question number, question text, and answer options <br>&emsp; + Show countdown timer for each question <br>&emsp; + Implement Next Question button: sends WebSocket action to advance the game <br>&emsp; + Display answer submission progress (number of players who have answered) <br>&emsp; + Handle End Game action and transition to results page | 06/16/2026 | 06/16/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - **Practice:** Develop Player gameplay page <br>&emsp; + Display question and answer options received via WebSocket <br>&emsp; + Implement answer selection: highlight selected answer, disable re-selection after submission <br>&emsp; + Send selected answer to backend via WebSocket on selection <br>&emsp; + Display feedback after answer submission (waiting for next question) <br>&emsp; + Handle game state transitions: question → waiting → next question → game ended | 06/17/2026 | 06/17/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - **Practice:** Integrate real-time leaderboard <br>&emsp; + Display leaderboard between questions: rank, player name, and current score <br>&emsp; + Update scores in real time when backend broadcasts score update event <br>&emsp; + Animate leaderboard rank changes for better user experience <br>&emsp; + Handle tie-breaking display logic | 06/18/2026 | 06/18/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - **Practice:** Develop Game Results page <br>&emsp; + Display final rankings: top 3 podium and full player list with final scores <br>&emsp; + Provide option to return to Dashboard or start a new game <br>&emsp; + Test the complete game flow: room creation → player join → game start → answer questions → leaderboard → results <br>&emsp; + Fix any issues found during end-to-end testing | 06/19/2026 | 06/19/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Week 9 Achievements:

* Developed the Host gameplay page with full question control, countdown timer, and answer progress tracking.

* Developed the Player gameplay page with answer selection, real-time feedback, and smooth state transitions.

* Integrated a real-time leaderboard that updates scores dynamically after each question via WebSocket events.

* Built the final Game Results page displaying the full ranking and final scores for all players.

* Completed end-to-end testing of the full game flow from room creation to final results display.

* The core SyncQuiz gameplay experience is fully functional on the frontend.