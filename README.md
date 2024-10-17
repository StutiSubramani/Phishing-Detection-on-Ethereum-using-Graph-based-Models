# Phishing-Detection-on-Ethereum-using-Graph-based-Models

## Project Overview

Phishing scams on the Ethereum blockchain have become increasingly prevalent as attackers target users to steal funds or sensitive information. Traditional phishing detection methods struggle to adapt to the diverse and constantly evolving tactics of cybercriminals. This project aims to improve phishing detection on Ethereum using graph-based analysis of the transaction network's structure.

## Objectives

The main objectives of this project are:

To explore the potential of graph-based models for detecting phishing scams on the Ethereum blockchain.
To evaluate different machine learning models and identify the most effective approach for classifying phishing and non-phishing addresses.
To address challenges such as data imbalance and the complexity of transaction networks in phishing detection.

## Methods

The project employed several graph-based methods to classify Ethereum addresses as phishing or non-phishing:

Node2Vec: Generates node embeddings via random walks to represent network structure.
Graph2Vec: Creates embeddings for entire subgraphs to capture richer context.
Graph Convolutional Networks (GCNs): Leverages the graph structure to propagate and integrate both local and global information.
GraphSAGE: An inductive approach that aggregates features from node neighborhoods to create embeddings.
Trans2Vec: Combines biased random walks with transaction features like amount and timestamp to generate node embeddings.
These embeddings were classified using models such as Logistic Regression, SVM, Random Forest, and k-Nearest Neighbors (KNN). Performance was evaluated using accuracy, precision, recall, and F1-score, and class imbalance was addressed using SMOTE and upsampling techniques.

## Key Results

The GCN model performed the best, achieving high accuracy, precision, and recall in detecting phishing addresses.
Ego graph methods, which focus on the local neighborhood of nodes, showed potential in enhancing detection accuracy.
Full-graph methods struggled with class imbalance, leading to lower performance, especially in classifying phishing nodes.

## Data Source

The dataset for this project was derived from Ethereum transaction records and included:

1600+ verified phishing addresses from Etherscan.
Normal addresses randomly selected to match the number of phishing addresses.
Transaction data, including amounts, timestamps, and network interactions between addresses.

## Tools & Technologies

The project made use of various tools and technologies, including:

Graph-based models: Node2Vec, Graph2Vec, GCN, GraphSAGE, Trans2Vec.
Machine learning classifiers: Logistic Regression, SVM, Random Forest, k-Nearest Neighbors (KNN).
Techniques to handle class imbalance: SMOTE and upsampling.
Libraries: Gensim (for embedding generation), Scikit-learn (for classification), and various graph neural network frameworks.
