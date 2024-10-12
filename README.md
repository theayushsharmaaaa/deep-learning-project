


# Fraud Detection in DeFi and Bitcoin Network

## Overview

This repository presents two related projects focused on fraud detection in decentralized financial (DeFi) platforms and Bitcoin transactions using deep learning techniques. 

### 1. **Bitcoin Theft Detection**  
   This project focuses on detecting Bitcoin theft and fraudulent activities in Bitcoin transactions by leveraging machine learning models, such as Random Forest, AdaBoost, SVM, KNN, MLP, and Graph Neural Networks (GNN). The goal is to identify abnormal transactions that indicate theft or fraud, improving the security of the Bitcoin network.

### 2. **DeFi Fraud Detection**  
   This project aims to develop a fraud detection system for DeFi platforms. DeFi platforms have revolutionized the financial world by offering decentralized, permissionless, and transparent services, but they are also vulnerable to fraud like scams, rug pulls, and malicious exploits. The fraud detection system employs deep learning approaches, including anomaly detection, classification models, and graph-based techniques, to flag suspicious activities in real-time.

## Key Features

- **Bitcoin Theft Detection:**
    - **Feature Extraction:** Extracts key features such as transaction volume, frequency, and node centrality from Bitcoin transactions.
    - **Supervised Learning:** Implements Random Forest, AdaBoost, KNN, SVM, and MLP models to classify transactions as normal or theft-related.
    - **Graph-based Learning:** Implements Graph Convolutional Networks (GCN) and Graph Attention Networks (GAT) to model the relationships between Bitcoin transactions and enhance fraud detection.
    - **Data Balancing:** Uses oversampling techniques (e.g., SMOTE) to handle class imbalance between theft and normal transactions.

- **DeFi Fraud Detection:**
    - **Anomaly Detection:** Identifies abnormal transaction patterns using deep learning techniques.
    - **Classification Models:** Utilizes deep learning models to classify transactions as fraudulent or non-fraudulent.
    - **Graph-based Techniques:** Uses graph structure analysis to detect fraudulent behavior based on relationships between users and transactions on the platform.
    - **Real-Time Fraud Detection:** Aims to identify fraud in real-time on DeFi platforms to reduce the risk of financial losses.

## Datasets

### Bitcoin Theft Detection Dataset
We use the **Elliptic dataset** for Bitcoin fraud detection. The dataset includes over 200,000 transactions, labeled as licit or illicit. Each transaction is represented as a node in a graph, where edges represent relationships between transactions. The dataset contains key features such as:
- Transaction timestamps
- Bitcoin flow between addresses
- Identifying heuristics for illicit transactions

