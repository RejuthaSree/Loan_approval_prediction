Ah, you mean the **README.md for your GitHub repository**, not notebook Markdown. Use this:

# Loan Approval Prediction Using Decision Tree

## 📌 Project Overview

This project predicts whether a loan application will be **approved or rejected** using a **Decision Tree Classifier**.

The model is trained on applicant and loan-related information such as income, education, credit history, employment status, and property area.

## 🎯 Objective

The main objective of this project is to build a machine learning classification model that can predict loan approval status based on the applicant's information.

* `Y` → Loan Approved
* `N` → Loan Rejected

## 📂 Dataset

The project uses three datasets:

* **Train Dataset** – Contains the input features and the target variable `Loan_Status`.
* **Test Dataset** – Contains unseen data used to generate predictions.
* **Sample Submission** – Provides the required format for the final predictions.

### Dataset Size

| Dataset       | Rows | Columns |
| ------------- | ---: | ------: |
| Training Data |  614 |      13 |
| Test Data     |  367 |      12 |

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* Jupyter Notebook / Google Colab

## 🔍 Features

The dataset contains features such as:

* Gender
* Married
* Dependents
* Education
* Self Employment
* Applicant Income
* Coapplicant Income
* Loan Amount
* Loan Amount Term
* Credit History
* Property Area

`Loan_ID` was excluded from model training because it is an identifier rather than a meaningful predictive feature.

## ⚙️ Data Preprocessing

The following preprocessing steps were performed:

1. Loaded the training and test datasets.
2. Checked the dataset structure and missing values.
3. Handled missing numerical values using the median.
4. Handled missing categorical values using the mode.
5. Removed the `Loan_ID` column from the model features.
6. Converted categorical variables into numerical form using one-hot encoding.
7. Converted the target variable:

   * `Y` → `1`
   * `N` → `0`

## 🌳 Model

A **Decision Tree Classifier** was used for loan approval prediction.

Different values of `max_depth` were tested to find the best-performing model.

### Hyperparameter Results

| Max Depth | Validation Accuracy |
| --------: | ------------------: |
|         2 |          **85.37%** |
|         3 |              84.55% |
|         4 |              84.55% |
|         5 |              82.93% |
|         6 |              82.93% |
|         7 |              78.86% |
|         8 |              79.67% |
|        10 |              77.24% |

The best result was obtained with:

```text
max_depth = 2
```

## 📊 Model Performance

The final validation accuracy was approximately:

**85.37%**

Classification report:

| Class    | Precision | Recall | F1-Score |
| -------- | --------: | -----: | -------: |
| Rejected |      0.95 |   0.55 |     0.70 |
| Approved |      0.83 |   0.99 |     0.90 |

The model performs particularly well at identifying approved loans. However, the recall for rejected loans is comparatively lower.

## 📁 Project Structure

```text
Loan-Approval-Decision-Tree/
│
├── train.csv
├── test.csv
├── Sample_Submission.csv
├── submission.csv
├── loan_approval_decision_tree.ipynb
└── README.md
```

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone <your-repository-url>
```

### 2. Install the required libraries

```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```

### 3. Open the notebook

```bash
jupyter notebook
```

Open:

```text
loan_approval_prediction.ipynb
```

### 4. Run the notebook

Run the cells sequentially to:

* Load the dataset
* Preprocess the data
* Train the Decision Tree
* Evaluate the model
* Generate test predictions
* Create `submission.csv`

## 📤 Output

The final predictions are saved in:

```text
submission.csv
```

The file contains:

```text
Loan_ID,Loan_Status
```

## 🔮 Future Improvements

The model could potentially be improved by:

* Feature engineering
* Class balancing
* Cross-validation
* Grid Search for hyperparameter tuning
* Random Forest
* Gradient Boosting
* XGBoost
* Comparing multiple classification algorithms

## 👩‍💻 Author

**Rejutha sree M**

---

⭐ If you found this project useful, consider giving the repository a star!
