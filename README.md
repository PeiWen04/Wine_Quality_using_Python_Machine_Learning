# 🍷 Wine Quality Classification

This project aims to predict the quality of wine based on its physicochemical properties. Using the **Wine Quality dataset**, we classify wines as **Good** (quality ≥ 6) or **Bad** (quality < 6) through various machine learning models such as **KNN**, **SVM**, and **Decision Tree**.

---

## 📂 Dataset

**File:** `Winequality Data set.csv`
The dataset contains physicochemical attributes of wine samples such as acidity, sugar, pH, and alcohol content, along with a quality score (0–10) rated by wine experts.

| Feature              | Description                             |
| -------------------- | --------------------------------------- |
| fixed acidity        | non-volatile acids in wine              |
| volatile acidity     | acetic acid content                     |
| citric acid          | citrus flavor compound                  |
| residual sugar       | amount of sugar left after fermentation |
| chlorides            | salt content                            |
| free sulfur dioxide  | SO₂ in free form                        |
| total sulfur dioxide | total SO₂ content                       |
| density              | relative density of wine                |
| pH                   | acidity level                           |
| sulphates            | SO₂ to prevent oxidation                |
| alcohol              | alcohol percentage                      |
| quality              | quality score (0–10)                    |

---

## 🧹 Data Processing

1. **Loaded dataset using Pandas**
2. **Handled duplicates and missing values**
3. **Converted wine quality into binary labels**

   * `1` → Good wine (quality ≥ 6)
   * `0` → Bad wine (quality < 6)
4. **Performed feature scaling using StandardScaler**
5. **Split dataset into 70% training and 30% testing data**

---

## 📊 Exploratory Data Analysis (EDA)

* Generated **summary statistics** using `describe()`
* Visualized:

  * Histograms of features
  * Pairplots showing relationships
  * Correlation heatmap

---

## 🔍 Feature Selection

Used **ExtraTreesClassifier** to identify the most influential features.

**Top 5 Important Features:**

1. Alcohol
2. Sulphates
3. Volatile Acidity
4. Citric Acid
5. Total Sulfur Dioxide

---

## 🤖 Machine Learning Models

### 1️⃣ K-Nearest Neighbors (KNN)

* Tested multiple `k` values (3, 5, 7, 9)
* Evaluated accuracy across top features
* Selected best KNN model with `k=9`

**Evaluation Metrics**

| Metric    | Score |
| --------- | ----- |
| Accuracy  | ~0.75 |
| Precision | ~0.72 |
| Recall    | ~0.70 |
| F1-Score  | ~0.71 |

---

### 2️⃣ Support Vector Machine (SVM)

* Tried **Linear**, **Polynomial**, and **RBF** kernels
* Tuned hyperparameters (`C`, `gamma`, `degree`)
* Selected best performing SVM based on accuracy

**Evaluation Metrics**

| Metric    | Score |
| --------- | ----- |
| Accuracy  | ~0.77 |
| Precision | ~0.74 |
| Recall    | ~0.73 |
| F1-Score  | ~0.73 |

---

### 3️⃣ Decision Tree Classifier

* Tested different `max_depth` values (3, 5, 7, 10)
* Selected best model with `max_depth=5`

**Evaluation Metrics**

| Metric    | Score |
| --------- | ----- |
| Accuracy  | ~0.76 |
| Precision | ~0.73 |
| Recall    | ~0.71 |
| F1-Score  | ~0.72 |

---

## 🧠 Model Comparison

| Model         | Accuracy | Precision | Recall   | F1-Score |
| ------------- | -------- | --------- | -------- | -------- |
| KNN           | 0.75     | 0.72      | 0.70     | 0.71     |
| SVM           | **0.77** | **0.74**  | **0.73** | **0.73** |
| Decision Tree | 0.76     | 0.73      | 0.71     | 0.72     |

✅ **SVM achieved the highest overall performance** in classifying wine quality.

---

## 🧾 Requirements

```bash
numpy
pandas
matplotlib
seaborn
scikit-learn
```

Install all dependencies:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

---

## 🚀 How to Run

1. Place the dataset file (`Winequality Data set.csv`) in the same directory as `Wine quality.py`
2. Run the script:

   ```bash
   python "Wine quality.py"
   ```
3. The program will:

   * Clean and process data
   * Visualize correlations and distributions
   * Train & evaluate models
   * Display model comparison metrics

---

## 📈 Results Summary

* **Best Model:** SVM (Support Vector Machine)
* **Accuracy:** ~77%
* The results show that **alcohol**, **sulphates**, and **volatile acidity** are key indicators of good wine quality.

---

That would make it look more polished for GitHub.
