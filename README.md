# **WiFi Signal Latency Analysis**

This project analyzes the main factors that affect Wi-Fi latency. The goal is to understand which network, signal, and environmental conditions have the strongest relationship with latency, and to rank these features using a custom Mutual Information (MI) implementation.

The work includes preprocessing, exploratory data analysis (EDA), feature engineering, visualization, and MI-based feature ranking. The whole analysis is implemented in the notebook `notebooks/wifi_latency_analysis.ipynb`.

## **Dataset**

The dataset is stored in **`data/wifi_latency.csv`**.
It was collected from the traffic of a **public Wi-Fi network**, and each row represents a **two-minute network flow**.

### **Main Features**

| Feature             | Type        | Description                                       |
| ------------------- | ----------- | ------------------------------------------------- |
| `latency_ms`        | numeric     | Network latency in milliseconds                   |
| `rssi_dbm`          | numeric     | Signal strength received by the device (dBm)      |
| `snr_db`            | numeric     | Signal-to-noise ratio                             |
| `band`              | categorical | Wi-Fi frequency band (e.g., 2.4 GHz / 5 GHz)      |
| `channel_util`      | numeric     | Channel utilization percentage                    |
| `num_assoc_devices` | numeric     | Number of devices connected to the access point   |
| `client_speed_mbps` | numeric     | Client device speed in Mbps                       |
| `ap_vendor`         | categorical | Access point vendor                               |
| `protocol`          | categorical | Wi-Fi protocol (e.g., 802.11n)                    |
| `distance_m`        | numeric     | Distance between client and access point (meters) |

The dataset includes both numerical and categorical features, which makes it suitable for studying how different factors influence Wi-Fi latency.

## **Project Structure**

```
WiFi-Signal-Latency-Analysis/
│
├── notebooks/
│   └── wifi_latency_analysis.ipynb
│
├── data/
│   └── wifi_latency.csv
│
├── results/
│   ├── correlation_heatmap.png
│   ├── mi_heatmap.png
│   ├── latency_hist_before.png
│   ├── latency_hist_after.png
│   ├── latency_log_hist.png
│   └── latency_boxplot.png
│
└── README.md
```

## **Analysis Steps**
