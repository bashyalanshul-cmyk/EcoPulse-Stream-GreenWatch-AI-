# 🌍 EcoPulse-Stream (GreenWatch AI)

[![Platform: Lovable](https://img.shields.io/badge/Platform-Lovable.app-7C3AED?style=flat-squared)](https://live-eco-watch.lovable.app/)
[![Language: Python](https://img.shields.io/badge/Language-Python-3776AB?style=flat-squared&logo=python&logoColor=white)](https://www.python.org/)
[![Framework: Polars](https://img.shields.io/badge/Data_Engine-Polars-F5BF45?style=flat-squared)](https://pola.rs/)
[![AI Framework: SHAP/XAI](https://img.shields.io/badge/AI-Explainable_AI_(XAI)-0052CC?style=flat-squared)](https://github.com/shap/shap)

### 🔗 **Live Interactive Deployment:** [EcoPulse-Stream Web Engine](https://live-eco-watch.lovable.app/)

---

## 🚀 Overview

**EcoPulse-Stream** (developed under the code name **GreenWatch AI**) is an advanced, real-time event-driven data streaming pipeline designed to dismantle corporate greenwashing and manual compliance bottlenecks. Moving away from traditional, static annual ESG reporting, this platform functions as an autonomous "watchdog" engine—continuously ingesting live supply chain telemetry, detecting environmental anomalies via machine learning, and utilizing **Explainable AI (XAI)** to transparently justify risk matrix assignments.

The system processes telemetry payloads through ultra-fast, multi-threaded pipelines, transforming unstructured log data into actionable risk matrices, automated dashboards, and diagnostic feature-importance plots.

---

## ⚡ Key Architectural Features

* **Event-Driven Telemetry Ingestion:** Engineered to process high-throughput, continuous streams of simulated IoT sensor logs and corporate operational JSON payloads.
* **Blazing-Fast Data Engineering via Polars:** Replaced conventional Pandas structures with a high-performance **Polars/Rust** backend to handle lazy evaluation, vectorization, and rapid real-time multi-threaded data filtering.
* **ML-Powered Anomaly Detection:** Implements automated machine learning (such as unsupervised Isolation Forests) to catch abrupt spikes in carbon equivalents, unauthorized supply chain route alterations, or sudden resource extraction irregularities.
* **Explainable AI (XAI) Transparency:** Integrates **SHAP (SHapley Additive exPlanations)** frameworks to mathematically dissect the model's outputs. It breaks open the "black box" of typical AI models by highlighting the exact feature weightings (e.g., a specific facility's sulfur dioxide threshold) that triggered an elevated risk tier.
* **Real-Time Analytical Interface:** Built with a highly responsive frontend deployed via Lovable to cleanly visualize dynamic data streams, rolling timeline trends, and interactive risk maps.

---

## 🛠️ Tech Stack & Dependencies

* **Data Engineering & Pipeline:** Python 3.11+, Polars (Rust-backed core), NumPy
* **Machine Learning & Analytics:** Scikit-Learn (Isolation Forest / Random Forest Regressor)
* **Explainable AI:** SHAP / LIME (Local Interpretable Model-agnostic Explanations)
* **Visualization Engine:** Matplotlib, Seaborn
* **Frontend Web Application Deployment:** Deployed natively via Lovable at [live-eco-watch.lovable.app](https://live-eco-watch.lovable.app/)

---

## 📐 Data Flow Pipeline

```text
[ Continuous Raw JSON Stream ] 
             │
             ▼
[ Polars DataFrame Transformation ] ──▶ (Lazy evaluation & multi-threaded cleaning)
             │
             ▼
[ Machine Learning Engine ] ──▶ (Isolation Forest analyzes multi-variable risk anomalies)
             │
             ▼
[ Explainable AI (SHAP Layer) ] ──▶ (Mathematical breakdown of feature importance scores)
             │
             ▼
[ Lovable UI / Interactive Engine ] ──▶ (Real-time live streaming dashboard and risk maps)
