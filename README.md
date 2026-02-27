# Exploratory Data Analysis (EDA) on the Titanic Dataset

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-2.x-150458?logo=pandas)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![License](https://img.shields.io/badge/License-MIT-green?logo=opensourceinitiative)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

A structured, end-to-end Exploratory Data Analysis project on the classic Titanic passenger dataset. This project walks through data ingestion, cleaning, univariate and multivariate analysis, and statistical insight extraction using Python's core data science stack.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Analysis Workflow](#analysis-workflow)
- [Key Findings](#key-findings)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Results Summary](#results-summary)
- [License](#license)
- [Author](#author)

---

## Project Overview

This project performs a comprehensive EDA on the Titanic dataset to identify the key factors that influenced passenger survival. The analysis follows a systematic pipeline — from raw data inspection and missing value treatment to in-depth visual and statistical exploration — concluding with actionable insights on survival predictors.

**Objective:** Identify the strongest demographic and socioeconomic features that correlate with survival outcomes aboard the RMS Titanic.

---

## Dataset

| Property       | Details                                                                                  |
|----------------|------------------------------------------------------------------------------------------|
| **Source**     | [DataScienceDojo GitHub Repository](https://raw.githubusercontent.com/datasciencedojo/datasets/refs/heads/master/titanic.csv) |
| **Records**    | 891 passengers                                                                           |
| **Features**   | 12 columns (PassengerId, Survived, Pclass, Name, Sex, Age, SibSp, Parch, Ticket, Fare, Cabin, Embarked) |
| **Target**     | `Survived` (0 = No, 1 = Yes)                                                             |
| **Format**     | CSV (loaded directly from URL)                                                           |

---

## Project Structure

```
EDA-Project/
│
├── Exploratory_Data_Analysis_(EDA)_on_the_Titanic_Dataset.ipynb   # Main analysis notebook
├── LICENSE                                                          # MIT License
└── README.md                                                        # Project documentation
```

---

## Analysis Workflow

### Task 1 — Data Loading & Initial Inspection
- Loaded dataset directly from a remote URL using `pandas.read_csv()`
- Inspected schema with `.info()`, `.dtypes()`, `.describe()`
- Identified missing values per column using `.isnull().sum()`

### Task 2 — Handling Missing Values
- **`Cabin`**: Dropped entirely — 77% missing values, low analytical value
- **`Embarked`**: Imputed 2 missing values using the **mode** (most frequent port)
- **`Age`**: Imputed missing values using the column **median** to preserve distribution robustness

### Task 3 — Univariate Analysis
- Calculated the overall survival rate (~38.4%)
- Visualized survival distribution with a bar chart
- Examined passenger class distribution (Class 3 had the most passengers)
- Analyzed age distribution via histogram

### Task 4 — Bivariate & Multivariate Analysis
- **Survival by Sex**: Cross-tabulation and stacked bar chart
- **Survival by Pclass**: Grouped mean survival rates with bar plot
- **Survival by Age**: Overlapping histograms comparing survivor vs. non-survivor age profiles
- **Survival by Port of Embarkation**: Grouped survival rates per embarkation point (C, Q, S)

### Task 5 — Conclusion & Insights
- Synthesized findings into the top survival predictors
- Documented statistical observations inline throughout the notebook

---

## Key Findings

| Factor              | Observation                                                                 |
|---------------------|-----------------------------------------------------------------------------|
| **Sex**             | Females had a ~74.2% survival rate vs. ~18.9% for males                    |
| **Passenger Class** | 1st class: ~63% survival; 2nd class: ~47%; 3rd class: ~24%                 |
| **Age**             | Children had notably higher survival rates; elderly passengers fared worse  |
| **Embarkation Port**| Passengers from Cherbourg (C) had the highest survival rate                 |

> **Top Survival Predictors:** `Sex` > `Pclass` > `Age`

---

## Tech Stack

| Library        | Purpose                              |
|----------------|--------------------------------------|
| `pandas`       | Data loading, manipulation, grouping |
| `numpy`        | Numerical operations                 |
| `matplotlib`   | Custom static visualizations         |
| `seaborn`      | Statistical plotting (count plots)   |
| `timeit`       | Performance benchmarking             |

---

## Getting Started

### Prerequisites

Ensure you have Python 3.8+ installed. Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### Clone the Repository

```bash
git clone https://github.com/MH-SHUVO20/EDA-Project.git
cd EDA-Project
```

### Running the Notebook

```bash
jupyter notebook Exploratory_Data_Analysis_(EDA)_on_the_Titanic_Dataset.ipynb
```

Alternatively, open the `.ipynb` file directly in **VS Code** with the Jupyter extension.

> **Note:** The dataset is fetched automatically from a public URL — no manual download required.

---

## Results Summary

The EDA confirms that survival on the Titanic was not random. **Gender** was the single strongest predictor, with female passengers far more likely to survive — consistent with the "women and children first" evacuation protocol. **Socioeconomic status** (Pclass) was the second most influential factor, as higher-class passengers had better access to lifeboats. **Age** showed that younger passengers, particularly children, had a survival advantage. Port of embarkation (Cherbourg) correlated with higher survival, likely due to its association with higher-class travelers.

These features form a strong foundation for downstream predictive modeling tasks (e.g., binary classification with logistic regression or tree-based models).

---

## License

This project is licensed under the **MIT License** — see the [LICENSE](./LICENSE) file for full details.

Copyright (c) 2025 [MH-SHUVO20](https://github.com/MH-SHUVO20)

---

## Author

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1117,50:1F6FEB,100:58A6FF&height=130&section=header&text=MD.%20MEHEDI%20HASAN%20SHUVO&fontSize=28&fontColor=ffffff&fontAlignY=65&animation=fadeIn" width="100%"/>

<br/>

<img src="https://github.com/MH-SHUVO20.png" width="110" style="border-radius: 50%; border: 3px solid #1F6FEB;" alt="MD. MEHEDI HASAN SHUVO"/>

<br/><br/>

### 👨‍💻 MD. MEHEDI HASAN SHUVO

<br/>

[![GitHub](https://img.shields.io/badge/GitHub-MH--SHUVO20-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/MH-SHUVO20)
[![Profile Views](https://komarev.com/ghpvc/?username=MH-SHUVO20&style=for-the-badge&color=1F6FEB&label=PROFILE+VIEWS)](https://github.com/MH-SHUVO20)

<br/>

<table align="center">
  <tr>
    <td align="center">🧑‍💼 <b>Role</b></td>
    <td>Project Owner</td>
  </tr>
  <tr>
    <td align="center">📊 <b>Project</b></td>
    <td>EDA on Titanic Dataset</td>
  </tr>
  <tr>
    <td align="center">🗓️ <b>Year</b></td>
    <td>2025</td>
  </tr>
  <tr>
    <td align="center">🛠️ <b>Tools Used</b></td>
    <td>Python · Pandas · NumPy · Matplotlib · Seaborn</td>
  </tr>
  <tr>
    <td align="center">📍 <b>Platform</b></td>
    <td>Google Colab / Jupyter Notebook</td>
  </tr>
</table>

<br/>

> *"Data is the new oil — and this project refines it into insight."*

<br/>

![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=18&pause=1000&color=58A6FF&center=true&vCenter=true&width=500&lines=Data+Analyst+%7C+Project+Owner;Python+%7C+Pandas+%7C+NumPy+%7C+Seaborn;EDA+on+Titanic+Dataset+%7C+2025)

<br/>

![GitHub Streak](https://streak-stats.demolab.com?user=MH-SHUVO20&theme=tokyonight&hide_border=true&ring=58A6FF&fire=1F6FEB&currStreakLabel=58A6FF)

<br/>

---

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:58A6FF,50:1F6FEB,100:0D1117&height=90&section=footer" width="100%"/>

⭐ **If you found this project helpful, please consider giving it a star!**

**Made with ❤️ by [MD. MEHEDI HASAN SHUVO](https://github.com/MH-SHUVO20) — 2025**

</div>