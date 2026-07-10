---
title: "Week 7 Worklog"
date: 2026-06-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---
### Week 7 Objectives:

* Develop Login and Signup pages integrated with Amazon Cognito.
* Build the user Dashboard and quiz management interface.
* Ensure secure session management using Cognito tokens.
* Test the complete authentication flow end-to-end.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2   | - Study Amazon Cognito SDK integration with React <br> - Review Cognito hosted UI vs custom UI approach <br> - Plan authentication flow: signup, login, token storage, logout, session persistence | 06/01/2026 | 06/01/2026 | <https://docs.amplify.aws/react/build-a-backend/auth/> |
| 3   | - **Practice:** Develop Login and Signup pages <br>&emsp; + Create Signup form: email, password, confirm password fields <br>&emsp; + Integrate Cognito SDK: signUp, confirmSignUp (OTP verification) <br>&emsp; + Create Login form: email and password fields <br>&emsp; + Integrate Cognito SDK: signIn, handle auth tokens <br>&emsp; + Store JWT tokens securely (localStorage / httpOnly cookie strategy) | 06/02/2026 | 06/02/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - **Practice:** Session management and route protection <br>&emsp; + Implement automatic token refresh using Cognito SDK <br>&emsp; + Handle session expiry and redirect to Login <br>&emsp; + Implement logout: clear tokens and redirect <br>&emsp; + Protect all authenticated routes using global auth state <br>&emsp; + Test login persistence across browser refresh | 06/03/2026 | 06/03/2026 | <https://docs.aws.amazon.com/cognito/latest/developerguide/> |
| 5   | - **Practice:** Develop Dashboard interface <br>&emsp; + Display authenticated user profile information (email, username) <br>&emsp; + Display quiz history: list of quizzes created by the user <br>&emsp; + Add navigation to quiz creation and game room creation <br>&emsp; + Implement responsive layout for the Dashboard page | 06/04/2026 | 06/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - **Practice:** Develop quiz management interface <br>&emsp; + Create form for creating a new quiz: title, description, category <br>&emsp; + Create form for adding questions: question text, answer options, correct answer, time limit <br>&emsp; + Implement quiz list view with edit and delete actions <br>&emsp; + Connect quiz management forms to HTTP API endpoints <br>&emsp; + Test end-to-end: create quiz → add questions → view on Dashboard | 06/05/2026 | 06/05/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Week 7 Achievements:

* Developed fully functional Login and Signup pages with Cognito SDK integration.

* Implemented secure session management: JWT tokens are stored and refreshed automatically via Cognito.

* Session persistence works correctly across browser refresh; expired sessions redirect users to the Login page.

* Built the user Dashboard displaying profile information and the quiz list.

* Developed the quiz management interface allowing users to create, edit, and delete quizzes with questions.

* Authentication flow and page redirection were tested successfully end-to-end.