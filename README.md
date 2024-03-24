# IoT Data Streaming powered by Apache Kafka and Databricks: Harnessing Windows Performance Monitor to Power BI Dashboards

![databricks-streaming-project drawio](https://github.com/FlorentineDev/IoT-powered-PerformanceMonitor/assets/16971296/34d111fe-1cb2-44e2-911c-d91af8d9c18d)

This IoT project is designed to provide hands-on experience with Spark Structured Streaming while developing a data pipeline for Internet-of-Things application. The project focuses on extracting computer performance metrics monitored by Windows Performance Monitor and employs a series of steps and technologies to enable visualization and dashboarding of this data through Power BI Client applications on any Internet-connected device.

Key Components:

\ **Microsoft Windows Performance Monitor** : The project initiates with the setup of Windows Performance Monitor to generate continuous performance data at 1-minute intervals.

![performancemonitor](https://github.com/FlorentineDev/IoT-powered-PerformanceMonitor/assets/16971296/9d9155c2-776f-43a1-bef8-1c68c720fea5)


\ **Python Script** : A custom Python script manages the produced CSV files, converts them into JSON strings, and transmit them to an Apache Kafka Server running on Confluent Cloud. Source files are in "Python Script" folder.

\ **Kafka Server on Confluent Cloud** : JSON-formatted performance data is published on a Kafka server hosted on Confluent Cloud, serving as the central hub for data dissemination.

![confluent 1](https://github.com/FlorentineDev/PerformanceMonitor_over_IoT/assets/16971296/84a954e7-fb27-484e-a6cc-fc30d88e90e8)

\ **Databricks** : A Databricks Spark cluster is established to consume data from the Kafka Server and continuously ingest data using Structured Streaming of Spark. PySpark (Python) is programmed on the cluster to execute multiple transformations, clean the received data, and load it into a table. This facilitates external software, such as Microsoft Power BI, to connect to the ckuster for data analysis. Source files are in "Databricks Script" folder.

\ **Microsoft Power BI** : The project integrates with Microsoft Power BI, allowing users to connect from their devices to the Databricks-generated table. Through Power BI, users can effortlessly create intuitive dashboards and conduct in-depth data analysis.

![power BI dashboard](https://github.com/FlorentineDev/IoT-powered-PerformanceMonitor/assets/16971296/f57416fb-a238-4e00-9117-f8c66e9acbe8)
![power BI dashboard2](https://github.com/FlorentineDev/IoT-powered-PerformanceMonitor/assets/16971296/b6d163d4-1181-49d0-92a8-6abfe7ed36f9)
