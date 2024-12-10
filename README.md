
# **HodlMyBeer: Fraud Detection in Decentralized Finance (DeFi)**

## **Project Overview**

**HodlMyBeer** is an innovative fraud detection project designed for decentralized financial platforms, specifically leveraging blockchain network analysis. Initially focused on detecting fraudulent activities within Bitcoin transactions using the **Elliptic Dataset**, we transitioned to the advanced **Elliptic++ Dataset** to deepen our analysis. 

The **Elliptic++ Dataset** provides richer and more diverse insights into the relationships between wallets and transactions, allowing for the creation of a **bipartite graph structure**. This unique dataset enables not only the identification of illicit transactions but also the detection of fraudulent wallets, making this project novel in its application to both actor-level and transaction-level fraud detection.

Our mission is to create a robust fraud detection system that harnesses cutting-edge graph neural network (GNN) techniques to improve security within decentralized finance ecosystems.

---

## **Key Objectives**

1. Transition from Bitcoin transaction-specific fraud detection to a **heterogeneous graph-based detection system** using the **Elliptic++ Dataset**.
2. Identify illicit wallet addresses and fraudulent transactions by analyzing both actor and transaction nodes within the blockchain network.
3. Introduce novel methodologies for analyzing **bipartite graphs**, combining actor-level and transaction-level insights for a more comprehensive fraud detection framework.
4. Address severe class imbalance with techniques like **oversampling, cost-sensitive learning, and weighted loss functions** to ensure robust model performance.

---

## **Dataset: Elliptic++**

The **Elliptic++ Dataset** represents an enriched blockchain transaction dataset, capturing both **actor-level (wallet)** and **transaction-level** data, organized as a **heterogeneous graph**. 

### **Dataset Highlights**

- **Node Categories:**
  - **Transactions:** ~203,769 nodes, each with 166 features.
  - **Wallets (Actors):** ~1,268,260 nodes, each with 55 features.
- **Edge Types:**  
  - Transaction-to-Transaction (234,355 edges)
  - Transaction-to-Wallet (837,124 edges)
  - Wallet-to-Transaction (477,117 edges)
  - Wallet-to-Wallet (2,868,964 edges)

### **Fraud Statistics**

- **Licit Transactions:** ~21%  
- **Illicit Transactions:** ~2%  
- **Unlabeled Transactions:** ~77%  
- **Wallet Nodes:** Licit and illicit wallets with unknown statuses.

### **Features**

1. **Transaction-Level Features:**  
   - Time step (1–49): Represents bi-weekly intervals.
   - Localized transaction data: Input/output counts, transaction fees, and output volumes.
   - Aggregated statistics from one-hop neighbors: Maximum, minimum, and standard deviations.

2. **Actor-Level Features (Wallets):**  
   - Behavioral characteristics: Total transactions as sender/receiver, lifetime in blocks, and average transaction values.

### **Novel Contributions of the Dataset**

- Introduces a **bipartite graph** structure for blockchain analysis, linking wallets and transactions.
- Provides both **heterogeneous graph data** and a foundation for exploring **multi-relational GNNs**.
- Captures temporal dynamics with a well-defined time-step attribute, enabling time-series analysis.

---

## **Novel Contributions of the Project**

1. **Bipartite Graph Learning:**  
   Our project uniquely integrates heterogeneous graph analysis, allowing for simultaneous detection of fraudulent wallets and illicit transactions.

2. **Advanced GNN Architectures:**  
   - **Heterogeneous Graph Neural Networks (Hetero-GNNs):** Process actor and transaction data as distinct node types, enhancing the detection of multi-relational fraud patterns.
   - **Graph Attention Networks (GATs):** Dynamically prioritize relationships between nodes to capture nuanced blockchain behaviors.

3. **Severe Class Imbalance Handling:**  
   - Use of **oversampling techniques (e.g., SMOTE)** for the minority illicit class.
   - **Weighted Cross-Entropy Loss:** Ensures models prioritize rare fraudulent patterns.

4. **Visualization of Blockchain Graphs:**  
   - Employs **NetworkX** for subgraph rendering and visual exploration.
   - Provides an intuitive view of the blockchain network, revealing transaction and wallet connections.

---

## **Approach**

### **Methodology**

1. **Feature Engineering:**  
   - Extract localized and aggregated features for both transactions and wallets.
   - Derive graph-based metrics such as node centrality and clustering coefficients.

2. **Model Selection:**  
   - Compare traditional machine learning (e.g., Random Forest, SVM) with advanced graph-based models (e.g., GCNs, GATs, Hetero-GNNs).

3. **Data Balancing:**  
   - Apply techniques like **oversampling** and **cost-sensitive learning** to mitigate class imbalance.

4. **Graph-Based Learning:**  
   - Train heterogeneous GNNs on **actor-transaction bipartite graphs**.

---

## **Models**

### **Traditional Machine Learning Models**
- **Random Forest:** Baseline model for robust performance.
- **Support Vector Machine (SVM):** Handles imbalanced datasets effectively.
- **Multilayer Perceptron (MLP):** Detects complex, non-linear relationships.

### **Graph-Based Models**
- **Graph Convolutional Networks (GCNs):** Learn node embeddings using graph topology.
- **Graph Attention Networks (GATs):** Assign attention scores to node relationships dynamically.
- **Heterogeneous GNNs (Hetero-GNNs):** Handle multi-relational data for actor and transaction graphs.

---

## **Results**

### **Baseline Models:**  
- Traditional models achieved moderate success but struggled with imbalanced data.

### **Graph-Based Models:**  
- **GCNs and GATs** significantly outperformed traditional models, leveraging graph structure.
- **Heterogeneous GNNs** provided the most comprehensive insights, detecting fraud at both wallet and transaction levels.

### **Key Metrics:**
- **Precision:** High precision for both licit and illicit classes.
- **Recall:** Improved recall for illicit transactions due to enhanced class balancing techniques.

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
   ```bash
   python models/hetero_gnn.py
   ```

4. **Explore Jupyter Notebooks**
   Analyze the dataset and model training in the `notebooks/` directory.

---

## **Future Directions**

1. Explore advanced GNNs like Graph Isomorphism Networks (GIN).
2. Extend fraud detection to real-time transaction streams.
3. Integrate the system with blockchain nodes for real-time fraud alerts.
4. Analyze temporal dynamics in actor and transaction behaviors.

---

## **Contributors**

- **Ayush Sharma**
- **Anirudh Chauhan**
- **Manan Chawla**
- **Sakarth Singh Brar**

---

## **References**

- Youssef Elmougy and Ling Liu. "Demystifying Fraudulent Transactions and Illicit Nodes in the Bitcoin Network for Financial Forensics." KDD 2023.
- [Elliptic++ Dataset Documentation](https://ellipticplusplus.org/)

---
