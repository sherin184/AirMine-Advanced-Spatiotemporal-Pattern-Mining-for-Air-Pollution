# 🌍 AirMine — Advanced Spatiotemporal Pattern Mining for Air Pollution

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![FastAPI](https://img.shields.io/badge/FastAPI-0.104-green.svg)
![React](https://img.shields.io/badge/React-18-61dafb.svg)
![TypeScript](https://img.shields.io/badge/TypeScript-5-3178c6.svg)

## 📌 Project Overview

AirMine is an advanced environmental analytics platform designed to analyze air pollution data using data mining and machine learning techniques.

The system identifies pollution patterns, detects unusual pollution events, performs temporal clustering, analyzes spatial pollution distributions, and evaluates environmental risks.

It provides an interactive dashboard that allows users to upload datasets, explore air quality information, visualize pollution trends, and generate analytical reports.

## ✨ Features

| Feature | Description |
|---|---|
| 📊 Overview Dashboard | Displays key performance indicators, pollutant trends, and risk distribution. |
| 🌬️ Air Quality Explorer | Interactive data exploration with filters and charts. |
| 🔬 Temporal Clustering | K-Means clustering with elbow method and silhouette scoring. |
| 🗺️ Spatial Analysis | Interactive pollution maps and hotspot detection. |
| ⚠️ Anomaly Detection | Isolation Forest algorithm for identifying unusual pollution patterns. |
| 🛡️ Risk Profiling | EPA AQI-based environmental risk assessment. |
| 📈 Correlation Analysis | Pearson correlation matrix with significance testing. |
| 📁 Dataset Management | CSV upload, column mapping, and data cleaning. |
| 📋 Reports | Downloadable PDF and CSV analytical reports. |

## 🧠 Algorithms Used

### 1. K-Means Clustering
- Groups air quality observations into clusters.
- Uses StandardScaler for data normalization.
- Applies the Elbow Method to identify suitable cluster counts.
- Uses Silhouette Score to evaluate clustering quality.

### 2. Isolation Forest
- Detects unusual pollution observations.
- Supports configurable contamination levels.
- Uses 150 estimators.
- Generates anomaly scores using the decision function.

### 3. Environmental Risk Profiling
- Uses EPA Air Quality Index (AQI) breakpoint calculations.
- Calculates individual pollutant sub-indices.
- Aggregates pollutant risk levels.
- Provides environmental recommendations.

### 4. Pearson Correlation Analysis
- Calculates relationships between pollutants.
- Generates correlation matrices.
- Performs statistical significance testing.
- Identifies significant pollutant relationships.

## 🛠️ Technology Stack

| Component | Technologies |
|---|---|
| Frontend | React 18, TypeScript, Vite |
| Styling | Tailwind CSS |
| Backend | Python, FastAPI |
| Database | SQLite, SQLAlchemy |
| Machine Learning | Scikit-learn |
| Data Processing | Pandas, NumPy, SciPy |
| Visualization | Recharts |
| Maps | Leaflet, React Leaflet |
| Reports | FPDF2 |

## 📂 Project Structure

```text
data_mining/
│
├── backend/
│   ├── main.py
│   ├── database.py
│   ├── models.py
│   ├── schemas.py
│   │
│   ├── routers/
│   │   ├── anomaly.py
│   │   ├── clustering.py
│   │   ├── correlation.py
│   │   ├── datasets.py
│   │   ├── explorer.py
│   │   ├── overview.py
│   │   ├── reports.py
│   │   ├── risk.py
│   │   └── spatial.py
│   │
│   ├── services/
│   │   ├── anomaly_service.py
│   │   ├── clustering_service.py
│   │   ├── correlation_service.py
│   │   ├── data_cleaning.py
│   │   ├── report_service.py
│   │   ├── risk_service.py
│   │   └── spatial_service.py
│   │
│   ├── sample_data/
│   ├── uploads/
│   ├── tests/
│   └── requirements.txt
│
├── frontend/
│   ├── src/
│   │   ├── api/
│   │   ├── components/
│   │   ├── hooks/
│   │   ├── pages/
│   │   └── types/
│   │
│   ├── package.json
│   ├── vite.config.ts
│   └── tailwind.config.js
│
├── start.bat
└── README.md
```

## ⚙️ Installation and Setup

### Prerequisites

Install the following before running the project:

- Python 3.10 or above
- Node.js 18 or above
- npm
- Git (optional)

### 1. Clone the Repository

```bash
git clone <YOUR_REPOSITORY_URL>
cd data_mining
```

### 2. Install Backend Dependencies

```bash
cd backend
pip install -r requirements.txt
```

### 3. Generate Sample Dataset

```bash
python sample_data/generate_sample.py
```

The project includes a synthetic air quality dataset for demonstration and testing.

### 4. Start Backend Server

```bash
uvicorn main:app --reload --port 8000
```

Backend URL:

http://localhost:8000

API Documentation:

http://localhost:8000/docs

### 5. Install Frontend Dependencies

Open another terminal:

```bash
cd frontend
npm install
```

### 6. Start Frontend

```bash
npm run dev
```

Frontend URL:

http://localhost:5173

## 🚀 Quick Start (Windows)

The project includes a Windows batch file to automate setup and execution.

From the project root, execute:

```bat
start.bat
```

This automatically:

1. Checks Python and Node.js installations.
2. Installs backend dependencies.
3. Installs frontend dependencies.
4. Generates sample data when required.
5. Starts the FastAPI backend.
6. Starts the React frontend.
7. Opens the dashboard in the browser.

## 🔌 API Documentation

The backend provides REST API endpoints for different analytical operations.

| Module | API Prefix |
|---|---|
| Dataset Management | `/api/v1/datasets` |
| Overview Dashboard | `/api/v1/overview` |
| Data Explorer | `/api/v1/explorer` |
| Clustering | `/api/v1/clustering` |
| Anomaly Detection | `/api/v1/anomaly` |
| Spatial Analysis | `/api/v1/spatial` |
| Risk Profiling | `/api/v1/risk` |
| Correlation Analysis | `/api/v1/correlation` |
| Reports | `/api/v1/reports` |

Interactive API documentation is available at:

http://localhost:8000/docs

## 🧪 Testing

The project includes backend tests for anomaly detection and clustering.

Run the tests using:

```bash
cd backend
python -m pytest tests/ -v
```

## 📊 Sample Dataset

The project includes a synthetic air quality dataset:

```text
backend/sample_data/synthetic_air_quality.csv
```

The platform also supports uploading external CSV datasets.

The column mapping functionality helps users map different CSV column names to the expected air quality fields.

**Note:** Synthetic data is intended for demonstration purposes and should not be treated as actual environmental monitoring data.

## 🎯 Project Objectives

- Analyze air pollution patterns using data mining techniques.
- Identify abnormal pollution levels through anomaly detection.
- Discover temporal patterns using clustering.
- Visualize pollution distribution using spatial analysis.
- Evaluate environmental risks using AQI calculations.
- Explore relationships between different air pollutants.
- Generate meaningful analytical reports through an interactive dashboard.

## ⚠️ Important Notes

- The included sample dataset is synthetic.
- Analysis results are generated through actual algorithm execution.
- Missing timestamps and geographic coordinates are handled where supported by the application.
- Users can upload datasets with different column names using column mapping.
- Results depend on the quality and completeness of the uploaded data.

## 📄 License

This project is developed for academic and educational purposes.
