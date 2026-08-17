# Global Video Game Sales — EDA & Data Visualization

**CodeAlpha Data Analytics Internship — Tasks 2 & 3**

An analysis of 16,598 video game titles (1980–2020), exploring global and regional
(NA / EU / JP / Other) sales trends, followed by interactive dashboards built to
visually communicate the findings.

---

## 📌 Overview

This project covers two of CodeAlpha's Data Analytics internship tasks using a single
dataset:

- **Task 2 — Exploratory Data Analysis (EDA):** framing questions, exploring data
  structure, identifying trends/patterns/anomalies, hypothesis testing, and documenting
  data quality issues.
- **Task 3 — Data Visualization:** turning the cleaned data into interactive dashboards
  using **Tableau** and **Power BI**.

The EDA notebook was the investigative groundwork done *before* the dashboards were
built — it shaped which charts and comparisons ended up in the final visualizations.

---

## 📂 Repository Contents

| File | Description |
|---|---|
| `EDA_Video_Game_Sales.ipynb` | Jupyter notebook with the full exploratory analysis |
| `EDA_Video_Game_Sales.html` | Rendered/exported HTML version of the notebook |
| `power_bi_game_sales_visualisation.pbix` | Power BI dashboard (Video Game Sales) |
| `Heritage_Treasures_Dashboard.twb` | Tableau workbook dashboard |
| `vgsales_csv.xlsx` | Source dataset (16,598 titles, 1980–2020) |

---

## 🔍 Task 2: EDA — Approach

The notebook is structured in six parts:

1. **Questions I wanted to answer** — five guiding questions, e.g. which genre sells
   most globally, whether console gaming declined over time, and whether regional
   genre preferences differ (especially Japan vs. the West).
2. **Data structure exploration** — shape, dtypes, column meanings, missing values,
   and duplicate checks.
3. **Trends, patterns & anomalies** — global sales by year, genre performance,
   outlier detection, and platform-family trends over time.
4. **Hypothesis testing** — statistically comparing Action-genre sales between North
   America and Japan.
5. **Data issues found & how they were handled** — a documented cleaning log.
6. **Key findings summary**.

### Key Findings

- **Action is the top-selling genre globally**, followed by Sports and Shooter — but
  this masks a real regional split: **Japan's market leans toward Role-Playing**, while
  Action dominates in NA and Europe. Confirmed statistically — Action sales average
  roughly **4x higher** in NA than in Japan (both mean and median).
- **Console platforms drove the industry's growth**, with global sales peaking sharply
  around **2008** before declining; PC and Handheld sales stayed comparatively flat
  throughout the period.
- **The sales distribution is heavily right-skewed.** The median title sold only
  **0.17M** units, but a handful of outliers — **Wii Sports (82.7M)** most of all —
  pull the mean up to 0.53M. This is why the dashboards use **sums and medians**
  rather than means for genre/region comparisons.
- **Data quality was solid overall.** Main issues were missing `Year` values, missing
  `Publisher` values, and a handful of rows from incomplete data-collection years
  (2017/2020) — all handled without discarding usable data (see the notebook's
  data-issues table for exact counts and handling logic).
- These findings directly shaped the dashboard design in Task 3 — particularly the
  decision to build a dedicated **"Genre Preferences by Region"** view, since the
  region–genre interaction turned out to be the most interesting pattern in the data.

---

## 📊 Task 3: Data Visualization — Approach

Using the cleaned dataset and insights from the EDA, two dashboards were built:

- **Power BI** (`power_bi_game_sales_visualisation.pbix`) — interactive dashboard
  covering global/regional sales trends, top genres and platforms, and publisher
  performance.
- **Tableau** (`Heritage_Treasures_Dashboard.twb`) — supporting visual dashboard
  built to present the same story with Tableau's charting tools.

Design choices were driven directly by the EDA: sums/medians over means (to avoid
outlier skew), a dedicated region-vs-genre comparison view, and a year-over-year trend
chart highlighting the industry's 2008 peak.

---

## 🛠️ Tools & Libraries Used

- **Python:** pandas, numpy, matplotlib, seaborn
- **Environment:** Jupyter Notebook
- **Visualization:** Power BI, Tableau

---

## 🎥 Video Explanation

📺 **Video Link:** _[Add your LinkedIn / YouTube video link here]_

> As per internship guidelines, a short video explaining this project was recorded and
> posted on LinkedIn, tagging **@CodeAlpha**.

---

## 🚀 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/<your-username>/CodeAlpha_ProjectName.git
   cd CodeAlpha_ProjectName
   ```
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn openpyxl jupyter
   ```
3. Launch the notebook:
   ```bash
   jupyter notebook EDA_Video_Game_Sales.ipynb
   ```
4. Open `power_bi_game_sales_visualisation.pbix` in **Power BI Desktop** or
   `Heritage_Treasures_Dashboard.twb` in **Tableau** to view the dashboards.

---

## 🙌 Acknowledgements

This project was completed as part of the **CodeAlpha Data Analytics Internship**.

- Website: [www.codealpha.tech](http://www.codealpha.tech)
- Email: services@codealpha.tech

---

## 👤 Author

_[Your Name]_
_[LinkedIn Profile Link]_
