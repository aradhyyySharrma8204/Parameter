
# 🧠 SVM Parameter Optimization on the Letter Recognition Dataset

## 📌 Project Overview

This project explores the optimization of **SVM (Support Vector Machine)** parameters using the **Letter Recognition Dataset** from OpenML. The focus is on experimenting with various kernel types and SVM hyperparameters (nu and epsilon) to evaluate classification accuracy. The goal is to identify the best configuration for each of 10 samples and visualize convergence over iterations.

---

## ⚙️ Methodology

1. **Dataset**: Letter Recognition dataset fetched from `openml.org`.
2. **Preprocessing**:
   - Features are normalized using `StandardScaler` for improved performance.
3. **Model**:
   - `NuSVC` from `sklearn.svm` is used.
   - Kernels tried: `'rbf'`, `'poly'`
   - Random sampling of `nu` and `epsilon` in each iteration for exploration.
4. **Process**:
   - For each of **10 samples (S1 to S10)**:
     - A new train-test split (70-30) is generated using a different random seed.
     - **20 iterations** of randomized parameter search are conducted.
     - The best accuracy and corresponding parameters are recorded for each sample.
5. **Visualization**:
   - A convergence graph is plotted for the sample achieving the **highest accuracy**, showing accuracy over the 20 iterations.

---

## 📈 Results

| Sample # | Best Accuracy (%) | Best SVM Parameters (kernel, nu, epsilon) |
|----------|-------------------|--------------------------------------------|
| S1       | 94.62             | rbf, 0.10, 0.23                            |
| S2       | 94.95             | rbf, 0.10, 0.12                            |
| S3       | 95.35             | rbf, 0.10, 0.23                            |
| S1       | 85.13             | rbf, 0.40, 0.01                            |
| S2       | 85.02             | rbf, 0.40, 0.17                            |
| S3       | 91.57             | rbf, 0.20, 0.39                            |
| S4       | 87.50             | poly, 0.30, 0.45                           |
| S1       | 91.17             | poly, 0.20, 0.45                           |
| S2       | 91.30             | rbf, 0.20, 0.34                            |
| S3       | 91.57             | rbf, 0.20, 0.17                            |
| S4       | 91.20             | rbf, 0.20, 0.45                            |
| S5       | 94.80             | rbf, 0.10, 0.12                            |
| S6       | 94.30             | poly, 0.10, 0.17                           |
| S7       | 86.90             | rbf, 0.30, 0.17                            |
| S8       | 90.50             | poly, 0.20, 0.34                           |
| S9       | 90.97             | poly, 0.20, 0.39                           |
| S10      | 94.90             | rbf, 0.10, 0.23                            |

---

## 🌟 Best Configuration

- **Sample**: `S3`
- **Best Accuracy**: `95.35%`
- **Best Parameters**: `rbf kernel, nu = 0.10, epsilon = 0.23`

---

## 📊 Convergence Graph

**Figure 1: Accuracy Convergence Plot (Best Sample: S3)**

This graph shows how the classification accuracy changes across 20 iterations of randomized parameter search for the best-performing sample:

![Convergence Plot](https://github.com/aradhyyySharrma8204/Parameter/blob/main/ConvergenceGraph.png)


---

## 🧪 Technologies Used

- Python
- Scikit-learn
- Matplotlib & Seaborn
- NumPy & Pandas
