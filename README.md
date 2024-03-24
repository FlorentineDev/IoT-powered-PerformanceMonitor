# IoT Project: Host Performance Analysis powered by Databricks and Kafka

![databricks-streaming-project drawio](https://github.com/FlorentineDev/IoT-powered-PerformanceMonitor/assets/16971296/34d111fe-1cb2-44e2-911c-d91af8d9c18d)

This IoT project aims to familiarize with Spark Structured Streaming and to develop from scratch a data pipeline for Internet-of-Things application.
Developed application takes Computer Performances monitored from Windows Performance Monitor and, through multiple steps and technologies, allows Power BI Client applications on any Internet-connected machine to visualize and dashabord these data.

Key Components:

Microsoft Windows Performance Monitor : The project begins with the setup of Windows Performance Monitor to generate continuous performance data at 1-minute intervals.

Python Script Management: A custom Python script efficiently manages the produced CSV files, converts them into JSON strings and send them to a Apache Kafka Server running on Confluent Cloud in a specific topic.

Kafka Server on Confluent Cloud: JSON-formatted performance data is published on a Kafka server hosted on Confluent Cloud, serving as the central hub for data dissemination.

Databricks: Databricks Spark cluster is established to consume data from Kafka Server and ingest data continously using Structured Streaming of Spark. Once data is ingested, PySpark (Python) is programmed on the Cluster to make multiple trasnformations, clean the received data and load into a Table. This allow external software (e.g., Microsofoft Power BI)
The pipeline ensures data cleansing and transformation, resulting in a refined dataset ready for analysis.

Microsoft Power BI: The project integrates with Microsoft Power BI, enabling users to connect from their devices to the Databricks-generated table. Through Power BI, users can create intuitive dashboards and conduct detailed data analysis.
