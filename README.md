Sonar Sensor Performance Analysis for Underwater Mine Detection
📌 Project Overview

The research investigates which sonar frequency-band characteristics enable the identification of underwater mines (M) from rocks (R). The complete data science lifecycle runs from data acquisition through preprocessing and exploratory data analysis and machine learning modeling and evaluation and interpretation. The research assesses classification accuracy to identify which factors between sonar sensor measurement uncertainty and model defects cause the remaining detection errors.

🎯 Objectives

The research evaluates sonar frequency-band data effectiveness for distinguishing between mines and rocks.

The goal of this work involves evaluating how linear and nonlinear machine learning approaches perform when used for mine detection tasks.

The research investigates how prediction confidence levels affect the accuracy of detection systems.

The evaluation process determines which features have the most impact while it also measures the degree of sensor measurement uncertainty.

🧪 Research Hypotheses

H1 – Feature Dominance Hypothesis:
A small subset of sonar frequency bands contributes most of the discriminative power.

H2 – Intrinsic Sensor Ambiguity Hypothesis:
The main reason for detection errors stems from the way sonar signatures overlap instead of being caused by any lack of model performance.

📂 Dataset

Source: UCI Machine Learning Repository – Sonar Mines vs Rocks

Samples: 208

Features: 60 frequency-band energy values

Classes: Mine (M), Rock (R)

Missing Values: None

The dataset contains equal distribution of data which makes it suitable for supervised classification tasks.

🛠 Tools & Technologies

Programming Language: Python

The following libraries serve as fundamental resources for this project: NumPy, Pandas, Matplotlib and scikit-learn.

The analysis used three different models which included Logistic Regression and Support Vector Machine (RBF) and Random Forest.

🔁 Methodology (Data Science Lifecycle)
1️⃣ Data Acquisition

The dataset receives its data from a compressed ZIP file which enables reproducibility while avoiding human involvement in file management.

2️⃣ Data Preprocessing

Feature standardization using StandardScaler

The research uses stratified train–test split to maintain equal representation of all classes throughout the evaluation process.

3️⃣ Exploratory Data Analysis

Class distribution visualization

PCA visualization to assess intrinsic separability

Mean frequency-band energy comparison between mines and rocks

4️⃣ Model Development

Logistic Regression as a linear baseline

SVM (RBF kernel) as the primary nonlinear classifier

Random Forest for comparison and feature interpretation

5️⃣ Model Validation

The evaluation of model performance stability uses repeated stratified cross-validation to assess different models.

6️⃣ Final Evaluation

Performance is evaluated on unseen test data using:

Accuracy

Precision, Recall, F1-score

Confusion matrix

ROC curve and ROC-AUC

7️⃣ Interpretation & Analysis

Prediction confidence distribution

Multiple Random Forest runs were used to perform stability assessment of their features.

SVM decision boundary visualization in PCA space (interpretive only)

📊 Key Results

Best Model: Support Vector Machine (RBF)

Test Accuracy: ~85–86%

ROC–AUC: ~0.92

Observation: High mine detection recall with some false alarms

The remaining errors stem from the built-in ambiguous nature of sonar sensor data.

#▶ How to Run the Code
1️⃣ Install Dependencies
pip install numpy pandas matplotlib scikit-learn

2️⃣ Set Dataset Path

Update the dataset path in the code:

ZIP_PATH = "path_to/connectionist+bench+sonar+mines+vs+rocks.zip"

3️⃣ Run the Script
python sonar_project_final_documented.py
