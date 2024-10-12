# HodlMyBeer: Fraud Detection in DeFi

## Project Overview

**HodlMyBeer** aims to develop an advanced fraud detection system specifically designed for decentralized financial platforms like Bitcoin. Leveraging cutting-edge machine learning and deep learning models, the project seeks to identify suspicious and fraudulent transactions in Bitcoin by analyzing transactional patterns and behaviors.

We use the **Elliptic Dataset**, which maps Bitcoin transactions to entities (licit and illicit). This dataset provides a transaction graph from the Bitcoin blockchain, making it possible to detect illicit activities such as scams, malware, and Ponzi schemes.

### Key Objectives:
1. Build a fraud detection model to identify Bitcoin theft and other illicit transactions.
2. Apply both traditional and graph-based machine learning methods to improve detection accuracy.
3. Mitigate the imbalance between legitimate and fraudulent transactions.

---

## Dataset

The **Elliptic Dataset** is used in this project. It maps Bitcoin transactions to real-world entities, either licit (wallet providers, miners, exchanges) or illicit (scams, malware, terrorist organizations, Ponzi schemes).  
The dataset consists of:
- **203,769 node transactions**
- **234,355 directed edges** representing payment flows  
Only **2%** of the nodes are labeled as illicit, while **21%** are classified as licit. The rest are unlabeled.

### Features:
Each node in the dataset has **166 features**, which include:
- **94 local features:** Transaction details such as transaction fees, inputs/outputs, and average volume of Bitcoin received.
- **72 aggregated features:** Aggregated statistics from neighboring transactions, including the maximum, minimum, and standard deviation of transactional properties.

---

## Approach

### Methodology:
We employ a mix of machine learning and graph-based learning techniques to detect illicit Bitcoin transactions:
- **Feature Extraction:** Transaction volume, node centrality, and other key characteristics.
- **Supervised Learning Models:**  
  - Random Forest
  - AdaBoost
  - Support Vector Machine (SVM)
  - k-Nearest Neighbor (KNN)
  - Multilayer Perceptron (MLP)
- **Graph Neural Networks:**  
  - Graph Convolutional Networks (GCNs)
  - Graph Attention Networks (GATs)
  
These models leverage the topological structure of the blockchain to detect fraudulent activities.

### Data Balancing:
Given the imbalance in the dataset (only 2% illicit transactions), we use oversampling techniques such as **SMOTE** to balance the data and ensure that our models are not biased toward the majority class.

---

## Models Used

### 1. **Random Forest (RF):** 
   - Used for its robustness and ability to handle imbalanced data. This is our baseline model.

### 2. **AdaBoost:**
   - Applied to improve classification of complex decision boundaries and enhance precision.

### 3. **k-Nearest Neighbor (KNN):**
   - A simple, non-parametric model used to benchmark our results.

### 4. **Support Vector Machine (SVM):**
   - Effective in detecting rare events and building strong decision boundaries.

### 5. **Multilayer Perceptron (MLP):**
   - A deep learning model that detects non-linear relationships between transactions.

### 6. **Graph Convolutional Networks (GCN):**
   - Incorporates node-level and structural information from the transaction graph.

### 7. **Graph Attention Networks (GAT):**
   - Dynamically assigns attention to nodes’ neighbors, capturing nuanced relationships in the transaction graph.

---

## Key Insights

- **Feature Extraction** from transaction graphs is crucial in identifying fraudulent patterns.
- **Supervised Learning Models** generally outperform unsupervised methods in terms of interpretability and accuracy.
- **Graph-based Models** (GCNs, GATs) offer a unique capability to analyze the structural properties of Bitcoin transactions and improve fraud detection.
- **Data Imbalance Techniques** like oversampling help mitigate bias toward the majority class and improve recall.

---

## Project Structure

```
hodlmybeer/
│
├── data/                      # Dataset (Elliptic Dataset)
├── models/                    # Machine learning and GNN models
│   ├── random_forest.py        # Random Forest implementation
│   ├── adaboost.py             # AdaBoost implementation
│   ├── knn.py                  # KNN implementation
│   ├── svm.py                  # SVM implementation
│   ├── mlp.py                  # Multilayer Perceptron implementation
│   ├── gcn.py                  # Graph Convolutional Network implementation
│   └── gat.py                  # Graph Attention Network implementation
├── notebooks/                  # Jupyter notebooks for exploration
├── scripts/                    # Preprocessing and utility scripts
├── README.md                   # Project readme
└── requirements.txt            # Python package dependencies
```

---

## Results

- The Random Forest model serves as a strong baseline, with GNN models showing improvements in detecting complex fraud patterns.
- Balancing the dataset significantly enhances recall for illicit transactions.

---

## How to Run

1. **Clone the repository:**
   ```bash
   git clone https://github.com/theayushsharmaaaa/deep-learning-project
   cd deep-learning-project
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run models:**
   You can run any of the models by executing the corresponding script. For example, to run the Random Forest model:
   ```bash
   python models/random_forest.py
   ```

4. **Explore Jupyter notebooks:**
   Explore the transaction data and models using the provided notebooks in the `notebooks/` directory.

---

## Future Work

1. Experiment with more advanced graph-based models.
2. Test on additional datasets or real-time Bitcoin transaction data.
3. Implement a live fraud detection pipeline integrated with blockchain nodes.

---

## Contributors

- Anirudh Chauhan
- Ayush Sharma
- Manan Chawla
- Sakarth Singh Brar

---

For more details, refer to our [project repository](https://github.com/theayushsharmaaaa/deep-learning-project).

---

This README is designed to guide users through the project setup, methodology, and model implementations for the **HodlMyBeer** fraud detection system. Let me know if you need any further modifications!

