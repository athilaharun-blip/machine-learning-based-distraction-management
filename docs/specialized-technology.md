# Part C: Specialized Technology – Machine Learning

## C1. Fundamental Concepts

### Overview

The proposed system uses **Supervised Machine Learning** to classify students' attention states based on study-context information. Supervised learning is a machine learning approach in which a model learns patterns from labelled training data and uses those patterns to predict the class of new data.

For this project, students will manually enter information about their completed study sessions. The trained model will classify each session into one of three attention states:

- **Focused:** The student experienced relatively few digital distractions during the study session.
- **Distracted:** The student experienced some digital distractions that may have affected concentration.
- **Highly Distracted:** The student experienced frequent digital distractions that may have significantly affected concentration.

These labels are proposed categories for the system, not medical diagnoses or direct measurements of attention.

### Input Features

The proposed machine learning model uses four study-context features:

| Feature | Description |
|---|---|
| Study Duration | Total duration of the study session in minutes |
| Notification Count | Number of notifications received during the session |
| Application-Switch Count | Number of times the student switched between applications |
| Activity Type | Type of study activity, such as reading, writing, or watching a video lecture |

### Machine Learning Workflow

The proposed workflow consists of two main phases.

**Training Phase**

1. Collect study-context data.
2. Assign attention-state labels to the collected data.
3. Prepare and extract the input features.
4. Split the labelled dataset into training and testing sets.
5. Train the supervised machine learning model.
6. Evaluate the trained model using the test dataset.

**Prediction Phase**

1. The student enters study-context information after completing a study session.
2. The system prepares the four input features.
3. The trained model predicts the attention state.
4. The system displays the predicted attention state.
5. The system provides a suitable context-aware suggestion if digital distraction is identified.

The training phase is used to develop and evaluate the model, while the prediction phase uses the trained model to classify new study sessions.

### Proposed Training Data

The training dataset will contain study-context information together with attention-state labels. One possible approach is to ask students to self-report their attention level after completing a study session. These labels will be used as the target values for supervised learning.

However, self-reported attention levels may be subjective. Therefore, the quality and consistency of the collected labels will need to be considered during model development.

### Worked Example

The following table shows **hypothetical data** to illustrate how the classification process may work.

| Duration (min) | Notifications | App Switches | Activity | Attention State |
|---|---|---|---|---|
| 45 | 1 | 0 | Reading | Focused |
| 30 | 5 | 4 | Video Lecture | Distracted |
| 20 | 10 | 8 | Writing | Highly Distracted |
| 50 | 0 | 1 | Reading | Focused |

For example, if a student enters a study duration of 35 minutes, 6 notifications, 5 application switches, and Video Lecture as the activity type, a trained model might classify the session as **Distracted**.

This is only an illustrative example. The actual prediction will depend on the collected dataset and the trained model.

### Model Evaluation

The dataset may be divided into training and testing sets using an 80:20 ratio. The training set will be used to train the model, while the test set will be used to evaluate its performance.

The following evaluation measures may be used:

- **Accuracy:** The proportion of correctly classified study sessions.
- **Precision:** How many predictions for a particular attention state are correct.
- **Recall:** How many actual instances of an attention state are correctly identified.
- **F1-score:** A measure that combines precision and recall.
- **Confusion Matrix:** A table showing correct and incorrect predictions for each attention state.

The proposed classification accuracy target is at least 70% on an independent test dataset. This is a project target and has not yet been achieved or evaluated.

## C2. Frameworks, Models, and Tools

Three supervised machine learning algorithms are considered for the proposed system.

| Algorithm | Description | Possible Use |
|---|---|---|
| Decision Tree | Classifies data using a sequence of decision rules. | Provides an interpretable model for understanding how study-context features influence predictions. |
| Random Forest | Combines predictions from multiple decision trees. | May improve classification performance and reduce overfitting compared with a single tree. |
| Logistic Regression | Uses statistical relationships between features and class probabilities. | Provides a baseline model for comparison with tree-based algorithms. |

These algorithms are suitable candidates because the proposed dataset contains structured input features and predefined attention-state labels.

The following tools may support development:

- **Python:** Programming language for data processing and machine learning development.
- **pandas:** Library for organising, cleaning, and preparing study-context datasets.
- **scikit-learn:** Machine learning library for training, testing, and evaluating classification models.

The algorithms will be compared using evaluation results before selecting the most suitable model. No algorithm is assumed to be the best before testing.

## C3. Suitability, Benefits, and Limitations

### Benefits

**1. Pattern Recognition**

Supervised machine learning can identify relationships between study-context features and attention-state labels. This may help the system recognise distraction patterns that are not easily represented by fixed rules.

**2. Personalised Context-Aware Support**

The predicted attention state can be used to provide suggestions that match the student's study situation. For example, a session classified as Highly Distracted may receive a suggestion to reduce unnecessary notifications during future study sessions.

**3. Adaptability**

The model may be retrained when more suitable labelled data becomes available. This allows the classification approach to be improved based on evaluation results.

### Limitations and Risks

**1. Data Quality**

The accuracy of the model depends on the quality and amount of labelled training data. A small or unbalanced dataset may affect classification performance.

**2. Subjective Attention Labels**

If attention states are labelled using student self-reports, different students may interpret their level of focus differently. This may introduce inconsistencies into the training dataset.

**3. Indirect Measurement**

Study duration, notifications, application switching, and activity type do not directly measure a student's actual attention. Therefore, the classification should be treated as an estimate based on study-context information.

**4. Manual Data Entry and Privacy**

The proposed system allows students to enter their own study-context information instead of automatically monitoring activities across other applications. This reduces the need for additional device permissions and limits intrusive data collection.

However, manually entered information may be inaccurate or incomplete, which could affect the classification results.

**5. Model Bias and Reliability**

If the training dataset does not represent different study habits and activity types, the model may perform less accurately for certain students or study situations.

### Comparison with Rule-Based Classification

A rule-based system is an alternative approach that classifies attention states using predefined conditions.

| Aspect | Supervised Machine Learning | Rule-Based System |
|---|---|---|
| Classification | Learns patterns from labelled data | Uses manually defined rules |
| Flexibility | Can adapt through retraining | Requires manual rule updates |
| Data Requirement | Requires labelled training data | Does not require model training |
| Interpretability | Depends on the selected algorithm | Usually easier to explain |
| Main Limitation | Sensitive to data quality and model performance | May not handle complex patterns effectively |

A rule-based system would be simpler to develop and test. However, supervised machine learning is selected because the project aims to investigate whether study-context features can be used to classify attention states through learned patterns.

The effectiveness of this approach will depend on the quality of the dataset and the model evaluation results.

Tabassi, E. (2023). *Artificial intelligence risk management framework (AI RMF 1.0)* (NIST AI 100-1). National Institute of Standards and Technology. https://doi.org/10.6028/NIST.AI.100-1
