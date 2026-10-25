# B3. User Stories

## User Stories and Acceptance Criteria

## US1 – Enter Study Context

**User Story:**

As a university student, I want to enter my study-context information after a study session, so that the system can use it to classify my attention state.

**Linked Requirements:** FR1, FR2, NFR3

**Acceptance Criteria:**

- **AC1:** The student can enter study duration, notification count, application-switch count, and activity type for a study session.
- **AC2:** After submission, the recorded values are passed to the machine learning model for attention-state classification.
- **AC3:** The system does not collect or store passwords, private messages, or personal communication content.

## US2 – View Classified Attention State

**User Story:**

As a university student, I want to view the classified attention state of my submitted study session, so that I can understand my level of focus during that session.

**Linked Requirements:** FR2, FR3, NFR1, NFR2

**Acceptance Criteria:**

- **AC1:** The system displays one of three attention states: Focused, Distracted, or Highly Distracted.
- **AC2:** The student can view the classification result within 2 user interactions from the main study-session screen.
- **AC3:** The classification result is displayed within 3 seconds after the submitted context data has been processed.

## US3 – Receive Context-Aware Support

**User Story:**

As a university student, I want to receive a suitable suggestion when digital distraction is identified, so that I can manage distractions during future study sessions.

**Linked Requirements:** FR4, FR5

**Acceptance Criteria:**

- **AC1:** The system flags a study session when its classified attention state is Distracted or Highly Distracted.
- **AC2:** The system displays a distraction-management suggestion that matches the classified attention state.
- **AC3:** The suggestion focuses on managing digital distractions and does not claim to diagnose or treat screen addiction.
