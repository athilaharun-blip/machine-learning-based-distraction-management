# Part B: Requirements and User Stories

# System Requirements

## 1. Functional Requirements

**FR1 – Record Study Context**

The system shall allow students to enter their study duration, number of notifications, number of application switches, and activity type for each study session.

**FR2 – Classify Attention State**

The system shall classify each study session as Focused, Distracted, or Highly Distracted using a trained machine learning model.

**FR3 – Display Attention State**

The system shall display the classified attention state to the student on the study-session screen.

**FR4 – Identify Digital Distraction**

The system shall flag a session as a digital distraction situation when the classified state is Distracted or Highly Distracted.

**FR5 – Provide Context-Aware Support**

The system shall display a distraction-management suggestion that matches the classified attention state when a digital distraction situation is flagged.

## 2. Non-Functional Requirements

**NFR1 – Performance**

The system shall display the classification result within 3 seconds after the context data has been processed.

**NFR2 – Usability**

The system shall let a student view their current attention state within 2 user interactions from the main study-session screen.

**NFR3 – Privacy**

The system shall store only the four study-context fields specified in FR1 and shall not collect or store passwords, private messages, or personal communication content.

**NFR4 – Classification Accuracy**

The classification model shall achieve at least 70% accuracy on an independent test dataset that was not used during training.

*Note: The 70% accuracy is a proposed performance target and has not yet been evaluated.*
