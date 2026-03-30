# 🌍 Global Happiness Report Analysis (2015–2019)

> ***Exploring what makes countries happy — through data, charts, and insights.***

---

## 📌 Project Overview

**Global Happiness Report Analysis** is a ***data science project*** built in a **Jupyter Notebook** that analyzes the ***World Happiness Report*** dataset spanning **5 years (2015–2019)**. The project loads, cleans, merges, and explores happiness data from **156+ countries** to uncover ***what factors drive happiness*** — including *GDP*, *Social Support*, *Life Expectancy*, *Freedom*, *Generosity*, and *Corruption*.

The analysis follows a ***complete EDA pipeline*** — from *raw CSV loading* and *data cleaning* to *statistical correlation analysis* and *8 rich Seaborn/Matplotlib visualizations* — making it a strong **portfolio-ready data science project**.

> **Key Finding:** ***GDP per Capita*** (correlation: **0.79**) and ***Social Support*** (correlation: **0.65**) are the *strongest predictors* of national happiness. ***Generosity*** has the *weakest* correlation at only **0.14**.

---

## ✨ Features

- 📂 **Multi-Year Data Loading** — Loads ***5 separate CSV files*** (2015–2019) into individual DataFrames
- 🧹 **Data Cleaning & Standardization** — Renames *inconsistent column names* across years and merges all into a ***single unified DataFrame***
- 🔍 **Exploratory Data Analysis (EDA)** — Inspects *shape*, *missing values*, *data types*, and *country counts* per year
- 📊 **8 Rich Visualizations** — Histogram, Bar Charts, Line Chart, Scatter Plots, Pie Chart, Heatmap, Box Plot, and Multi-line Chart — all built with ***Matplotlib & Seaborn***
- 📈 **Correlation Analysis** — Computes and ranks ***which factor contributes most*** to happiness using `.corr()`
- 🏆 **Top & Bottom Country Ranking** — Identifies ***Top 10 happiest*** and ***Bottom 10 least happy*** countries in 2019
- 🌐 **Top 5 Country Tracking** — Tracks ***score trends*** of the top 5 countries across all 5 years
- ✅ **Final Conclusions** — Summarizes *total records*, *unique countries*, *happiest/least happy country*, and *most important factor*

---

## 📈 Charts & Visual Analysis

> *Every chart tells a part of the story — together they reveal the full picture of global happiness.*

---

### 📊 Chart 1 — Average World Happiness Score Each Year
> *Described — chart saved as `chart1_distribution.png` in original notebook but not in Charts folder*

The ***global average happiness score*** was calculated for each year from 2015 to 2019 using `df.groupby('Year')['Score'].mean()`. The results reveal:

- **2015** → avg score: **5.38** — *stable starting point*
- **2016** → avg score: **5.38** — *slight rise*
- **2017** → avg score: **5.35** — ***lowest point*** of the 5-year period
- **2018** → avg score: **5.38** — *recovery*
- **2019** → avg score: **5.41** — ***highest point*** — world getting happier overall

> 💡 **Insight:** Despite global challenges, the world's ***average happiness trended upward*** from 2015 to 2019 — with **2017 being the only dip** in the otherwise positive trajectory.

---

### 📈 Chart 2 — Average World Happiness Score Trend (Line Chart)

The ***line chart*** plots the *year-by-year average happiness score* from **2015 to 2019**. Each data point is annotated with its exact value, making the trend immediately readable. The score dipped to its ***lowest in 2017 (5.35)*** before recovering strongly to ***5.41 in 2019***.

![Average Happiness Trend](Charts/chart2_line.png)

> 💡 **Insight:** The ***V-shaped dip in 2017*** suggests a *global event or measurement shift* that temporarily reduced average scores — but the subsequent recovery indicates ***long-term positive momentum*** in global wellbeing.

---

### 🔵 Chart 3 — GDP per Capita vs Happiness Score (Scatter Plot)

This ***scatter plot*** visualizes the relationship between a country's ***economic wealth (GDP per Capita)*** and its ***Happiness Score*** across all 5 years combined. The clear ***upward diagonal pattern*** of orange dots confirms a *strong positive relationship*.

![GDP vs Happiness Scatter](Charts/chart3_scatter.png)

