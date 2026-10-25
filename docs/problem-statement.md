# Part A: Problem Formulation

## A1. Problem Statement

University students who study on laptops, tablets, and smartphones are often distracted by social media, messaging, entertainment, and notifications. In a cross-sectional study, Thapa et al. (2025) found that 51.2% of surveyed students used digital devices for non-classroom activities one to three times during a class, while 68.6% identified reduced attention as a main negative effect. These distractions can interrupt students' concentration, making study sessions less effective and potentially increasing the time needed to complete tasks. Students may also find it difficult to recognise when their attention is decreasing during study sessions, making it harder to manage distractions at the right time. Although the study focuses on classroom settings, similar digital distractions may also occur during independent study sessions, which are the focus of this project.

## A2. Users, Stakeholders, and Project Scope

### Target Users

The main target users of the proposed system are university students who use digital devices during independent study sessions. These students may experience distractions from notifications, social media, and switching between applications.

### Stakeholders

- **University students:** The main users who enter study-context information, view their classified attention states, and receive distraction-management suggestions.
- **Lecturers:** May benefit from understanding how the proposed system supports students in managing digital distractions.
- **Project supervisor:** Provides guidance and evaluates the development and research outcomes of the project.

### In Scope

The proposed system will:

1. Allow students to manually enter study-context information, including study duration, notification count, application-switch count, and activity type.
2. Use a trained supervised machine learning model to classify study sessions as Focused, Distracted, or Highly Distracted.
3. Display the classified attention state to students after they submit their study-context information.
4. Identify study sessions classified as Distracted or Highly Distracted.
5. Provide context-aware suggestions based on the classified attention state.

### Out of Scope

The proposed system will not:

1. Diagnose or treat screen addiction or other medical conditions.
2. Automatically monitor notifications, applications, or private communications across a student's device.
3. Guarantee that students will remain focused or completely avoid digital distractions.
4. Evaluate or grade students' academic performance.

## Reference

Thapa, P. P., Sharma, P., Goundar, S., Tsirkas, P., Valamontes, A., & Adamopoulos, I. P. (2025). Health education and digital distractions in the classroom among students: A cross-sectional study. *European Journal of Health and Biology Education, 12*(1), e2507. https://doi.org/10.29333/ejhbe/16752
