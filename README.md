**Teach For America Admissions Prediction — Machine Learning Project**

This project builds a predictive model to identify whether Teach For America applicants complete the admissions process. Using a large dataset with severe class imbalance, the project explores multiple supervised learning approaches, advanced feature engineering, and model tuning strategies to improve minority-class detection.

**Dataset Overview**

74,839 records, 39 variables

Target: Completed Admissions Process (0/1)

80/20 class imbalance, requiring careful evaluation beyond accuracy

Rich mix of demographic, behavioral, and essay-based attributes

 **Feature Engineering**

Created 10+ engineered features to strengthen predictive signal, including:

Time-based metrics (sign-up → start, start → submit, submit → deadline)

Essay metrics (length, unique words, sentiment, density)

Region preference indicators

Deadline behavior + event attendance
These features captured motivation, engagement, and applicant follow-through patterns.

**Models Implemented**

Five supervised learning models were trained and compared:

Model	Key Insight
kNN	Accuracy: 75.8%, Sensitivity: 0.901, Specificity: 0.159
Naive Bayes	~0.807 accuracy but ~0 specificity
Decision Tree (C5.0)	Same issue: predicts almost all positives
SVM (Radial)	~0.807 accuracy, ~0 specificity
ANN (Tuned)	Best minority-class detection
** Best Model — Tuned Artificial Neural Network**

A tuned ANN (maxit=500, 10-fold CV, architecture [7,15,2], decay grid) delivered the strongest balanced performance:

Accuracy: 0.8072

Kappa: 0.0510

Sensitivity: 0.9908

Specificity: 0.0436

The ANN significantly outperformed all other models in detecting non-completers, the minority class.
