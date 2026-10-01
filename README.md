# Breast Cancer Classification using Decision Tree

This project uses a **Decision Tree Classifier** to classify breast cancer tumors as **Benign (B)** or **Malignant (M)** using the Breast Cancer Wisconsin Diagnostic dataset.

## 📌 Project Overview

The goal of this project is to build a machine learning classification model that can predict whether a tumor is:

* **B — Benign**
* **M — Malignant**

The project also evaluates the model using training accuracy, testing accuracy, and a confusion matrix.

## 📊 Dataset

The dataset used in this project is the **Breast Cancer Wisconsin Diagnostic Dataset**.

* Total samples: **569**
* Features: **30**
* Target classes:

  * Benign (B)
  * Malignant (M)

The dataset files included in this repository are:

* `wdbc.data`
* `wdbc.names`

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib

## 🔄 Machine Learning Workflow

The project follows these main steps:

1. Load the dataset from GitHub
2. Add column names to the dataset
3. Separate features and target labels
4. Convert labels:

   * `B → 0`
   * `M → 1`
5. Split the dataset into training and testing sets
6. Train a Decision Tree Classifier
7. Set the maximum tree depth to **5**
8. Make predictions on the test data
9. Calculate training and testing accuracy
10. Generate a confusion matrix

## 🌳 Decision Tree Model

The Decision Tree model is configured with:

```python
DecisionTreeClassifier(max_depth=5, random_state=42)
```

The `max_depth=5` limits the maximum depth of the decision tree and helps control the complexity of the model.

## 📈 Model Results

After increasing the maximum depth to **5**, the model achieved:

| Dataset  |   Accuracy |
| -------- | ---------: |
| Training | **99.12%** |
| Testing  | **95.61%** |

### Training Accuracy

```text
0.9912087912087912
```

This means the model correctly classified approximately **99.12%** of the training samples.

### Testing Accuracy

```text
0.956140350877193
```

This means the model correctly classified approximately **95.61%** of the unseen testing samples.

## 🔍 Overfitting Analysis

The training accuracy is higher than the testing accuracy:

```text
Training Accuracy = 99.12%
Testing Accuracy  = 95.61%
```

The difference is approximately:

```text
99.12% - 95.61% = 3.51 percentage points
```

The model performs well on both training and testing data. The difference between the two scores indicates some generalization gap, but the testing accuracy remains high.

## 📉 Confusion Matrix

The confusion matrix is used to understand how many samples were correctly and incorrectly classified.

For this binary classification problem:

* **True Negative (TN):** Benign predicted as Benign
* **False Positive (FP):** Benign predicted as Malignant
* **False Negative (FN):** Malignant predicted as Benign
* **True Positive (TP):** Malignant predicted as Malignant

The confusion matrix provides more information than accuracy alone because it shows the types of classification errors made by the model.

## 📁 Project Structure

```text
Decision_Tree/
│
├── wdbc.data
├── wdbc.names
├── README.md
└── DecisionTree.py
```

## ▶️ How to Run

### 1. Clone the repository

```bash
git clone https://github.com/Eng-Waheedullah-wazir/Decision_Tree.git
```

### 2. Install required libraries

```bash
pip install pandas  scikit-learn matplotlib
```

### 3. Run the Python program

```bash
python DecisionTree.ipynb
```

## 🎯 Objective

The main objective of this project is to understand:

* Classification using Decision Trees
* Dataset preprocessing
* Training and testing data
* Model accuracy
* Maximum tree depth
* Overfitting and generalization
* Confusion matrix
* Binary classification

## 👨‍💻 Author

**Waheed Ullah**

Software Engineering Student
FAST NUCES Peshawar