The dataset can be accessed from [Elliptic Cryptocurrency Dataset](https://www.kaggle.com/datasets/ellipticco/elliptic-cryptocurrency-dataset).

### DeFi Fraud Detection Dataset
For the DeFi fraud detection, we also use the **Elliptic dataset**, which is structured as a graph where:
- Nodes represent individual Bitcoin transactions.
- Edges represent relationships between transactions.

The dataset provides insights into Bitcoin flow between addresses, which can be used for fraud detection in both Bitcoin and DeFi ecosystems. The dataset can be accessed from [Elliptic Cryptocurrency Dataset](https://www.kaggle.com/datasets/ellipticco/elliptic-data-set/data).

## Approach

### Bitcoin Theft Detection Approach:
1. **Data Preprocessing:**  
   - Clean and preprocess Bitcoin transaction data, including feature extraction for transaction volume, behavior, and relationships between nodes (addresses).
   - Apply oversampling techniques (SMOTE) to handle class imbalance, as theft events are less frequent than normal transactions.

2. **Machine Learning Models:**
    - **Random Forest (RF):** Robust ensemble model for detecting theft events.
    - **AdaBoost:** Boosting model to improve weak classifiers.
    - **KNN (K-Nearest Neighbors):** A simple model used for benchmarking.
    - **SVM (Support Vector Machine):** Effective for binary classification tasks.
    - **MLP (Multilayer Perceptron):** Neural network-based model for non-linear relationships.

3. **Graph Neural Networks (GCN & GAT):**  
   Use graph-based models to capture complex relationships between transactions, treating Bitcoin transactions as nodes and relationships between them as edges.

4. **Evaluation:**  
   Models are evaluated using classification metrics such as accuracy, precision, recall, F1-score, and ROC-AUC.

### DeFi Fraud Detection Approach:
1. **Anomaly Detection:**  
   Use deep learning techniques such as autoencoders and LSTM models to detect anomalies in transaction data, identifying unusual behavior indicative of fraud.

2. **Classification Models:**  
   Train deep learning models to classify transactions as legitimate or fraudulent based on transaction patterns.

3. **Graph-based Fraud Detection:**  
   Use graph-based models like GCN and GAT to identify suspicious patterns in the relationships between users and transactions.

4. **Real-Time Detection:**  
   Implement a real-time fraud detection system that can flag suspicious activities as they happen on DeFi platforms.

## Installation

### Prerequisites:
Ensure you have the following installed:
- Python 3.x
- TensorFlow (for MLP and GNN models)
- Scikit-learn (for traditional machine learning models)
- NetworkX (for graph-based models)
- imbalanced-learn (for oversampling)
- Pandas, NumPy, and Matplotlib (for data processing and visualization)

### Install Dependencies
To install the required libraries, create a `requirements.txt` file and include the following:

```text
numpy
pandas
matplotlib
scikit-learn
tensorflow
networkx
imbalanced-learn
spektral
```

Run the following command to install dependencies:

```bash
pip install -r requirements.txt
```

## Usage

### 1. Data Preprocessing:
To preprocess the data and extract features, run the following script:

```bash
python preprocess.py
```

This script will clean and transform the raw Bitcoin transaction data into a structured format suitable for machine learning.

### 2. Train Machine Learning Models:
To train the traditional machine learning models (Random Forest, AdaBoost, KNN, SVM, MLP), use:

```bash
python train_models.py
```

This will train the models using the preprocessed dataset and save the trained models.

### 3. Model Evaluation:
To evaluate the performance of the models and generate performance metrics, run:

```bash
python evaluate_models.py
```

### 4. Graph-based Model Training (Optional):
To train the Graph Neural Networks (GCN and GAT), use:

```bash
python train_gnn.py
```

This will create and train the GNN models for detecting fraud events based on the graph structure of Bitcoin transactions.

## Expected Outcome

- **Bitcoin Theft Detection:**  
   The model will be able to classify Bitcoin transactions as either normal or theft-related. The system will improve detection accuracy by using a combination of traditional machine learning and graph-based techniques.

- **DeFi Fraud Detection:**  
   The system will identify fraudulent activities such as scams, rug pulls, and malicious exploits in DeFi platforms by analyzing user behavior, transaction patterns, and relationships between entities.

## Results

- **Model Performance Metrics:** A table comparing the precision, recall, F1-score, and other classification metrics of each model.
- **Graph-based Model Accuracy:** Performance of GCN and GAT models for detecting fraud.

## Team

- **Anirudh Chauhan (U20220013)**
- **Ayush Sharma (U20220024)**
- **Manan Chawla (U20220111)**
- **Sakarth Brar (U20220076)**

## Acknowledgments

We would like to thank **Elliptic** for providing the dataset used in both projects. The dataset has been invaluable for developing our fraud detection models.

## Contact

For any inquiries, please contact the project team at [manan.chawla@plaksha.edu.in].
```

### Customizations:
- Make sure to replace `[your-email@example.com]` with your actual email address.
- If you have specific scripts (`preprocess.py`, `train_models.py`, etc.), make sure they are properly referenced and implemented in your project directory.
- Ensure all necessary Python libraries (e.g., `spektral`, `tensorflow`, etc.) are listed in `requirements.txt` and that you have included any other necessary files for the project.
