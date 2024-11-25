Overview

The objective of this project is to generate synthetic time-series data representing various system performance metrics such as cpu_temperature, cpu_usage, memory_usage, and others, and then apply anomaly detection methods to identify unusual patterns in the data.

Features of the Data:

cpu_temperature: The CPU temperature of the system.
cpu_usage: The percentage of CPU used by processes.
cpu_load: The CPU load of the system.
memory_usage: The percentage of memory being used.
battery_level: The battery charge level of the system.
cpu_power: The power usage of the CPU.

Data Generation

The dataset consists of 6000 time-series data points, generated with random values for each of the system performance features. The data spans several timestamps with the following columns:

timestamp
cpu_temperature
cpu_usage
cpu_load
memory_usage
battery_level
cpu_power
The synthetic data is saved in a CSV file named synthetic_time_series.csv.

Anomaly Detection

Two anomaly detection techniques were applied to the synthetic dataset:

1. Percentile Method
The percentile method flags values outside a specified range of percentiles as anomalies.
Anomalies were detected based on thresholds for each feature, and data points outside this range were considered anomalies.

2. Isolation Forest Method
Isolation Forest is an unsupervised learning algorithm that identifies anomalies based on how isolated the data points are in a random forest.
The method was applied with default settings and flagged extreme outliers as anomalies.

Results

Correlation Matrix
The correlation matrix was computed between the features cpu_temperature, cpu_usage, and memory_usage. The results showed low correlations between the features:

cpu_temperature & cpu_usage: 0.14
cpu_temperature & memory_usage: 0.14
cpu_usage & memory_usage: 0.12
Detected Anomalies:
Percentile Method: Detected 1800 anomalies.
Isolation Forest Method: Detected 300 anomalies.