> 💡 **Insight:** Countries with ***higher GDP per Capita consistently score higher*** on happiness. The correlation coefficient of **0.79** makes GDP the ***single strongest predictor*** of happiness — but outliers exist, showing that *wealth alone doesn't guarantee happiness*.

---

### 🥧 Chart 4 — Countries by Happiness Group in 2019 (Pie Chart)

This ***pie chart*** categorizes all countries in 2019 into **3 happiness groups** based on their score:

| Group | Score Range | % of Countries |
|-------|------------|----------------|
| 🟢 **Happy** | Score ≥ 6 | ***33.3%*** |
| 🟠 **Moderate** | Score 4 to 6 | ***56.4%*** |
| 🔴 **Unhappy** | Score < 4 | ***10.3%*** |

![Happiness Groups Pie Chart](Charts/chart4_pie.png)

> 💡 **Insight:** In 2019, ***more than half the world's countries*** fall in the *moderate happiness range*. Only **1 in 3** countries are truly happy (score ≥ 6), while a ***concerning 10.3%*** remain in the unhappy category — mostly conflict-affected or economically struggling nations.

---

### 📊 Chart 5 — Average Factor Contribution to Happiness (Horizontal Bar Chart)

This ***horizontal bar chart*** ranks all **6 happiness factors** by their *average contribution value* in 2019, revealing which factors play the *biggest role* in determining a country's happiness score.

![Factor Contribution Bar Chart](Charts/chart5_hbar.png)

| Factor | Avg Contribution |
|--------|-----------------|
| 🥇 ***Social Support*** | **1.209** |
| 🥈 ***GDP*** | **0.905** |
| 🥉 ***Life Expectancy*** | **0.725** |
| 4️⃣ *Freedom* | 0.393 |
| 5️⃣ *Generosity* | 0.185 |
| 6️⃣ *Corruption* | 0.111 |

> 💡 **Insight:** ***Social Support*** contributes the *most* to happiness on average — even more than GDP. This suggests that ***having people to count on*** matters more than *how rich a country is* when it comes to overall wellbeing.

---

### 🌡️ Chart 6 — Correlation Heatmap (How Factors Relate to Each Other)

This ***Seaborn heatmap*** displays the ***Pearson correlation coefficients*** between all happiness factors using a *red-to-white color scale*. Darker red = stronger positive correlation, white/gray = weak or no correlation.

![Correlation Heatmap](Charts/chart6_heatmap.png)

**Key correlations with Happiness Score:**

| Factor | Correlation with Score |
|--------|----------------------|
| ***GDP*** | **0.79** — *very strong* |
| ***Life Expectancy*** | **0.74** — *strong* |
| ***Social Support*** | **0.65** — *strong* |
| ***Freedom*** | **0.55** — *moderate* |
| ***Corruption*** | **0.40** — *moderate* |
| ***Generosity*** | **0.14** — *weak* |

> 💡 **Insight:** ***Generosity has almost no correlation*** with happiness (-0.01 with GDP, -0.04 with Social Support) — suggesting that *giving* doesn't necessarily make countries happier at a national level. ***GDP and Life Expectancy*** are the *most interconnected factors* (0.78), implying wealthier nations also tend to live longer.

---

## 🧠 Concepts Used

- 🐼 **Pandas** — `read_csv()`, `rename()`, `concat()`, `groupby()`, `corr()`, `isnull()`, `describe()`, `head()`, `value_counts()`
- 📊 **Matplotlib** — `plt.hist()`, `plt.barh()`, `plt.plot()`, `plt.scatter()`, `plt.pie()`, `plt.savefig()`, `plt.tight_layout()`
- 🎨 **Seaborn** — `sns.heatmap()`, `sns.boxplot()` with `palette`, `annot`, `fmt`, `cmap` parameters
- 🧹 **Data Cleaning** — *Column renaming* across 5 differently structured CSVs, *adding Year column*, *concatenation* with `pd.concat()`
- 📐 **Correlation Analysis** — `.corr()` matrix, `idxmax()` to find *strongest factor*, sorted ranking
- 🔢 **EDA (Exploratory Data Analysis)** — `.shape`, `.describe()`, `.isnull().sum()`, `.value_counts()` for *data understanding*
- 🗂️ **Multi-file Data Pipeline** — Loading, cleaning, and ***merging 5 yearly CSV files*** into one unified DataFrame
- 📓 **Jupyter Notebook** — *Step-by-step documented analysis* with markdown cells explaining every section

