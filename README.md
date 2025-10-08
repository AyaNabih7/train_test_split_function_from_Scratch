# 🧮 Train-Test Split Function from Scratch

This repository contains a simple Python implementation of a **Train-Test Split** function — a fundamental step in preparing datasets for machine learning models.  
Instead of using `train_test_split` from scikit-learn, this project shows how to build it manually using only **NumPy** and **Pandas**.

---

## 📘 Project Overview

When training machine learning models, we need to divide our dataset into:
- **Training set** → Used to train the model.  
- **Testing set** → Used to evaluate model performance on unseen data.

This notebook demonstrates:
- How to shuffle dataset indices manually.
- How to split data into training and testing sets.
- How to use random seeds for reproducibility.

---

## 🧠 What You'll Learn

- The logic behind dataset splitting.
- How random sampling works in NumPy.
- How to handle reproducibility using `np.random.seed()`.
- How to manage Pandas DataFrames efficiently.

---

## 🧩 Function Overview

### Function Name:
```python
def my_own_train_test_split(df, train_ratio=0.8, test_ratio=0.2, seed=None)

| Parameter     | Type        | Description                                     |
| ------------- | ----------- | ----------------------------------------------- |
| `df`          | DataFrame   | The dataset to be split                         |
| `train_ratio` | float       | Proportion of data for training (default = 0.8) |
| `test_ratio`  | float       | Proportion of data for testing (default = 0.2)  |
| `seed`        | int or None | Random seed to ensure reproducibility           |
```
Returns:
```
train_df, test_df
```
Two DataFrames — one for training, and one for testing.
###🧾 Example Usage
```python
import pandas as pd
import numpy as np
from my_train_test_split import my_own_train_test_split

# Create sample data
data = {
    'Student_ID': [1, 2, 3, 4, 5],
    'Score': [90, 85, 78, 92, 88]
}
df = pd.DataFrame(data)

# Apply the custom split function
train_df, test_df = my_own_train_test_split(df, train_ratio=0.8, test_ratio=0.2, seed=42)

print("Training Set:\n", train_df)
print("\nTesting Set:\n", test_df)
```
### 🛠️ Requirements

- Python ≥ 3.7
- NumPy
- Pandas

Install dependencies using:
```python
pip install numpy pandas
```
### 🧑‍💻 Author

Aya Nabih
📊 Data Scientist & University Lecturer.
🎓 Specializing in Machine Learning, NLP, and Educational Content Development.
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/aya-fouad-nabih)


### ⭐ Acknowledgments

This project is part of a practical exercise to understand core machine learning concepts by building functions from scratch without relying on external ML libraries.
