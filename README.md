# Streaming IoT Data Processing with Databricks: Harnessing Windows Performance Monitor to Power BI Dashboards

![databricks-streaming-project drawio](https://github.com/FlorentineDev/IoT-powered-PerformanceMonitor/assets/16971296/34d111fe-1cb2-44e2-911c-d91af8d9c18d)

This IoT project is designed to provide hands-on experience with Spark Structured Streaming while developing a data pipeline for Internet-of-Things applications. The project focuses on leveraging computer performance metrics monitored by Windows Performance Monitor and employs a series of steps and technologies to enable visualization and dashboarding of this data through Power BI Client applications on any Internet-connected device.

Key Components:

\ Microsoft Windows Performance Monitor : The project initiates with the setup of Windows Performance Monitor to generate continuous performance data at 1-minute intervals.

\ Python Script : A custom Python script manages the produced CSV files, converts them into JSON strings, and transmit them to an Apache Kafka Server running on Confluent Cloud.

\ Kafka Server on Confluent Cloud : JSON-formatted performance data is published on a Kafka server hosted on Confluent Cloud, serving as the central hub for data dissemination.

\ Databricks : A Databricks Spark cluster is established to consume data from the Kafka Server and continuously ingest data using Structured Streaming of Spark. PySpark (Python) is programmed on the cluster to execute multiple transformations, clean the received data, and load it into a table. This facilitates external software, such as Microsoft Power BI, to connect to the ckuster for data analysis.

\ Microsoft Power BI : The project integrates with Microsoft Power BI, allowing users to connect from their devices to the Databricks-generated table. Through Power BI, users can effortlessly create intuitive dashboards and conduct in-depth data analysis.
