---
title: "Week 3 Worklog"
date: 2026-05-04
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---
### Week 3 Objectives:

* Learn about Amazon Cognito and its role in user authentication.
* Learn about Amazon API Gateway and how to build REST APIs on AWS.
* Learn about API Gateway WebSocket API for real-time communication.
* Analyze how Cognito, API Gateway, and WebSocket API apply to the SyncQuiz project.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2   | - Study Amazon Cognito: overview, purpose, and key components <br>&emsp; + User Pools: user registration, login, and identity management <br>&emsp; + App Clients: application-level access configuration <br>&emsp; + JWT tokens: ID token, access token, and refresh token <br> - Understand the Cognito signup and login flow | 05/04/2026 | 05/04/2026 | <https://docs.aws.amazon.com/cognito/latest/developerguide/> |
| 3   | - Study Amazon API Gateway: overview and how to build REST APIs on AWS <br>&emsp; + Resources and routes, HTTP methods, and request/response mapping <br>&emsp; + Lambda proxy integration: connecting API Gateway to Lambda functions <br>&emsp; + Authorizers: using Cognito JWT Authorizer to protect API routes <br>&emsp; + CORS configuration for frontend communication | 05/05/2026 | 05/05/2026 | <https://docs.aws.amazon.com/apigateway/latest/developerguide/> |
| 4   | - **Practice:** Connect API Gateway with AWS Lambda <br>&emsp; + Create a REST API in API Gateway <br>&emsp; + Create routes and integrate with Lambda functions <br>&emsp; + Add Cognito JWT Authorizer to protect a protected route <br>&emsp; + Test using Postman or API Gateway console | 05/06/2026 | 05/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Study API Gateway WebSocket API for real-time applications <br>&emsp; + Understand the WebSocket connection lifecycle: $connect, $disconnect, $default routes <br>&emsp; + Learn how clients connect, send messages, and receive broadcast messages <br>&emsp; + Study how Lambda handles WebSocket messages and manages connection IDs | 05/07/2026 | 05/07/2026 | <https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-websocket-api.html> |
| 6   | - Analyze how Cognito, API Gateway, and WebSocket API can be applied to the SyncQuiz project <br>&emsp; + Cognito: authenticate hosts and manage user sessions <br>&emsp; + REST API: quiz CRUD, room creation, and player joining operations <br>&emsp; + WebSocket API: real-time game communication, player lists, and live leaderboards <br> - Take design notes for the SyncQuiz backend architecture | 05/08/2026 | 05/08/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Week 3 Achievements:

* Learned Amazon Cognito and understood User Pools, App Clients, and the JWT token-based authentication flow.

* Studied Amazon API Gateway and understood how to build REST APIs with Lambda integration and Cognito JWT Authorizer.

* Successfully practiced connecting API Gateway with a Lambda function and tested a protected route using Cognito.

* Learned about API Gateway WebSocket API and understood the connection lifecycle, message routing, and how Lambda handles real-time messages.

* Analyzed how Cognito, API Gateway REST API, and WebSocket API can be applied to the SyncQuiz project: Cognito for user authentication, REST API for quiz and room management, and WebSocket API for real-time gameplay communication and live leaderboards.