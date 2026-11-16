# 🕸️ Graph Based Financial Fraud Ring Detection System

An advanced data science and network science pipeline designed to uncover coordinated financial crime syndicates using **Graph Theory, Topological Centrality Metrics, and Community Detection Algorithms**. 

---

## 📌 Executive Summary
Traditional rule based fraud detection systems and standard tabular machine learning models (such as isolated customer churn or classification models) evaluate accounts and transactions in independent silos. Sophisticated fraud syndicates such as synthetic identity rings and money laundering rings exploit this blind spot by fragmenting illicit funds across dense, cyclical transfer loops. 

This project implements a **Network Topology Engine** that transforms flat transactional records into a directed graph network, allowing institutions to mathematically isolate hidden criminal rings that look completely normal on an individual basis.

---

## 🚀 Key Capabilities & Architecture

1. **Synthetic Enterprise Transaction Generation (`generate_graph_data.py`):**
   - Simulates thousands of legitimate retail background transactions across hundreds of accounts.
   - Programmatically injects a coordinated, high-velocity fraud ring executing dense structural loops and structuring amounts to mimic real-world financial crime patterns.

2. **Graph Construction & Mathematical Analysis (`analyze_network.py`):**
   - Constructs a directed graph (`DiGraph`) using `NetworkX` to map account-to-account fund flows.
   - Computes advanced structural metrics:
     - **Degree Centrality:** Identifies accounts with the highest immediate transaction partners.
     - **Betweenness Centrality:** Mathematically isolates structural "bridges" and bottlenecks the exact nodes coordinating fund movement between separate clusters.
     - **PageRank:** Quantifies systemic influence across the broader financial network.

3. **Louvain Community Detection:**
   - Unsupervised partitioning of the network into distinct topological communities based on edge weights and connection density, automatically clustering the hidden fraud syndicate without prior labeling.

4. **Interactive Executive Web Dashboard (`app.py`):**
   - Built with **Streamlit** and **PyVis**, providing an interactive, dark-slate visual canvas where reviewers can filter by community, inspect individual ego-networks, and instantly spot glowing-red fraud rings.

---

## 📊 Real-World Implications & Impact

In the financial sector, graph-based analytics are transforming Anti-Money Laundering (AML) and fraud prevention:
* **Defeating Structuring & Layering:** Criminals split large illicit transactions into smaller sums across multiple accounts. Graph networks capture the *shape* of these flows rather than the absolute dollar amount.
* **Reducing False Positives:** By evaluating relational context, compliance teams can reduce alert fatigue caused by flagging isolated, high "risk looking" legitimate users.
* **Regulatory Compliance:** Financial institutions face strict penalties for failing to detect money laundering rings; graph topology provides auditable, visual proof of systemic risk identification.

---

## 🛠️ Tech Stack
* **Language:** Python 
* **Data Processing & Manipulation:** Pandas, DuckDB
* **Graph Mathematics & Algorithms:** NetworkX, Python-Louvain (`python-louvain`)
* **Interactive Visualization:** PyVis, Streamlit
