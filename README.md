# 🚚 AI-Powered Delivery ETA Optimization

## Graph-Based Network Intelligence for Logistics

> An industry-grade **Machine Learning + Graph Analytics** system for predicting delivery ETAs, detecting bottleneck hubs, and optimizing logistics routes using Python, Scikit-learn, NetworkX, and Streamlit.

---

## 📌 Project Snapshot

| Component            | Details                              |
| -------------------- | ------------------------------------ |
| **Domain**           | Logistics and Supply Chain Analytics |
| **Dataset Size**     | 5,000 logistics records              |
| **Network Size**     | 20 hubs and 380 directed routes      |
| **Best Model**       | Gradient Boosting Regressor          |
| **Best Performance** | (R^2 \approx 0.988)                  |
| **Route Algorithm**  | Dijkstra’s Shortest-Path Algorithm   |
| **Dashboard**        | 9-page Streamlit application         |

---

## 📋 Table of Contents

1. [Project Overview](#-project-overview)
2. [Problem Statement](#-problem-statement)
3. [Core Capabilities](#-core-capabilities)
4. [System Architecture](#️-system-architecture)
5. [End-to-End Workflow](#-end-to-end-workflow)
6. [Features](#-features)
7. [Technology Stack](#️-technology-stack)
8. [Dataset](#-dataset)
9. [Machine-Learning Models](#-machine-learning-models)
10. [Graph Analytics](#️-graph-analytics)
11. [Route Optimization](#️-route-optimization)
12. [Dashboard Pages](#-dashboard-pages)
13. [Model Performance](#-model-performance)
14. [Setup and Installation](#️-setup-and-installation)
15. [Usage](#-usage)
16. [Future Improvements](#-future-improvements)

---

## 🎯 Project Overview

This project builds an intelligent logistics analytics system that combines machine learning, graph analytics, route optimization, and interactive visualization.

The system is designed to:

* **Predict delivery ETA** using multiple regression models
* **Detect bottleneck hubs** through graph-centrality analysis
* **Model logistics operations** as a weighted directed network
* **Optimize delivery routes** for speed, safety, and distance
* **Generate actionable business insights** from ML and graph outputs
* **Visualize operational intelligence** through a nine-page Streamlit dashboard

Rather than only predicting delivery time, the project also helps identify where delays originate and how logistics operations can be improved.

---

## 🚧 Problem Statement

Delivery time depends on much more than route distance.

Real-world logistics operations are affected by:

* Traffic congestion
* Weather conditions
* Hub utilization
* Shipment priority
* Route type
* Intermediate stops
* Historical delays
* Network bottlenecks

A conventional ETA model may estimate how long a delivery will take, but it does not necessarily explain:

* Which hub is causing the delay
* Which route is operationally risky
* Whether an alternative route is available
* Whether the shortest route is also the fastest or safest

This project addresses these limitations by integrating predictive machine learning with graph-based network intelligence.

---

## 🧠 Core Capabilities

### 1. Delivery ETA Prediction

The system predicts delivery time using:

* Linear Regression
* Random Forest Regressor
* Gradient Boosting Regressor

The best-performing model achieves approximately:

[
R^2 = 0.988
]

---

### 2. Bottleneck Hub Detection

The logistics network is analyzed using:

* Betweenness Centrality
* Closeness Centrality
* Degree Centrality
* Composite Bottleneck Score

These metrics identify hubs that are highly connected, frequently used, overloaded, or responsible for delay propagation.

---

### 3. Graph-Based Network Modelling

The logistics network is represented as a weighted directed graph using NetworkX.

* **Nodes** represent logistics hubs
* **Edges** represent delivery routes
* **Edge weights** represent distance, travel time, congestion, delay, or risk

The final network contains:

* **20 logistics hubs**
* **380 directed delivery routes**

---

### 4. Multi-Objective Route Optimization

Using Dijkstra’s shortest-path algorithm, the system compares:

* **Fastest route**
* **Safest route**
* **Shortest route**

This allows users to select a route according to different operational priorities.

---

### 5. Automated Business Insights

The platform generates more than eight actionable recommendations by combining model predictions, route performance, hub load, and graph-centrality results.

---

### 6. Interactive Dashboard

The complete solution is integrated into a nine-page Streamlit dashboard for data exploration, prediction, network visualization, model comparison, and decision support.

---

## 🏗️ System Architecture

```text
Raw Logistics Data
      5,000 Rows
          │
          ▼
┌───────────────────────────────┐
│     PREPROCESSING PIPELINE    │
│                               │
│  Deduplicate                  │
│  Impute Missing Values        │
│  Engineer Features            │
│  Encode Categories            │
│  Normalize Variables          │
└───────────────┬───────────────┘
                │
        ┌───────┴────────┐
        │                │
        ▼                ▼
┌───────────────┐  ┌──────────────────┐
│  ML PIPELINE  │  │  GRAPH PIPELINE  │
│               │  │                  │
│ Linear Reg.   │  │ Build DiGraph    │
│ Random Forest │  │ Centrality       │
│ Gradient Boost│  │ Bottlenecks      │
│ Evaluation    │  │ Dijkstra Routing │
└───────┬───────┘  └─────────┬────────┘
        │                     │
        └──────────┬──────────┘
                   ▼
        ┌──────────────────────┐
        │  STREAMLIT DASHBOARD │
        │                      │
        │ Predictions          │
        │ Network Analysis     │
        │ Route Optimization   │
        │ Business Insights    │
        └──────────────────────┘
```

---

## 🔄 End-to-End Workflow

```text
Data Collection
      ↓
Data Cleaning and Validation
      ↓
Feature Engineering
      ↓
Categorical Encoding and Normalization
      ↓
ML Model Training and Evaluation
      ↓
Directed Graph Construction
      ↓
Centrality and Bottleneck Analysis
      ↓
Route Optimization
      ↓
Business Insight Generation
      ↓
Streamlit Dashboard
```

---

## ✨ Features

| Feature                      | Description                                                                 |
| ---------------------------- | --------------------------------------------------------------------------- |
| 📦 **Data Pipeline**         | Deduplication, imputation, feature engineering, encoding, and normalization |
| 🤖 **ETA Prediction**        | Three regression models with (R^2 \approx 0.99) on the best model           |
| 🕸️ **Graph Analytics**      | 20-node and 380-edge directed logistics network                             |
| 🔍 **Bottleneck Detection**  | Centrality metrics combined with a composite bottleneck score               |
| 🗺️ **Route Optimization**   | Fastest, safest, and shortest path comparison                               |
| 💡 **Business Insights**     | More than eight automatically generated operational recommendations         |
| 📊 **Interactive Dashboard** | Nine-page Streamlit application                                             |
| 📈 **Model Comparison**      | MAE, RMSE, and (R^2) evaluation across all models                           |

---

## 🛠️ Technology Stack

| Category                            | Technologies                                        |
| ----------------------------------- | --------------------------------------------------- |
| **Programming Language**            | Python                                              |
| **Data Processing**                 | `pandas`, `numpy`                                   |
| **Machine Learning**                | `scikit-learn`                                      |
| **Regression Models**               | Linear Regression, Random Forest, Gradient Boosting |
| **Graph Analytics**                 | `networkx`                                          |
| **Graph Structure**                 | Directed Graph, Dijkstra, Centrality                |
| **Visualization**                   | `matplotlib`, `seaborn`                             |
| **Dashboard**                       | `streamlit`                                         |
| **Scientific Utilities**            | `scipy`                                             |
| **Model Storage**                   | `pickle`                                            |
| **Configuration and Data Exchange** | `json`                                              |

---

## 📊 Dataset

The project uses a real-world **Delhivery logistics dataset** mapped across 20 major Indian logistics hubs.

### Dataset Size

[
N = 5{,}000 \text{ logistics records}
]

### Core Columns

| Column              | Description                                                   |
| ------------------- | ------------------------------------------------------------- |
| `source_hub`        | Origin city or warehouse mapped from the raw source name      |
| `destination_hub`   | Delivery destination mapped from the raw destination name     |
| `route_distance`    | Route distance in kilometres                                  |
| `traffic_level`     | Traffic congestion factor based on OSRM travel times          |
| `weather_condition` | Weather condition assigned using temporal monsoon patterns    |
| `num_stops`         | Number of intermediate delivery stops                         |
| `hub_load`          | Hub-capacity utilization factor                               |
| `shipment_priority` | Economy, Standard, Express, or Same-Day                       |
| `delay_minutes`     | Actual delay compared with OSRM travel time                   |
| `delivery_time_hrs` | Target variable representing actual trip travel time in hours |

### Engineered Features

The preprocessing pipeline creates additional logistics and operational variables, including:

* `congestion_score`
* `weather_risk`
* `avg_delay_per_route`
* `est_travel_hrs`
* `is_peak_hour`
* `is_weekend`

These features help capture operational effects that may not be represented by raw distance alone.

---

## 🤖 Machine-Learning Models

Three regression models were trained and compared.

### Linear Regression

Used as an interpretable baseline for understanding linear relationships between logistics features and delivery time.

### Random Forest Regressor

Used to model nonlinear relationships and feature interactions across route, traffic, hub, and shipment variables.

### Gradient Boosting Regressor

Used to sequentially reduce prediction errors and produce the strongest overall model performance.

---

## 🕸️ Graph Analytics

The delivery network is represented as:

[
G = (V,E)
]

where:

* (V) is the set of logistics hubs
* (E) is the set of directed delivery routes

Each route can contain attributes such as:

* Distance
* Travel time
* Delay
* Traffic congestion
* Weather risk
* Route-risk score

### Centrality Measures

#### Degree Centrality

Measures how strongly connected a hub is within the logistics network.

[
C_D(v)=\frac{\deg(v)}{|V|-1}
]

#### Closeness Centrality

Measures how efficiently a hub can reach other hubs.

[
C_C(v)=\frac{|V|-1}{\sum_{u\neq v}d(v,u)}
]

#### Betweenness Centrality

Measures how frequently a hub lies on shortest paths between other logistics hubs.

[
C_B(v)=
\sum_{s\neq v\neq t}
\frac{\sigma_{st}(v)}{\sigma_{st}}
]

These measures are combined with operational variables to produce a composite bottleneck score.

---

## 🗺️ Route Optimization

The platform applies Dijkstra’s shortest-path algorithm to compare multiple routing strategies.

### Shortest Route

Finds the route with minimum total distance.

[
P_{\text{shortest}}
===================

\arg\min_P
\sum_{e\in P}\text{distance}(e)
]

### Fastest Route

Finds the route with minimum predicted travel time.

[
P_{\text{fastest}}
==================

\arg\min_P
\sum_{e\in P}\text{travel time}(e)
]

### Safest Route

Finds the route with minimum operational risk.

[
P_{\text{safest}}
=================

\arg\min_P
\sum_{e\in P}\text{risk}(e)
]

The route objective is selected by changing the edge-weight attribute used by the graph algorithm.

---

## 📱 Dashboard Pages

The Streamlit dashboard contains nine pages.

| Page                       | Purpose                                                               |
| -------------------------- | --------------------------------------------------------------------- |
| 🏠 **Home**                | KPI cards, project overview, architecture, and technology stack       |
| 📊 **Dataset Overview**    | Data samples, descriptive statistics, and distribution visualizations |
| 🔮 **ETA Prediction**      | Interactive shipment form with real-time ETA prediction               |
| 🕸️ **Graph Network**      | Delivery-network visualization and route highlighting                 |
| 🔍 **Bottleneck Analysis** | Centrality rankings, bottleneck subgraphs, and risky routes           |
| 🗺️ **Route Optimizer**    | Comparison of fastest, safest, and shortest routes                    |
| 💡 **Business Insights**   | Automatically generated operational recommendations                   |
| 📈 **Model Performance**   | MAE, RMSE, (R^2), actual-vs-predicted plots, and feature importance   |
| 🏁 **Conclusion**          | Achievements, deployment notes, and future improvements               |

---

## 📈 Model Performance

| Model                 | MAE (hrs) | RMSE (hrs) |      (R^2) |
| --------------------- | --------: | ---------: | ---------: |
| Linear Regression     |     ~8.13 |     ~11.62 |     ~0.904 |
| Random Forest         |     ~3.45 |      ~5.62 |     ~0.978 |
| **Gradient Boosting** | **~2.23** |  **~4.09** | **~0.988** |

### Best Model

The Gradient Boosting Regressor achieved the strongest performance:

[
MAE \approx 2.23 \text{ hours}
]

[
RMSE \approx 4.09 \text{ hours}
]

[
R^2 \approx 0.988
]

---

## ⚙️ Setup and Installation

### 1. Clone or Download the Project

```bash
cd delivery_eta
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the Complete Pipeline

This command preprocesses the data, engineers features, trains the models, builds the graph, and stores the required outputs.

```bash
python main.py
```

### 4. Launch the Streamlit Dashboard

```bash
streamlit run src/dashboard/app.py
```

---

## 🚀 Usage

### Run the Complete Pipeline

```bash
python main.py
```

### Launch the Dashboard

```bash
streamlit run src/dashboard/app.py
```

### Predict ETA Programmatically

```python
from src.models.predict import load_best_model, build_feature_row

model, name, _ = load_best_model()

X = build_feature_row(
    distance=500,
    traffic=0.6,
    hub_load=0.5,
    stops=2,
    weather="Rain",
    priority="Express",
    route_type="Highway"
)

eta_hrs = model.predict(X)[0]

print(f"Predicted ETA: {eta_hrs:.2f} hrs")
```

---

## 📁 Recommended Project Structure

```text
delivery_eta/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── src/
│   ├── preprocessing/
│   ├── models/
│   ├── graph/
│   ├── insights/
│   └── dashboard/
│       └── app.py
│
├── main.py
├── requirements.txt
├── Dockerfile
└── README.md
```

---

## 💡 Business Value

The platform helps logistics teams answer critical operational questions:

* What is the predicted delivery time?
* Which hubs are creating bottlenecks?
* Which routes are consistently delayed?
* Is the shortest route also the fastest?
* Which alternative path has lower operational risk?
* Where should logistics capacity be increased?
* Which shipments are most likely to face delays?

By combining ML predictions with graph intelligence, the project converts raw logistics data into actionable operational decisions.

---

## 🔭 Future Improvements

### Real-Time Data Integration

* Live Delhivery or FedEx logistics APIs
* Real-time traffic information
* Live weather data
* Dynamic hub-capacity updates

### Advanced Geographic Visualization

* Folium
* Kepler.gl
* GeoPandas
* Real hub latitude and longitude coordinates

### Predictive Enhancements

* Time-series delay forecasting
* Prophet-based forecasting
* LSTM models
* Temporal forecasting models
* SLA breach prediction

### Network Intelligence

* Real-time dynamic rerouting
* Graph Neural Network embeddings
* Delay-propagation modelling
* Network disruption detection

### Cloud and Deployment

* AWS deployment
* Google Cloud Platform deployment
* Docker-based deployment
* Scalable production APIs

### Automated Alerts

* Email notifications
* SMS notifications
* SLA breach alerts
* Hub overload alerts
* High-risk route warnings

---

## 🏁 Conclusion

AI-Powered Delivery ETA Optimization combines machine learning, graph analytics, and interactive visualization into a complete logistics decision-support system.

The project provides:

* Accurate delivery ETA prediction
* Bottleneck hub detection
* Multi-objective route optimization
* Graph-based network intelligence
* Automated business recommendations
* Interactive operational dashboards

The system demonstrates how predictive analytics and network science can work together to improve logistics visibility, route planning, and supply-chain efficiency.

---

> Built as an industry-grade capstone project in **Machine Learning, Graph Analytics, and Logistics Optimization**.
