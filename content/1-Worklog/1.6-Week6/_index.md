---
title: "Week 6 Worklog"
date: 2026-05-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---
### Week 6 Objectives:

* Initialize the React frontend project boilerplate for SyncQuiz.
* Configure the routing system and state management for the application.
* Create reusable UI components to support future feature development.
* Standardize the project structure for scalability and maintainability.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2   | - Research React project setup best practices <br> - Initialize React frontend project using Create React App or Vite <br> - Configure ESLint, Prettier, and project-level coding standards | 05/25/2026 | 05/25/2026 | <https://vitejs.dev/guide/> |
| 3   | - **Practice:** Configure routing system <br>&emsp; + Install and set up React Router v6 <br>&emsp; + Define route structure: Home, Login, Signup, Dashboard, Quiz Management, Game Room <br>&emsp; + Implement protected routes for authenticated users <br>&emsp; + Set up navigation guards based on authentication state | 05/26/2026 | 05/26/2026 | <https://reactrouter.com/en/main> |
| 4   | - **Practice:** Set up state management <br>&emsp; + Evaluate and select state management approach (Redux Toolkit / Zustand / Context API) <br>&emsp; + Implement global auth state: current user, token, login status <br>&emsp; + Implement UI state: loading indicators, modal visibility, error messages <br>&emsp; + Write unit tests for state reducers or context providers | 05/27/2026 | 05/27/2026 | <https://redux-toolkit.js.org/> |
| 5   | - **Practice:** Build reusable base components <br>&emsp; + Create Header component with navigation links and user info <br>&emsp; + Create Footer component <br>&emsp; + Create Layout wrapper component for consistent page structure <br>&emsp; + Create Loading spinner and error boundary components <br>&emsp; + Apply basic CSS/Tailwind styling for consistency | 05/28/2026 | 05/28/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - Standardize folder structure: components/, pages/, hooks/, store/, services/, utils/ <br> - Verify the project runs correctly in local development environment <br> - Set up environment variables (.env) for API endpoints and configuration <br> - Document the project structure and component usage guidelines | 05/29/2026 | 05/29/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Week 6 Achievements:

* Successfully initialized the React frontend project with Vite, ESLint, and Prettier configuration.

* Configured React Router v6 with a complete route structure, including protected routes for authenticated pages.

* Implemented global state management for authentication and UI states using the selected approach.

* Built reusable base components: Header, Footer, Layout, Loading, and Error Boundary.

* Established a standardized folder structure to support scalable development in the following weeks.

* The project runs correctly in the local development environment with environment variable configuration in place.