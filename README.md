# 🚢 TitanicLens — Survival Pattern Analysis with Python
An **Exploratory Data Analysis (EDA)** project using Python to investigate the
factors that influenced passenger survival aboard the Titanic. Through data
cleaning, statistical analysis, and visualizations, this project uncovers the
key patterns behind one of history's most studied datasets.

---

## 📁 Repository Structure

```
📦 TitanicLens
 ┣ 📓 Titanic.ipynb               ← Main Jupyter Notebook (EDA + visualizations)
 ┣ 📂 Titanic-Dataset.csv         ← Source dataset
 ┣ 📁 screenshots/
 ┃ ┣ 🖼️ survival_by_sex.png
 ┃ ┣ 🖼️ age_distribution.png
 ┃ ┗ 🖼️ correlation_heatmap.png
 ┗ 📄 README.md
```

---

## 🔍 Project Workflow

### 1. 📥 Data Loading
- Loaded `Titanic-Dataset.csv` using **Pandas**
- Initial exploration using `.head()`, `.info()`, `.describe()`, `.columns()`

---

### 2. 🧹 Data Cleaning

| Column | Issue | Fix Applied |
|---|---|---|
| `Age` | 177 missing values | Filled with **column mean** |
| `Embarked` | 2 missing values | Filled with **mode** (most common port) |
| `Cabin` | Too many missing values | **Dropped** entirely |
| `Survived` | Object type | Cast to **integer** |

---

### 3. 📊 Exploratory Data Analysis (EDA)

#### Statistical Summary
- Calculated **mean age** and **mean fare** across all passengers
- Grouped survival rates by **Sex**, **Passenger Class (Pclass)**, and **Embarkation Port**

#### Survival Rate by Sex
```
df.groupby('Sex')['Survived'].mean()
```
→ Females had a significantly higher survival rate than males

#### Survival Rate by Class
```
df.groupby('Pclass')['Survived'].mean()
```
→ 1st class passengers survived far more often than 3rd class

#### Survival Rate by Embarkation Port
```
df.groupby('Embarked')['Survived'].mean()
```
→ Port of embarkation showed notable differences in survival rates

---

### 4. 📈 Visualizations

| Chart | Type | Insight |
|---|---|---|
| Survival by Sex | Bar Chart (Seaborn) | Females dramatically outsurvived males |
| Passenger Count by Port | Count Plot (Seaborn) | Southampton had the most passengers |
| Age Distribution | Histogram (Matplotlib) | Most passengers were 20–40 years old |
| Feature Correlation | Heatmap (Seaborn) | Fare & Pclass most correlated with survival |

---

## 💡 Key Findings

| # | Finding |
|---|---|
| 1 | **Females had a much higher survival rate than males** — "women and children first" policy clearly reflected in the data |
| 2 | **First-class passengers survived more often** than second and third class |
| 3 | **Younger passengers** had slightly better survival chances |
| 4 | **Most passengers boarded from Southampton** (Port S) |
| 5 | **Higher ticket fares were associated with higher survival rates** — a proxy for socioeconomic status |

---

## 🛠️ Tools & Libraries

| Tool | Purpose |
|---|---|
| **Python 3** | Core programming language |
| **Pandas** | Data loading, cleaning, and analysis |
| **Matplotlib** | Histogram and plot customization |
| **Seaborn** | Bar chart, count plot, heatmap |
| **Jupyter Notebook** | Interactive analysis environment |

---

## 📦 Dataset

| Property | Value |
|---|---|
| **File** | `Titanic-Dataset.csv` |
| **Source** | [Kaggle Titanic Competition](https://www.kaggle.com/c/titanic) |
| **Key Columns** | `Survived`, `Pclass`, `Sex`, `Age`, `Fare`, `Embarked`, `SibSp`, `Parch` |

---

## ⚙️ Requirements

```bash
pip install pandas matplotlib seaborn notebook
```

## 🚀 Getting Started

```bash
# 1. Clone the repository
git clone https://github.com/sararaafat08/-TitanicLens-Survival-Pattern-Analysis-with-Python.git

# 2. Navigate to the project folder
cd TitanicLens

# 3. Launch Jupyter Notebook
jupyter notebook Titanic.ipynb
```

---

## 🧠 Skills Demonstrated

`Python` · `Pandas` · `Matplotlib` · `Seaborn` · `Data Cleaning` ·
`Exploratory Data Analysis (EDA)` · `Statistical Analysis` ·
`Data Visualization` · `Missing Value Handling` · `Feature Analysis`

---

## 📌 About This Project

This project is part of my data analytics portfolio built during my studies in
Mathematics & Computer Science at **Faculty of Science, Helwan University**.
It demonstrates core EDA skills: loading raw data, handling missing values,
extracting statistical insights, and communicating findings through clean
visualizations.

---

## 📄 License

Free to use as a learning reference or portfolio template. Attribution appreciated.
