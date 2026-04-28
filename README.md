# **Real-Time Cryptocurrency Data Streaming & Analysis**

A robust big data pipeline designed to simulate, process, and analyze high-frequency Bitcoin market data in real-time. This project leverages a contemporary dataset (January 2023 – October 2025\) to provide institutional-grade financial analytics.

## **System Architecture**

The system is built on a scalable big data architecture to handle high-velocity market data:

* **Data Ingestion**: High-resolution historical Bitcoin data is streamed through **Apache Kafka** to simulate a live market environment.

* **Stream Processing**: **Apache Spark Structured Streaming** consumes the Kafka topics to perform real-time transformations and anomaly detection.

* **Storage**: Historical baselines and processed results are managed using **Parquet** for optimized read/write performance.

##  **Key Features**

* **Real-Time Anomaly Detection**:  
  * **Price Drop Alert**: Detects rapid volatility where price changes exceed 0.1%.

  * **Volume Spike Detection**: Identifies unusual market activity by flagging volume data that exceeds 3 standard deviations from the historical mean.

* **Strategy Simulation**: Simulates "Flash Crash" and volume-based trading strategies to evaluate entry efficiency and portfolio growth.

* **Data Verification**: Ensures 100% data consistency and high throughput during the transition from historical batch data to real-time streams.

## **Tech Stack**

* **Language**: Python (PySpark)

* **Streaming**: Apache Kafka 3.5.0

* **Analytics**: Apache Spark 3.5.0

* **Environment**: Java 8, Google Colab

## **Methodology**

1. **Environment Setup**: Initialization of Java, Kafka, and Zookeeper background processes within a Colab environment.

2. **Historical Baseline**: Analyzing over 2 years of modern BTC data to establish standard deviation thresholds for volume anomalies.

3. **Kafka Production**: Ingesting 25,000+ rows of market data into the btc\_trades topic to simulate live traffic.

4. **Streaming Analytics**: Real-time parsing of JSON data from Kafka into a structured schema for immediate analysis.

## **Author & Contributions**

This project was completed for **MBAI5110G \- Big Data Analytics** at Ontario Tech University.

**Primary Developer**: Scott Hodgins

* Designed and implemented the full Spark-Kafka integration.

* Authored the real-time anomaly detection logic and data ingestion scripts.

* Conducted historical Parquet data analysis for baseline thresholding.

**Group Members**: Joy Harrison, Ali Abughamja, Jasmeet Singh.

