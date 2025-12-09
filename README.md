# Imbalanced-Medical-Classification-with-Multilayer-Perceptrons-Predicting-Type-2-Diabetes
Type 2 diabetes is a chronic metabolic disease that affects hundreds of millions of people worldwide. Early detection is crucial, because lifestyle changes and treatment can significantly reduce the risk of complications. However, screening large populations is expensive and time-consuming. 
Type 2 Diabetes Prediction using Multilayer Perceptrons (MLP)
Overview

This project focuses on predicting Type 2 diabetes using a dataset of anonymized patient records. The model leverages Multilayer Perceptrons (MLPs) to perform classification and tackles the challenges of imbalanced medical classification. The dataset contains various clinical and lifestyle features that are used to predict whether a person has diabetes. Special attention is given to addressing class imbalance and evaluating the model performance using appropriate metrics.

Dataset

The dataset diabetes_prediction_dataset.csv consists of anonymized patient-level records with the following features:

Demographic Variables:

Gender (Male, Female, Other)

Age (in years)

Clinical History:

Hypertension (0/1)

Heart Disease (0/1)

Lifestyle:

Smoking History (never, current, former, etc.)

Biomarkers:

BMI (Body Mass Index)

HbA1c Level (long-term blood sugar marker)

Blood Glucose Level (short-term blood sugar)

Target Variable:

Diabetes (0 = No diabetes, 1 = Diabetes)

The dataset is imbalanced, with a majority of non-diabetic records, which presents a challenge in model training.

Key Concepts

Multilayer Perceptrons (MLPs): A type of neural network architecture used for supervised classification tasks.

Imbalanced Classification: In this project, the dataset is highly imbalanced, with many more non-diabetic patients than diabetic ones, making it essential to handle class imbalance carefully.

Class Weighting: To address the class imbalance, class weighting is used to penalize the misclassification of the diabetic class more heavily.

Threshold Tuning: The model’s decision threshold is adjusted to balance false positives and false negatives, a crucial aspect of medical predictions.

Methodology

The following steps were taken to build and evaluate the model:

Preprocessing:

Categorical variables (e.g., gender, smoking history) were one-hot encoded.

Numeric variables (e.g., age, BMI, HbA1c level) were standardized.

The data was split into training (80%) and testing (20%) sets.

Modeling:

Baseline MLP: A basic MLP without class weighting was trained.

Weighted MLP: A second MLP was trained with class_weight='balanced' to give more importance to the minority class (diabetic patients).

Model Evaluation:

Performance metrics such as accuracy, precision, recall, F1-score, ROC AUC, and average precision were used.

Decision threshold analysis was performed to understand trade-offs between precision and recall.

Learning Curve:

A learning curve was plotted to assess how increasing the amount of training data affects the model’s performance.

Results

Baseline Model: High accuracy, but low recall for the positive (diabetic) class.

Weighted Model: Improved recall and F1-score for the positive class, but with a slight drop in overall accuracy.

Visualizations:

Confusion Matrices: To show how well the models distinguish between diabetic and non-diabetic patients.

ROC Curve: To evaluate the model's discriminative ability.

Precision-Recall Curve: To evaluate the model's performance on imbalanced data.

Ethical Considerations

Bias and Fairness: The dataset may not represent all populations equally, which could lead to biased predictions for underrepresented groups.

Clinical Impact: Misclassifications (false negatives and false positives) have significant consequences in medical decision-making.

AI in Healthcare: AI models should be used as decision-support tools, not as replacements for human professionals. Transparency and human oversight are essential.
