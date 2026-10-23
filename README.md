# ML Network Intrusion Detector

**IBM SkillsBuild Cyber Security 2026 | BharatCares**
**Author:** Karan Dewangan
**Project:** Machine Learning Based Network Intrusion Detection System

---

## 📌 Project Description

This project implements a **Machine Learning-based Network Intrusion Detection System (NIDS)** that classifies network traffic connections as either **Normal** or **Attack** using the NSL-KDD benchmark dataset.

The system trains and compares four supervised machine learning classifiers:

- Decision Tree
- Random Forest *(Best Performer)*
- Gradient Boosting
- Logistic Regression

Models are evaluated using Accuracy, Precision, Recall, F1-Score, and ROC-AUC. The project also includes feature importance analysis, confusion matrices, ROC curves, and a live prediction demo on unseen traffic samples.

---

## 📂 Dataset

| Property | Details |
|----------|---------|
| **Name** | NSL-KDD Dataset |
| **Source** | https://www.unb.ca/cic/datasets/nsl.html |
| **Files** | `KDDTrain+.txt`, `KDDTest+.txt` |
| **Features** | 41 network traffic features |
| **Labels** | 1 normal class + 22 attack categories |
| **Type** | Tabular / CSV |

> **Note:** If you do not download the dataset, the notebook automatically generates synthetic NSL-KDD-style data for a full end-to-end demonstration.

---

## 🛠️ Technologies Used

| Technology | Purpose |
|-----------|---------|
| Python 3.9+ | Core programming language |
| Jupyter Notebook | Interactive development & presentation |
| NumPy / Pandas | Data manipulation |
| Scikit-learn | Machine learning models & evaluation |
| Matplotlib / Seaborn | Data visualization |

---

## 🗂️ Project Structure

```
ML-Network-Intrusion-Detector/
├── KaranDewangan_MLNetworkIntrusionDetector.ipynb   # Main Jupyter Notebook
├── requirements.txt                                # Python dependencies
├── README.md                                       # Project overview
├── KaranDewangan_ProjectReport.pdf                 # Full project report
├── KDDTrain+.txt                                   # (Optional) NSL-KDD training data
└── KDDTest+.txt                                    # (Optional) NSL-KDD test data
```

---

## ⚙️ Setup & Run Instructions

### 1. Clone the repository

```bash
git clone https://github.com/YourUsername/ML-Network-Intrusion-Detector.git
cd ML-Network-Intrusion-Detector
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. (Optional) Download the NSL-KDD Dataset

Download `KDDTrain+.txt` and `KDDTest+.txt` from:
https://www.unb.ca/cic/datasets/nsl.html
Place them in the **same folder** as the notebook.

> If not downloaded, the notebook uses auto-generated synthetic data automatically — no setup needed.

### 4. Launch Jupyter Notebook

```bash
jupyter notebook KaranDewangan_MLNetworkIntrusionDetector.ipynb
```

### 5. Run All Cells

In Jupyter: **Kernel → Restart & Run All**

---

## 📊 Key Results

| Model | Accuracy | F1-Score | ROC-AUC |
|-------|----------|----------|---------|
| Decision Tree | ~95% | ~0.95 | ~0.95 |
| **Random Forest** | **~97%** | **~0.97** | **~0.98** |
| Gradient Boosting | ~96% | ~0.96 | ~0.97 |
| Logistic Regression | ~88% | ~0.88 | ~0.92 |

*Results may vary slightly depending on whether synthetic or real NSL-KDD data is used.*

---

## 🖼️ Output Graphs Generated

| File | Description |
|------|-------------|
| `label_distribution.png` | Attack type distribution & Normal vs Attack pie chart |
| `protocol_flag_dist.png` | Protocol and flag distribution |
| `confusion_matrices.png` | Confusion matrices for all 4 models |
| `roc_curves.png` | ROC curves comparison |
| `feature_importance.png` | Top 20 Random Forest feature importances |
| `model_comparison.png` | Bar chart comparing all metrics across models |

---

## 🔐 Cybersecurity Relevance

This system models how a **Security Operations Center (SOC)** analyst can use ML to:

- Automate detection of port scans, DoS/DDoS, and brute-force attempts
- Reduce manual log analysis workload
- Integrate with SIEM/SOAR pipelines for automated response
- Flag zero-day anomalies that signature-based IDS would miss

---

## 📚 References

1. Tavallaee, M. et al. (2009). *A Detailed Analysis of the KDD CUP 99 Data Set*
2. NSL-KDD Dataset — University of New Brunswick: https://www.unb.ca/cic/datasets/nsl.html
3. OWASP Top 10 Security Risks — https://owasp.org
4. NIST Cybersecurity Framework — https://www.nist.gov/cyberframework
5. Scikit-learn Documentation — https://scikit-learn.org
