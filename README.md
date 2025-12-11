# 🧠 Bank Marketing Campaign Classification with Deep Neural Networks

Predicting whether a bank customer will subscribe to a term deposit is a classic business intelligence and machine learning problem. In this project, we apply a Deep Neural Network (DNN) using Keras to classify whether a customer is likely (`deposit=1`) or unlikely (`deposit=0`) to subscribe, based on features such as age, contact duration, and previous campaign outcomes.

---

## 📌 Project Highlights

- 📊 Preprocessing of numerical and categorical data  
- 🧮 Model built using Keras (with scikit-learn wrapper)  
- 📉 Visual evaluations: Confusion Matrix, ROC Curve, Precision-Recall Curve, Calibration Plot  
- 📌 Feature interpretation using Permutation Importance (Radar Chart)  
- ✅ Achieved 86% Accuracy and AUC of 0.92 on the test set  

---

## 🧪 Dataset Overview

- **Source**: UCI Bank Marketing Dataset  
- **Target Variable**: `deposit` (yes/no → 1/0)  
- **Number of Rows**: ~11,000  
- **Features**: Demographic + campaign-related (e.g., `job`, `balance`, `duration`, `month`, `poutcome`)

---

## 🛠️ Model Architecture

- **Input**: 42 features after encoding and scaling
- **Layers**:
  - Dense(64, relu) → BatchNorm → Dropout(0.3)
  - Dense(32, relu) → BatchNorm → Dropout(0.2)
  - Dense(16, relu) → BatchNorm → Dropout(0.2)
  - Dense(1, sigmoid)
- **Loss Function**: Binary Crossentropy  
- **Optimizer**: Adam  
- **Regularization**: Dropout & EarlyStopping  

---

## 📈 Evaluation Metrics

| Metric        | Value  |
|---------------|--------|
| Accuracy      | 86%    |
| Recall (Class 1) | 90% |
| AUC-ROC       | 0.92   |

---

## 📊 Visualizations

- Confusion Matrix (Mako colormap)
- ROC Curve and AUC
- Precision-Recall Curve
- Calibration Plot (Model Confidence)
- Radar Chart for Top 8 Feature Importances

---

```bash
# Clone the repository
git clone https://github.com/yourusername/BankMarketing-DNN.git
cd BankMarketing-DNN