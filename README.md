
# Heart Disease Classification using Random Forest and Gradient Boosting

## Overview
This project aims to classify heart disease patients using the UCI Heart Disease Dataset. Two machine learning models, **Random Forest** and **Gradient Boosting**, were implemented to evaluate the performance on the dataset.

SMOTE (Synthetic Minority Oversampling Technique) was applied to address class imbalance, ensuring that all target classes had equal representation in the training data.

---

## Dataset
- **Source**: UCI Heart Disease Dataset
- **Target Variable**: `num` (Indicates the presence of heart disease, with values ranging from 0 to 4)
- **Features**:
  - Numeric Columns: `['id', 'age', 'trestbps', 'chol', 'thalch', 'oldpeak', 'ca']`
  - Categorical Columns: `['sex', 'dataset', 'cp', 'fbs', 'restecg', 'exang', 'slope', 'thal']`

---

## Preprocessing
1. **Handling Missing Values**:
   - Numeric columns: Imputed missing values with the median.
   - Categorical columns: Imputed missing values with the most frequent category.

2. **Feature Scaling and Encoding**:
   - Numeric features were standardized using `StandardScaler`.
   - Categorical features were one-hot encoded.

3. **Class Imbalance**:
   - Applied SMOTE to balance the dataset, ensuring each target class had equal representation.

---

## Models and Results

### 1. Random Forest
- **Accuracy**: **85.89%**
- **Confusion Matrix**:
  ![Random Forest Confusion Matrix](random_forest_confusion_matrix.png)
- **Classification Report**:
  - Precision, Recall, and F1-score were strong across all classes, with particularly high performance for Class `3` and Class `4`.

### 2. Gradient Boosting
- **Accuracy**: **76.16%**
- **Confusion Matrix**:
  ![Gradient Boosting Confusion Matrix](gradient_boosting_confusion_matrix.png)
- **Classification Report**:
  - Gradient Boosting performed reasonably well but was outperformed by Random Forest in overall accuracy and metrics for minority classes.

---

## Observations
1. **Random Forest**:
   - Performed the best with an overall accuracy of **85.89%**.
   - Strong performance across all classes, even for previously underrepresented classes like `2` and `4`.

2. **Gradient Boosting**:
   - Accuracy of **76.16%**, showing slightly lower performance compared to Random Forest.
   - Struggled with precise classification for some classes.

3. **SMOTE**:
   - Balancing the dataset improved the performance of both models significantly, especially for minority classes.

---

## Conclusion
- **Random Forest** is the recommended model for deployment due to its superior performance and balanced classification across all target classes.
- The project demonstrates the importance of handling class imbalance and evaluating multiple models to determine the best solution.

---

## Dependencies
- Python 3.7+
- Required Libraries:
  ```bash
  pip install pandas scikit-learn imbalanced-learn seaborn matplotlib kagglehub
  ```

---

