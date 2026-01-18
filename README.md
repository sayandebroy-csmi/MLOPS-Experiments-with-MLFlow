# MLOPS-Experiments-with-MLFlow

A complete demonstration of performing ML experiment tracking using MLflow. This repository showcases various MLflow features including local/remote tracking, autologging, hyperparameter tuning, and model versioning.

## 📋 Table of Contents

- [Features](#features)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Experiments](#experiments)
- [Dependencies](#dependencies)

## ✨ Features

- **Local Experiment Tracking** - Track experiments on your local MLflow server
- **Remote Experiment Tracking** - Track experiments using DagsHub as remote MLflow server
- **Autologging** - Automatic logging of parameters, metrics, and models
- **Hyperparameter Tuning** - GridSearchCV with nested MLflow runs
- **Model Logging** - Log and version scikit-learn models
- **Artifact Logging** - Log plots, source code, and other artifacts
- **Data Logging** - Log training and testing datasets

## 📁 Project Structure

```
├── src/
│   ├── runs_local.py              # Local MLflow tracking example (Wine dataset)
│   ├── runs_remote.py             # Remote MLflow tracking with DagsHub
│   ├── autolog.py                 # MLflow autologging example
│   ├── hyper_parameter_tuning_1.py # Hyperparameter tuning with nested runs
│   └── artifacts/                 # Generated artifacts (plots, etc.)
├── mlartifacts/                   # MLflow artifact storage
├── requirements.txt               # Project dependencies
└── README.md
```

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/sayandebroy-csmi/MLOPS-Experiments-with-MLFlow.git
   cd MLOPS-Experiments-with-MLFlow
   ```

2. **Create a virtual environment** (recommended)
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

## 💻 Usage

### Start the MLflow UI (Local Tracking)

```bash
cd src
mlflow ui
```

Access the MLflow UI at `http://127.0.0.1:5000`

### Run Experiments

```bash
# Local experiment tracking
python src/runs_local.py

# Remote experiment tracking (DagsHub)
python src/runs_remote.py

# Autologging example
python src/autolog.py

# Hyperparameter tuning
python src/hyper_parameter_tuning_1.py
```

## 🧪 Experiments

### 1. Local Tracking (`runs_local.py`)
- **Dataset**: Wine Classification
- **Model**: Random Forest Classifier
- **Features**: Manual logging of params, metrics, confusion matrix, and model

### 2. Remote Tracking (`runs_remote.py`)
- **Dataset**: Wine Classification
- **Model**: Random Forest Classifier
- **Features**: Remote tracking using DagsHub integration

### 3. Autologging (`autolog.py`)
- **Dataset**: Wine Classification
- **Model**: Random Forest Classifier
- **Features**: Automatic parameter and metric logging with `mlflow.autolog()`

### 4. Hyperparameter Tuning (`hyper_parameter_tuning_1.py`)
- **Dataset**: Breast Cancer Classification
- **Model**: Random Forest Classifier
- **Features**: 
  - GridSearchCV with nested MLflow runs
  - Logging all hyperparameter combinations as child runs
  - Data logging (training/testing datasets)
  - Best model logging

## 📦 Dependencies

| Package | Version |
|---------|---------|
| mlflow | 3.8.1 |
| scikit-learn | 1.7.2 |
| matplotlib | 3.10.8 |
| seaborn | 0.13.2 |
| dagshub | 0.6.4 |

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

**Sayan Deb Roy**

---

⭐ Star this repository if you find it helpful!
