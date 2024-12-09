
# **HodlMyBeer: Fraud Detection in Decentralized Finance (DeFi)**

## **Project Overview**

**HodlMyBeer** initially began as an exploration of fraud detection within Bitcoin transactions. The project aimed to identify illicit activities like scams, malware, and Ponzi schemes using the **Elliptic Dataset**, which provided a transaction graph from the Bitcoin blockchain.

During our research, we discovered the **Elliptic++ Dataset**, a more comprehensive and enriched dataset designed for fraud detection in decentralized financial ecosystems. This dataset offers deeper insights into transaction patterns, wallet behaviors, and graph structures. Recognizing its potential, we transitioned our project to leverage the **Elliptic++ Dataset** for building a robust fraud detection system for decentralized finance (DeFi) platforms.

This decision was driven by the dataset’s inclusion of both **transaction-level** and **actor-level** data, enabling more granular analysis of fraudulent behavior. Our mission is to develop a cutting-edge detection system that secures DeFi ecosystems against illicit activities.

---

## **Key Objectives**

1. Transition from Bitcoin-centric fraud detection to a broader DeFi fraud detection framework using **Elliptic++ Dataset**.
2. Detect illicit wallet addresses and fraudulent transactions by analyzing graph-based features.
3. Combine traditional machine learning methods with graph neural networks (GNNs) to enhance detection accuracy.
4. Address the challenges of imbalanced datasets with advanced techniques like oversampling and weighted loss functions.

---

## **Dataset: Elliptic++**

The **Elliptic++ Dataset** provides an extensive view of Bitcoin transactions, addressing both **transaction-level** and **actor-level** data. It offers detailed statistics and features that enable in-depth fraud detection.

### **Dataset Highlights**

- **203,769 Node Transactions**
- **234,355 Directed Edges**, representing payment flows
- **Wallet-Level Data:** Categorization into licit and illicit wallets
- **Feature-Rich Data:**  
  - **166 Transaction-Level Features**
  - **Actor-Level Attributes** detailing wallet behaviors

### **Fraud Statistics**
- **Licit Transactions:** ~21%
- **Illicit Transactions:** ~2%
- **Unlabeled Transactions:** ~77%

### **Features**
- **Transaction Features:** Detailed metrics like transaction fees, input/output volume, and average Bitcoin received.
- **Graph-Based Features:** Aggregated statistics from neighboring nodes, capturing structural insights.

---

## **Approach**

### **Methodology**
The project uses a blend of traditional machine learning and graph-based learning approaches to detect fraud in DeFi. Key steps include:
1. **Feature Engineering:** Extract key characteristics such as transaction volume, wallet centrality, and temporal patterns.
2. **Model Selection:** Implement and compare performance across various models.
3. **Graph-Based Learning:** Leverage GNNs to analyze the topological and structural properties of transaction graphs.

---

## **Models**

### **Traditional Machine Learning Models**
- **Random Forest (RF):** Baseline model for robust performance.
- **AdaBoost:** Boosting technique to refine decision boundaries.
- **Support Vector Machine (SVM):** Effective for imbalanced datasets.
- **k-Nearest Neighbors (KNN):** Benchmark for simple classification.
- **Multilayer Perceptron (MLP):** Detects non-linear relationships in features.

### **Graph-Based Models**
- **Graph Convolutional Networks (GCNs):** Incorporates node and edge features to analyze transaction graphs.
- **Graph Attention Networks (GATs):** Dynamically focuses on important neighboring nodes, capturing nuanced relationships.

### **Addressing Data Imbalance**
Given the low proportion of illicit transactions, we employ techniques like:
- **Synthetic Minority Oversampling (SMOTE):** To balance the dataset.
- **Weighted Loss Functions:** Prioritize minority classes during model training.

---

## **Insights and Challenges**

- **From Bitcoin to DeFi:** Transitioning to the **Elliptic++ Dataset** allowed us to adopt a more comprehensive approach to fraud detection.
- **Graph-Based Learning:** GNNs outperform traditional models in detecting complex fraud patterns.
- **Imbalanced Data:** Overcoming data imbalance significantly improves recall for illicit transactions.
- **Scalability:** The models are designed to handle large-scale transaction graphs, essential for real-world DeFi platforms.

---

## **Results**

- **Baseline Models:**  
  - Random Forest achieved satisfactory precision but struggled with imbalanced data.
  - Graph-based models like GCN and GAT significantly improved illicit transaction detection, especially in terms of recall.

- **Key Metrics:**  
  - **Precision:** High precision for both licit and illicit transactions.
  - **Recall:** Recall for illicit transactions improved after applying oversampling and weighted loss functions.

---

## **How to Run**

1. **Clone the Repository**
   ```bash
   git clone https://github.com/theayushsharmaaaa/deep-learning-project
   cd deep-learning-project
   ```

2. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run Models**
   Execute the desired model script:
   ```bash
   python models/random_forest.py
   ```

4. **Explore Jupyter Notebooks**
   The `notebooks/` directory contains EDA and model experimentation notebooks.

---

## **Future Directions**

1. Extend fraud detection to real-time DeFi transaction data.
2. Experiment with more advanced GNN architectures, such as Graph Isomorphism Networks (GIN).
3. Integrate the model into a live blockchain node for on-the-fly fraud detection.

---

## **Contributors**

- Ayush Sharma
- Anirudh Chauhan
- Manan Chawla
- Sakarth Singh Brar

---

For more details, refer to our [project repository](https://github.com/theayushsharmaaaa/deep-learning-project).

---
