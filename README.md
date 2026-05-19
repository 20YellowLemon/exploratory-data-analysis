# 🏠 AirBnB Booking Analysis using Exploratory Data Analysis (EDA)

> A comprehensive Python code for analyzing AirBnB listing data through structured data cleaning, transformation, and visualization techniques.

---

1. [Project Overview](#1-project-overview)
2. [Features](#2-features)
3. [Prerequisites & Dependencies](#3-prerequisites-dependencies)
4. [Dataset](#4-dataset)
5. [Project Structures](#5-project-structure)
6. [License](#7-license)

---

## 1. Project Overview

This code performs **Exploratory Data Analysis (EDA)** on an AirBnB Open Dataset. Exploratory Data Analysis (EDA) is a critical first phase in any Data Science workflow — it uncovers patterns, detects anomalies, tests assumptions, and validates the quality of raw data before modeling or reporting.

---

## 2. Features

- ✅ Automated missing values detection and imputation.
- ✅ Currency string parsing (`$1,200` → `1200.0`).
- ✅ Datetime normalization for review timestamps.
- ✅ Duplicate record removal.
- ✅ Five publication-ready visualizations.
- ✅ Runs end-to-end in Google Colab with zero configuration.

---

## 3. Prerequisites & Dependencies

### Python Version

Python **3.7 or higher** is recommended.

### Installation

**For local environments:**
```bash
pip install pandas matplotlib seaborn
```

**For Google Colab:**
All three libraries come pre-installed. No additional setup is needed.

**For Conda environments:**
```bash
conda install pandas matplotlib seaborn
```

---

## 4. Dataset

### Source

The code uses the **AirBnB Open Data** dataset, a publicly available dataset commonly found on [Kaggle](https://www.kaggle.com/datasets/arianazmoudeh/airbnbopendata).

---

## 5. Project Structure

```
airbnb-eda/
│
├── airbnb_booking_analysis_using_exploratory_data_analysis_(eda).py
│         └── Main analysis script / notebook
│
├── Airbnb_Open_Data.csv          ← Dataset (not included; download separately)
│
└── README.md                     ← This documentation file
```

---

## 6. License

This project is released for educational and analytical use. The AirBnB Open Dataset is subject to its own terms on Kaggle — please review those before using the data in commercial applications.