# Machine Learning-Based Attention State Classification for Context-Aware Digital Distraction Management

## Project Overview

This project aims to support university students in managing digital distractions during independent study sessions.

The proposed system uses supervised machine learning to classify students' attention states based on study-context information. Students will manually enter their study duration, notification count, application-switch count, and activity type after completing a study session.

Based on this information, the trained machine learning model will classify the study session into one of three attention states:

- **Focused**
- **Distracted**
- **Highly Distracted**

The system will then display the classified attention state and provide suitable distraction-management suggestions when distractions are identified.

The purpose of this project is to support students in understanding their study habits and managing digital distractions, rather than diagnosing or treating screen addiction.

## Problem Statement

University students may experience digital distractions from social media, messaging, entertainment, and notifications while using digital devices for studying. These distractions can interrupt their concentration and affect the effectiveness of their study sessions.

Students may also find it difficult to recognise when their attention has decreased during a study session. This creates a need for a system that can estimate attention states based on study-context information and provide suitable support for managing digital distractions.

## Project Objectives

1. To identify relevant study-context features for classifying university students' attention states during study sessions.
2. To develop a supervised machine learning model that classifies study sessions into Focused, Distracted, or Highly Distracted attention states.
3. To develop a context-aware web application that displays the classified attention state and provides suitable distraction-management suggestions.

## Proposed Technology

- **Specialized Technology:** Supervised Machine Learning
- **Candidate Algorithms:** Decision Tree, Random Forest, and Logistic Regression
- **Programming Language:** Python
- **Libraries:** pandas and scikit-learn
- **Application Type:** Web Application

The machine learning algorithms will be compared during model development to determine the most suitable approach based on classification performance.

## Documents

- [Problem Statement](docs/problem-statement.md)
- [Requirements](docs/requirements.md)
- [User Stories](docs/user-stories.md)
- [Specialized Technology](docs/specialized-technology.md)
- [Sprint Log](docs/sprint-log.md)

## Project Structure

```text
.
|-- README.md
|-- LICENSE
|-- .gitignore
|-- docs/
|   |-- problem-statement.md
|   |-- requirements.md
|   |-- user-stories.md
|   |-- specialized-technology.md
|   |-- sprint-log.md
|-- src/
    |-- README.md
```

*The src/ folder is reserved for future implementation.*

## Roadmap

- [x] Define project problem statement and scope
- [x] Identify functional and non-functional requirements
- [x] Write user stories and acceptance criteria
- [x] Select and explain specialized technology
- [x] Document proposed machine learning workflow
- [ ] Collect and prepare study-context dataset
- [ ] Train and evaluate machine learning models
- [ ] Develop web application prototype
- [ ] Integrate attention-state classification and context-aware suggestions
- [ ] Test and evaluate the proposed system

## Current Status

**CSC649 Assignment 1 – Documentation Stage**

The initial project documentation has been prepared, including the problem statement, requirements, user stories, and proposed specialized technology.

The machine learning model and web application have not yet been implemented.

## Author

Hani Nur Athilah Binti Harun Nurashid
