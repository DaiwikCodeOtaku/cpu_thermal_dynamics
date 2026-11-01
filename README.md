# CPU Thermal Profiling & Temperature Prediction

A data-driven study of CPU thermal behavior using **exploratory data analysis, thermal dynamics modeling, numerical methods, and machine learning**.

## Overview

CPU temperature varies with workload, utilization, power consumption, and system conditions. This project analyzes real CPU/system monitoring data to understand these thermal patterns and explores methods for predicting **next-step CPU temperature**.

The project combines a physics-inspired thermal model with numerical methods and machine learning approaches.

## Objectives

- Analyze CPU temperature and system-performance metrics
- Understand relationships between workload and thermal behavior
- Model CPU temperature using a simplified thermal dynamics equation
- Implement numerical methods such as **Euler** and **Runge-Kutta (RK4)**
- Compare physics-inspired predictions with machine learning baselines
- Evaluate prediction performance using standard regression metrics

## Dataset

The dataset contains CPU/system monitoring measurements collected over time.

Important features include measurements related to:

- CPU temperature
- CPU utilization
- Power/system metrics
- Time-series system behavior

> The dataset is used for experimentation and educational analysis of CPU thermal behavior.

## Methodology

### 1. Exploratory Data Analysis

The project begins by examining:

- Temperature distributions
- CPU utilization patterns
- Correlations between system metrics
- Temperature variation over time
- Relationships between workload and thermal response

### 2. Thermal Dynamics Model

A simplified thermal model is used to represent the change in CPU temperature over time.

The model captures the basic intuition that:

- Higher workload/power can increase temperature
- Heat dissipation causes temperature to move toward an equilibrium
- The rate of temperature change depends on the current thermal state

### 3. Numerical Methods

The thermal model is solved numerically using:

**Euler Method**

A simple first-order numerical integration method used to estimate the next temperature state.

**Runge-Kutta 4th Order (RK4)**

A higher-order numerical integration method used to obtain more accurate estimates of the thermal dynamics.

### 4. Machine Learning Baselines

Machine learning regression models are used as comparison points.

Current experiments include:

- Linear Regression
- Random Forest Regression

This allows the project to compare a physics-inspired approach against conventional data-driven models.

## Evaluation

Model performance is evaluated using:

- **MAE** — Mean Absolute Error
- **RMSE** — Root Mean Squared Error
- **R² Score** — Coefficient of Determination

The evaluation uses chronological data splitting where appropriate to better reflect the time-series nature of CPU measurements.

## Project Structure

```text
cpu-thermal-profiling/
│
├── README.md
├── CPU_Thermal_Dynamics.ipynb
├── Computer_metrics.csv
└── requirements.txt
```

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/DaiwikCodeOtaku/cpu-thermal-profiling.git
cd cpu-thermal-profiling
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the notebook

```bash
jupyter notebook CPU_Thermal_Dynamics.ipynb
```

You can also open the notebook directly using J