---

## ▶️ How to Run

**Requirements:**
- ***Python 3.8 or higher***
- ***Jupyter Notebook*** or ***JupyterLab***
- Required libraries: ***Pandas***, ***Matplotlib***, ***Seaborn***

**Install dependencies:**
```bash
pip install pandas matplotlib seaborn jupyter
```

**Clone the repository:**
```bash
git clone https://github.com/your-username/Global_Happiness_Report_Analysis.git
cd Global_Happiness_Report_Analysis
```

**Launch Jupyter Notebook:**
```bash
jupyter notebook Global__Happiness_Report_Analysis.ipynb
```

> 💡 Make sure all **5 CSV files** (`2015.csv` to `2019.csv`) are in the ***same directory*** as the notebook before running.

---

## 📂 Program Flow

> **Analysis Pipeline Summary:**
> - 📦 **Step 1** → Import libraries — `pandas`, `matplotlib`, `seaborn`
> - 📂 **Step 2** → Load ***5 CSV files*** (2015–2019) into separate DataFrames
> - 🧹 **Step 3** → ***Rename columns*** to a standard format + add `Year` column → `pd.concat()` into one DataFrame
> - 🔍 **Step 4** → ***EDA*** — `.head()`, `.describe()`, `.isnull().sum()`, `.value_counts()`
> - 📊 **Step 5** → ***8 Visualizations*** — histogram, bar, line, scatter, pie, heatmap, boxplot, multi-line
> - 📈 **Step 6** → ***Correlation Analysis*** — `.corr()` → rank factors by relationship with Score
> - 🌍 **Step 7** → ***Track Top 5 countries*** across all 5 years
> - ✅ **Step 8** → ***Final Conclusions*** — happiest country, least happy, most important factor, total records

---

## 👨‍💻 Developer Notes & Code Highlights

### 🧹 Standardizing Column Names Across 5 Years
```python
df2015 = df2015.rename(columns={
    'Happiness Score'              : 'Score',
    'Economy (GDP per Capita)'     : 'GDP',
    'Family'                       : 'Social_Support',
    'Health (Life Expectancy)'     : 'Life_Expectancy',
    'Trust (Government Corruption)': 'Corruption'
})
df2015['Year'] = 2015
```
> Each year's CSV had ***different column names*** — this renaming step was critical to make `pd.concat()` work correctly. Without it, the merged DataFrame would have ***30+ duplicate columns*** instead of a clean 10-column structure.

---

### 🔗 Merging All Years into One DataFrame
```python
df = pd.concat([df2015, df2016, df2017, df2018, df2019], ignore_index=True)
print('Total records:', len(df))
```
> `pd.concat()` with `ignore_index=True` ***resets the row index*** after merging — essential for clean downstream operations like `.groupby()` and `.corr()`.

---

### 🌡️ Building the Correlation Heatmap
```python
correlation = df[factor_columns].corr()
sns.heatmap(correlation, annot=True, fmt='.2f', cmap='RdYlGn', linewidths=0.5)
```
> `annot=True` prints the ***exact correlation value*** inside each cell. `fmt='.2f'` formats it to *2 decimal places*. `cmap='RdYlGn'` uses a ***red-yellow-green color scale*** where green = strong positive, red = negative correlation.

---

### 🏆 Finding the Most Important Factor
```python
corr_with_score = df[factor_columns].corr()['Score'].drop('Score')
corr_with_score = corr_with_score.sort_values(ascending=False)
print('Most important factor:', corr_with_score.idxmax())
```
> `.corr()['Score']` extracts only the ***Score column*** from the full correlation matrix. `.idxmax()` returns the ***name of the factor*** with the highest correlation — which turns out to be **GDP (0.79)**.

---

## 📜 License

This project is licensed under the **MIT License** — *free to use, modify, and distribute.*

---

> Built with 🐍 **Python** | 🐼 **Pandas** | 🎨 **Seaborn** | 📊 **Matplotlib** | 📓 **Jupyter Notebook**
