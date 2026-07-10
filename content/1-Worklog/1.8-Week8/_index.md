---
title: "Week 8 Worklog"
date: 2026-06-08
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---
### Week 8 Objectives:

* Develop Host and Player views for quiz room management.
* Integrate the WebSocket client into the frontend for real-time communication.
* Build the Waiting Room UI with real-time player list updates.
* Test WebSocket connection, disconnection, and live data synchronization.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2   | - Study WebSocket protocol and browser WebSocket API <br> - Review AWS API Gateway WebSocket API message structure and connection lifecycle <br> - Design real-time communication flow: connect, join room, broadcast player list, start game | 06/08/2026 | 06/08/2026 | <https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-websocket-api.html> |
| 3   | - **Practice:** Develop Host view for room creation <br>&emsp; + Create Host page: select quiz, generate room PIN, display room code to players <br>&emsp; + Connect Host to WebSocket on room creation <br>&emsp; + Display waiting room: show real-time player list as players join <br>&emsp; + Add Start Game button that sends game start signal via WebSocket | 06/09/2026 | 06/09/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - **Practice:** Develop Player view for joining rooms <br>&emsp; + Create Join Room page: input room code and player nickname <br>&emsp; + Connect Player to WebSocket after submitting room code <br>&emsp; + Display Waiting Room UI: show room code, waiting message, and player count <br>&emsp; + Handle player join confirmation and error messages (e.g., room not found, room full) | 06/10/2026 | 06/10/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - **Practice:** Integrate WebSocket client into frontend core <br>&emsp; + Create a centralized WebSocket service module (connect, disconnect, send, onMessage) <br>&emsp; + Handle WebSocket reconnection logic on connection drop <br>&emsp; + Parse incoming WebSocket messages by action type and dispatch to state <br>&emsp; + Update player list in real time as players join or leave the waiting room | 06/11/2026 | 06/11/2026 | <https://docs.aws.amazon.com/apigateway/latest/developerguide/websocket-api-develop-routes.html> |
| 6   | - Test WebSocket connection establishment and disconnection handling <br> - Verify real-time player list updates in both Host and Player views <br> - Simulate network interruption and test reconnection behavior <br> - Review and fix any race conditions or message ordering issues | 06/12/2026 | 06/12/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Week 8 Achievements:

* Developed the Host view for room creation, displaying the room PIN and managing the waiting room in real time.

* Developed the Player view with room code input flow and a Waiting Room UI showing live player information.

* Integrated a centralized WebSocket client service into the frontend for consistent message handling across all components.

* Implemented real-time player list updates in the Waiting Room using WebSocket push messages.

* Successfully tested WebSocket connection establishment, disconnection handling, and reconnection behavior.

* The system is ready to support real-time gameplay in the following week.