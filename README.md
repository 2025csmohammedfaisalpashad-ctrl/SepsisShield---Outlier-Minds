# SepsisShield — Outlier Minds 🏥

### Explainable Early-Warning Research for Sepsis Risk in ICU Patients

SepsisShield is a healthcare data-analysis and machine-learning research project focused on studying early warning patterns associated with sepsis in Intensive Care Unit (ICU) patients.

The project analyses patient vital signs, laboratory measurements, and demographic information to explore patterns in clinical time-series data and prepare the dataset for further predictive modelling.

**Project:** SepsisShield  
**Team:** Outlier Minds  
**Event:** NIErnaya 2026  
**Institution:** The National Institute of Engineering, Mysuru  
**Department:** Computer Science and Engineering  
**Current Phase:** Phase 2 — EDA, Data Preprocessing and Feature Engineering

---

## 🎯 Project Objectives

- Explore ICU patient data and understand its structure.
- Identify missing values, duplicate records and unusual observations.
- Discover patterns and relationships among clinical variables.
- Analyse changes in patient measurements over time.
- Perform data cleaning and preprocessing.
- Develop meaningful temporal features.
- Explore feature selection and Principal Component Analysis (PCA).
- Prepare the dataset for subsequent machine-learning research.

## 📊 Dataset

This project uses the **PhysioNet/Computing in Cardiology Challenge 2019** dataset.

The dataset contains hourly ICU patient observations, including:

| Category | Variables |
|---|---|
| Vital Signs | HR, O2Sat, Temp, SBP, MAP, DBP, Resp, EtCO2 |
| Laboratory Measurements | Lactate, Creatinine, Glucose, WBC, Platelets and others |
| Demographic Information | Age, Gender |
| ICU Information | ICULOS, HospAdmTime, Unit1, Unit2 |
| Target Variable | SepsisLabel |

**Original Dataset Source:**  
https://physionet.org/content/challenge-2019/1.0.0/

**Important:** The notebook uses the project-prepared merged file named `Dataset.csv`. The dataset is not included in this GitHub repository because of its large file size. Obtain the source data from PhysioNet and use the prepared merged dataset locally.

## 🔍 Phase 2 — Exploratory Data Analysis

The first stage investigates the structure, quality and characteristics of the ICU dataset.

### Analysis Performed

- Dataset dimensions and variable inspection.
- Descriptive statistical analysis.
- Patient-level and hourly-level sepsis label distribution.
- Missing-value analysis.
- Measurement availability across patients.
- Duplicate record investigation.
- Outlier identification using the IQR method.
- Vital-sign distribution analysis.
- Correlation analysis between clinical measurements.
- Missingness comparison between positive and negative sepsis labels.
- Temporal analysis around the first positive SepsisLabel hour.

### Interactive Visualizations

Interactive graphs are developed using Plotly.

They support:
- Hovering over data points to inspect values.
- Zooming and panning.
- Interactive histograms and boxplots.
- Correlation heatmaps with labelled values.
- Temporal trend visualizations.
- Annotated reference points.

## 📁 Repository Structure

```text
SepsisShield---Outlier-Minds/
│
├── README.md
│
├── SepsisShield_Person1_EDA.ipynb
│
├── .gitignore
│
└── Dataset.csv  (kept locally, not uploaded)
```

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming language |
| Jupyter Notebook | Interactive analysis |
| Pandas | Data manipulation and analysis |
| NumPy | Numerical computation |
| Plotly | Interactive visualizations |

## ⚙️ How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/2025csmohammedfaisalpashad-ctrl/SepsisShield---Outlier-Minds.git
```

### 2. Navigate into the project directory

```bash
cd SepsisShield---Outlier-Minds
```

### 3. Install the required libraries

```bash
pip install pandas numpy plotly jupyter
```

### 4. Add the dataset

Place the prepared `Dataset.csv` file in the same folder as the Jupyter notebook.

### 5. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open `SepsisShield_Person1_EDA.ipynb` and select **Run All Cells**.

## 📌 Important Data Considerations

- The dataset contains repeated hourly observations for individual patients. Row-level and patient-level statistics must therefore be interpreted separately.
- Missing measurements indicate that a variable was not recorded at a particular time point; they do not automatically indicate a normal or abnormal clinical condition.
- Statistical outliers are investigated rather than automatically removed.
- Correlations and observed patterns do not establish causal relationships.
- The PhysioNet 2019 challenge labels are already shifted six hours ahead of the defined sepsis onset for early prediction. The label must not be shifted another six hours.

## ⚠️ Disclaimer

SepsisShield is an academic research prototype. Its analysis and future predictive models are not intended to diagnose sepsis, replace clinical judgement, or provide medical advice.

Any predictive performance must be evaluated and clinically validated before potential real-world use.

## 🚀 Future Scope

- Complete data preprocessing and temporal feature engineering.
- Feature selection and PCA exploration.
- Develop and evaluate machine-learning models.
- Incorporate explainability techniques.
- Explore an interactive interface for visualizing patient risk patterns.

---

**Developed by Team Outlier Minds**  
**NIErnaya 2026 | The National Institute of Engineering, Mysuru**
