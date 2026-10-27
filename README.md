# Phishing Website Detection Using SVM

## 📌 Project Overview

This project implements a Machine Learning-based Phishing Website Detection System using a Linear Support Vector Machine (SVM) classifier.

The model uses the **PhiUSIIL Phishing URL Dataset** to classify websites as phishing or legitimate based on numerical website-related features. The project also evaluates the model's performance using standard classification metrics and visualizations.

## 🎯 Objectives

The main objectives of this project are to:

- Detect phishing websites using Machine Learning.
- Explore and preprocess the phishing website dataset.
- Select relevant numerical features for model training.
- Build and train a Linear SVM classification model.
- Evaluate model performance using standard classification metrics.
- Visualize classification results using a Confusion Matrix and ROC Curve.

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## 📂 Dataset

**Dataset Name:** PhiUSIIL Phishing URL Dataset

The dataset contains website-related features and labels used to identify phishing and legitimate websites.

The numerical features are used as input variables, while the `label` column serves as the target variable.

## 🧹 Data Preprocessing

The following preprocessing steps are performed:

- Load the dataset from a CSV file.
- Remove records with missing target labels.
- Remove irrelevant and non-numeric columns, including `URL`, `Domain`, `TLD`, and `Title`.
- Convert the original labels into binary target values.
- Select numerical features for model training.
- Replace infinite values with missing values.
- Handle missing numerical values using median imputation.

## 🤖 Machine Learning Model

**Algorithm:** Linear Support Vector Machine (LinearSVC)

Linear SVM is a supervised Machine Learning algorithm that identifies a decision boundary to classify websites into two categories: phishing and legitimate.

### Pipeline Components

1. **StandardScaler:** Standardizes numerical features before model training.
2. **LinearSVC:** Trains the classification model to distinguish between the two classes.

### Model Parameters

```python
LinearSVC(
    C=1.0,
    class_weight="balanced",
    random_state=42,
    max_iter=5000
)
```

### Dataset Splitting

The dataset is divided into two subsets:

- **Training Set:** 80%
- **Testing Set:** 20%

The training set is used to train the model, while the testing set is used to evaluate its performance.

## 📊 Evaluation Metrics

The model's performance is evaluated using the following metrics:

- **Confusion Matrix:** Summarizes correct and incorrect predictions for each class.
- **Precision:** Measures the proportion of positive predictions that are correct.
- **Recall:** Measures the proportion of actual positive cases correctly identified.
- **F1-Score:** Represents the harmonic mean of precision and recall.
- **ROC-AUC Score:** Measures the model's ability to distinguish between the two classes.
- **Classification Report:** Provides precision, recall, F1-score, and support for each class.

## 📈 Visualizations

### Confusion Matrix

The Confusion Matrix visualizes the number of correctly and incorrectly classified phishing and legitimate websites.

### ROC Curve

The ROC Curve illustrates the model's ability to distinguish between phishing and legitimate websites across different classification thresholds.

## 📁 Project Structure

```text
├── ML task 9.py
├── PhiUSIIL_Phishing_URL_Dataset.csv
└── README.md
```

## ▶️ How to Run the Project

### 1. Install Dependencies

Install the required Python libraries using the following command:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### 2. Update the Dataset Path

Ensure that the dataset is available in the project directory and update the file path if necessary:

```python
df = pd.read_csv("PhiUSIIL_Phishing_URL_Dataset.csv")
```

### 3. Execute the Python Script

Run the Python script using the following command:

```bash
python "ML task 9.py"
```

## ✅ Expected Output

After executing the program, the following outputs are generated:

- Dataset summary and shape.
- Dataset column information and class distribution.
- Trained Linear SVM classification model.
- Confusion Matrix visualization.
- Precision, Recall, F1-Score, and ROC-AUC values.
- Classification Report.
- ROC Curve visualization.

## 🎓 Learning Outcomes

Through this project, you will learn how to:

- Perform data preprocessing and handle missing values.
- Select numerical features for Machine Learning.
- Build and train a classification model using Linear SVM.
- Evaluate model performance using classification metrics.
- Visualize classification results using Matplotlib and Scikit-learn.
- Apply Machine Learning techniques to phishing website detection.

## 📝 Conclusion

This project demonstrates the application of Linear SVM for phishing website detection using the PhiUSIIL Phishing URL Dataset. By preprocessing website-related features, training a classification model, and evaluating its performance, the project provides a practical introduction to using Machine Learning for website security.

The evaluation metrics and visualizations help assess how effectively the model distinguishes between phishing and legitimate websites.
