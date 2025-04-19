# SVM Optimization on UCI Letter Recognition Dataset

## 📌 Overview
This project implements a Support Vector Machine (SVM) optimization strategy on the **UCI Letter Recognition dataset**. It evaluates different SVM models performance across multiple samples with different parameters.

---

## 🚀 Features
- Loads and preprocesses the UCI Letter Recognition dataset
- Creates 10 different train/test splits for robustness
- Performs 100 iterations of random SVM parameter tuning per sample
- Tracks and saves:
  - Best accuracy and corresponding parameters per sample
  - Convergence graph of best model
  - Class distribution and feature correlation plots

---

## 📊 Dataset
- **Name**: Letter Recognition
- **Source**: UCI Machine Learning Repository
- **Format**: `.data` file with 17 columns
- **Samples**: 20,000
- **Features**: 16 integer-based statistical features
- **Target**: Letters A–Z (capital letters)

---

## 🧪 Methodology
1. **Data Loading**: Loads `.data` into a pandas DataFrame and assigns column names.
2. **Sampling**: Creates 10 randomized training and testing sets using different random seeds.
3. **SVM Optimization**:
   - Uses `SVC` from `scikit-learn`
   - Randomly varies:
     - `C` (regularization strength)
     - `kernel` (`'linear'` or `'rbf'`)
   - Evaluates 100 configurations per sample and records the best.
4. **Evaluation**:
   - Saves best parameters and accuracy
   - Plots convergence over iterations for best-performing sample
   - Visualizes data using class distribution and correlation heatmap

---

## 📈 Results
- Best SVM configuration per sample is recorded in `svm_best_results.csv`
- Convergence trend of best model shown in `svm_convergence_graph.png`
- Data exploration insights through:
  - `svm_class_distribution.png`
  - `svm_feature_correlation.png`

---

## 📁 Output Files
| File Name                    | Description                                 |
|-----------------------------|---------------------------------------------|
| `svm_best_results.csv`      | Best accuracy and parameters for each sample|
| `svm_convergence_graph.png` | Line plot showing accuracy over iterations  |
| `svm_class_distribution.png`| Class frequency across A-Z                  |
| `svm_feature_correlation.png`| Heatmap of feature correlations            |

---

## 📎 Dependencies
- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

---

## 📚 References
- [UCI Letter Recognition Dataset](https://archive.ics.uci.edu/ml/datasets/Letter+Recognition)
- [scikit-learn SVM Documentation](https://scikit-learn.org/stable/modules/svm.html)

## Contributor
Kartik Sidana



