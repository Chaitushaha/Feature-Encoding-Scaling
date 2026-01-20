# Feature-Encoding-Scaling
# Adult Income Dataset – Preprocessing Project
## Tools / Libraries Used
- Python: Pandas, Matplotlib, Seaborn
## Dataset
- **Name:** Adult Income Dataset
 
## Steps Followed

### 1. Identify Categorical and Numerical Features
- **Numerical columns:** age, fnlwgt, education-num, capital-gain, capital-loss, hours-per-week
- **Categorical columns:** workclass, education, marital-status, occupation, relationship, race, sex, native-country, income

### 2. Label Encoding
- Applied on **`education`** column (since it has natural order)
- Converts text categories to numeric labels

### 3. One-Hot Encoding
- Applied on categorical columns **without natural order:** workclass, marital-status, occupation, relationship, race, sex, native-country
- Converts each category into separate binary columns

### 4. Scaling Numerical Features
- Used **StandardScaler** on numerical columns
- Features now have mean ≈ 0 and standard deviation ≈ 1
- Helps balance the data for machine learning models

### 5. Compare Before vs After Scaling
- **Before scaling:** Numerical features had very different ranges
- **After scaling:** All numerical features are on similar scale
- Dataset is more ready for ML models

### 6. Impact of Scaling on ML Algorithms
- **Distance-based algorithms (KNN, K-Means):** Prevents large values from dominating
- **Gradient-based algorithms (Linear/Logistic Regression, Neural Networks):** Faster and stable learning
- **Tree-based algorithms (Decision Tree, Random Forest):** No effect

### 7. Save Processed Dataset
- Processed dataset saved as **`adult_processed.csv`**
- Includes scaled numerical features and one-hot encoded categorical features

# Deliverables
1. **Preprocessed Dataset:** `adult_processed.csv`
2. **Notebook:**
- Screenshots of dataset head and describe outputs are included in the notebook
- All preprocessing steps are reproducible
