# Part C: Specialized Technology – Machine Learning

## C1. Fundamental Concepts of Machine Learning

### What is Machine Learning?

Machine Learning (ML) is a specialized technology that allows a computer system to learn patterns from data and use those patterns to make predictions or classifications. Instead of manually writing a rule for every possible situation, an ML model learns from examples provided during training.

For this project, **supervised machine learning** is suitable because the system needs to classify a student's attention state into predefined categories. For example, the attention states can be labelled as **Focused, Distracted, or Highly Distracted**. The model can learn the relationship between study-context features and these attention-state labels.

### Key Concepts

**1. Features**

Features are the input information used by the machine learning model. For this project, possible features may include study duration, number of notifications, frequency of switching between applications, and type of activity being performed.

**2. Labels**

A label is the expected output that the model learns to predict. In this project, the label represents the student's attention state, such as Focused, Distracted, or Highly Distracted.

**3. Training Data**

Training data contains examples of features together with their known attention-state labels. The ML model uses these examples to learn patterns.

**4. Classification**

Classification is a machine learning task where the model assigns an input to one of several predefined categories. Scikit-learn describes classification as identifying which category an object belongs to and provides several classification algorithms.

**5. Model Evaluation**

After training, the model needs to be tested using data that was not used for training. This helps determine whether the model can make correct predictions on unseen data. Scikit-learn provides train/test splitting, cross-validation, and classification metrics for model evaluation.

### Basic ML Process

The basic process for the proposed project can be represented as:

```text
Student Study Activity
        ↓
Collect Study Context
        ↓
Extract Features
        ↓
Training Data
        ↓
Train ML Classification Model
        ↓
Test / Evaluate Model
        ↓
New Student Context
        ↓
Predict Attention State
        ↓
Focused / Distracted / Highly Distracted
        ↓
Context-Aware Support
```

### Simple Worked Example

For example, a training dataset could contain:

| Study Duration | Notifications | App Switching | Attention State |
|---|---:|---:|---|
| 45 minutes | 1 | 0 | Focused |
| 30 minutes | 5 | 4 | Distracted |
| 20 minutes | 10 | 8 | Highly Distracted |
| 50 minutes | 0 | 1 | Focused |

The model learns patterns from these examples. If a new student has a high number of notifications and frequently switches between applications, the model may classify the student's attention state as **Distracted**.

The predicted state can then be displayed to the student and used to provide suitable digital distraction management support.

---

## C2. Machine Learning Models and Tools

### 1. Decision Tree

A Decision Tree is a supervised learning method that can be used for classification. It makes decisions using a sequence of rules based on input features. For example, a tree could first check whether the number of notifications is high, followed by checking application switching frequency.

Decision trees are relatively easy to understand because their decision rules can be visualized. They also require relatively little data preparation compared with some other techniques.

**Use in this project:**  
A Decision Tree can be used to classify a student's attention state based on study-context features.

---

### 2. Random Forest

Random Forest is an ensemble classification method that combines multiple decision trees. The predictions from the trees are combined to produce the final classification. Scikit-learn describes Random Forest as using multiple decision trees and averaging their predictions to improve predictive accuracy and help control overfitting.

**Use in this project:**  
Random Forest can be used to classify attention states when several study-context features are considered together.

---

### 3. Logistic Regression

Logistic Regression is a classification algorithm that can be used to predict class membership based on input features. Scikit-learn provides `LogisticRegression` as a classifier and supports binary as well as multiclass classification in appropriate configurations.

**Use in this project:**  
Logistic Regression can be used as a simpler classification model and can provide a baseline for comparing its performance with Decision Tree and Random Forest.

---

### C3. Fit of Machine Learning to the Problem

Machine Learning is suitable for this project because the main problem involves identifying a student's attention state from patterns in study-context information. The system does not need to rely only on fixed rules. Instead, a supervised ML model can learn from labelled examples and classify new study-context data into predefined attention states.

The proposed approach can therefore connect directly with the requirements:

```text
FR1: Collect Study Context
             ↓
FR2: Classify Attention State
             ↓
FR3: Display Attention State
             ↓
FR4: Identify Digital Distraction Situation
             ↓
FR5: Provide Context-Aware Support
```

### Benefits

**1. Pattern-based classification**

ML can learn patterns from multiple features instead of relying on one fixed condition. This is useful because digital distraction may occur differently between students and situations.

**2. Multiple models can be compared**

Decision Tree, Random Forest, and Logistic Regression can be trained and evaluated using the same dataset. This allows the project to compare their classification performance before selecting a suitable model.

**3. Can support context-aware decisions**

The classification result can be combined with the student's current context to provide more suitable digital distraction management support.

### Limitations and Risks

**1. Data quality and availability**

Machine learning depends on suitable training data. If the dataset is too small, inaccurate, or does not represent different student situations, the model may not perform well on new data. Model performance therefore needs to be evaluated using appropriate testing and validation methods.

**2. Bias and fairness**

If the training data does not represent different types of students and study situations, the model may perform better for some situations than others. NIST identifies fairness and harmful-bias management as important characteristics of trustworthy AI systems.

**3. Privacy concerns**

Student context may involve information about digital-device usage. Collecting unnecessary personal information could create privacy risks. Therefore, the project should follow the privacy limitation already stated in NFR3 and only collect information that is necessary for the intended classification.

### Comparison with an Alternative Approach

An alternative approach is a **rule-based system**. Instead of learning from data, a rule-based system would use manually defined conditions.

For example:

```text
IF notifications > 5
AND app switching > 5
THEN attention state = Distracted
```

A rule-based approach is simpler and easier to understand, but it requires the developer to manually define the rules. It may also become difficult to maintain when there are many combinations of study contexts.

Machine Learning is therefore selected for this project because the main objective is to **classify attention states from patterns in study-context data**. ML provides a way to learn these patterns from labelled examples rather than relying entirely on manually created rules.

However, the ML model should still be evaluated carefully because good training performance does not automatically mean that the model will perform well on unseen data.