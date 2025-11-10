# 🧠 Distributed Machine Learning for Banking Analytics  
**End-to-End Big Data Pipeline using Hadoop, Hive, Spark, Spark ML, and Spark Streaming**

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![Apache Spark](https://img.shields.io/badge/Apache%20Spark-ML%20%26%20Streaming-orange?logo=apachespark)
![Hadoop](https://img.shields.io/badge/Hadoop-Data%20Storage%20%26%20Ingestion-yellow?logo=apache)
![Hive](https://img.shields.io/badge/Hive-Data%20Warehouse-brightgreen?logo=apachehive)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

---

## 🏁 Project Overview
This project demonstrates how **Distributed Machine Learning** can transform **banking data** into actionable insights using an integrated **Big Data ecosystem**.  
It simulates a **real-world banking analytics environment**, from **data ingestion and querying** to **predictive modeling** and **real-time data streaming**.

---

## 🎯 Objectives
| Objective | Description |
|------------|-------------|
| 🗄️ Data Analysis & Management | Use **Hadoop + Hive** to store and query large banking data. |
| 🔍 Exploratory Data Analysis | Perform distributed EDA with **Apache Spark** to uncover trends & anomalies. |
| 🤖 Predictive Modeling | Build ML models with **Spark MLlib** to predict client term deposit subscriptions. |
| ⚡ Real-Time Transaction Analysis | Stream and process simulated transactions using **Spark Structured Streaming**. |
| 🚀 Data Parallelism | Utilize distributed computing to enhance processing efficiency and scalability. |

---

## 🧩 Tech Stack

| Category | Tools/Frameworks |
|-----------|------------------|
| Distributed Storage | 🐘 **HDFS (Hadoop Distributed File System)** |
| Query Engine | 🐝 **Apache Hive / DuckDB (Simulation)** |
| Distributed Processing | 🔥 **Apache Spark (PySpark)** |
| Machine Learning | 🤖 **Spark MLlib (Logistic Regression, Decision Tree)** |
| Real-Time Streaming | ⚡ **Spark Structured Streaming** |
| Visualization | 📊 **Matplotlib, Pandas, Seaborn** |
| Environment | ☁️ **Google Colab (Cluster Simulation)** |

---
    +-----------------------------+
    |         bank.csv            |
    +-------------+---------------+
                  |
                  ▼
      [ Hadoop HDFS Storage ]
                  |
                  ▼
      [ Hive Data Warehouse ]
                  |
                  ▼
       [ Apache Spark for EDA & Aggregation ]
                  |
                  ▼
      [ Spark MLlib Model Training & Tuning ]
                  |
                  ▼
    [ Spark Structured Streaming for Real-Time ML ]
                  |
                  ▼
     [ Live Insights & Predictions ]


---

## 🧮 Dataset Information
**Dataset Name:** `bank.csv`  

| Column | Description |
|---------|--------------|
| age | Client age |
| job | Job type |
| marital | Marital status |
| education | Education level |
| default | Credit default |
| balance | Account balance |
| housing | Housing loan |
| loan | Personal loan |
| contact | Contact type |
| month | Last contact month |
| duration | Contact duration |
| poutcome | Previous campaign outcome |
| y | Subscription (target variable) |

---

## ⚙️ Workflow Summary

### 1️⃣ **Data Ingestion and Management**
- Uploaded `bank.csv` into **HDFS**.
- Created Hive database `banking_data` and table `client_info`.
- Queried average balance, default rate, and subscription trends.

### 2️⃣ **Exploratory Data Analysis (EDA) with Spark**
- Loaded data into **Spark DataFrame**.  
- Performed filtering, grouping, and visualization.  
- Derived new features: `quarter`, `age_group`, and `month_num`.

### 3️⃣ **Predictive Modeling (Spark MLlib)**
- Used **StringIndexer**, **OneHotEncoder**, and **VectorAssembler** for preprocessing.
- Built **Logistic Regression** & **Decision Tree Classifiers**.  
- Evaluated using **Accuracy**, **AUC**, and **CrossValidator** tuning.
- Extracted **feature importance** for interpretability.

### 4️⃣ **Real-Time Machine Learning (Spark Streaming)**
- Simulated live transaction data by chunking `bank.csv`.  
- Processed streams with **Structured Streaming**.  
- Applied trained model for **real-time predictions**.  
- Implemented **windowing & watermarking** for trend analysis and late data handling.

### 5️⃣ **Data Parallelism & Efficiency**
- Leveraged Spark’s distributed computing for scalability.
- Reduced computation time by parallelizing ETL and ML pipelines.

---

## 📊 Key Results & Insights

| Analysis | Insight |
|-----------|----------|
| 📈 Average Balance per Job | Management roles have the highest average balances. |
| 💍 Subscription Rate | Married & tertiary-educated clients are more likely to subscribe. |
| 🧠 Feature Importance | Duration, Poutcome, and Balance are top predictors. |
| ⚡ Real-Time Insights | Streaming pipeline detects trends by job and transaction frequency. |
| 🤖 Model Performance | Logistic Regression AUC ≈ 0.88, Accuracy ≈ 90%. |

---

## 🧠 Real-Time Streaming Example

![Streaming Output Example](https://user-images.githubusercontent.com/yourusername/streaming-demo.gif)

> *Spark Structured Streaming continuously updates job-level averages and predicts subscription likelihood for each new transaction in real-time.*


