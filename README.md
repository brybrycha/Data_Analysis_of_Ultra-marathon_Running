# Ultra Marathon Race Analysis (2020)

This project provides an in-depth exploratory data analysis (EDA) of ultra-marathon race data from **2020**. The analysis was conducted using **Python** with the `pandas` and `seaborn` libraries in a **Jupyter Notebook** environment.  
The primary goal was to **clean and prepare** a large dataset and then use it to answer specific questions about runner performance based on **age, gender,** and **race season**.

---

## Dataset

The data for this analysis was sourced from the [**The Big Dataset of Ultra Marathon Running**](https://www.kaggle.com/datasets) on Kaggle.  
This comprehensive dataset contains over **7 million race records from 1798 to 2022**  
`[cite: marathon.ipynb]`

For this project, the focus was narrowed to:
- **Races in the USA**
- **Year: 2020**
- **Distances: 50km or 50mi**  
`[cite: marathon.ipynb]`

---

## Data Cleaning and Preparation

The initial dataset had:
- **7.4 million+ rows**
- **13 columns**  
`[cite: marathon.ipynb]`

Key cleaning steps included:

### Filtering:
- Races from **2020**
- Located in **USA**
- Distance of **50km or 50mi**  
→ Resulting in **26,090 rows**  
`[cite: marathon.ipynb]`

### Column Creation and Modification:
- `athlete_age`: Calculated as `2020 - year_of_birth`  
- Cleaned `event_name`: Removed "(USA)"  
- Cleaned `performance`: Removed "h" for hours  
`[cite: marathon.ipynb]`

### Handling Missing Data:
- Removed rows with null values (especially in `athlete_age`)  
`[cite: marathon.ipynb]`

### Data Type Conversion:
- `athlete_age`: Converted to `int`  
- `average_speed`: Converted to `float`  
`[cite: marathon.ipynb]`

### Column Renaming:
- All column names standardized to **snake_case**  
`[cite: marathon.ipynb]`

---

## 📈 Analysis, Visualizations & Key Findings

### 🔹 Race Distance Distribution

- **50km races** had more participants than **50mi races**
- More **male runners**, but **gender gap smaller** in 50km races
- 
<img width="589" height="434" alt="output" src="https://github.com/user-attachments/assets/b694ef18-6b0f-4f48-bd5f-e1f256abd359" />


---

### How does average speed differ between male and female runners?

**50km Races:**
- Male: **7.74 km/h**
- Female: **7.08 km/h**  
`[cite: marathon.ipynb]`

**50mi Races:**
- Male: **7.26 km/h**
- Female: **6.83 km/h**  
`[cite: marathon.ipynb]`

> Violin plots show that **gender speed gaps** narrow in longer races

---

### What are the fastest and slowest age groups for 50mi races?

(Among age groups with ≥ 20 participants)

- **Fastest**: **29-year-olds**, avg speed **7.90 km/h**
- **Slowest**: **60s**, avg speeds **6.26 – 6.62 km/h**  
`[cite: marathon.ipynb]`

> lmplot shows a trend of **decreasing speed with age** for both genders

---

### Does race season affect a runner's average speed?

Created a new `race_season` column to group by season:

**50mi Races – Avg Speed by Season:**
- 🍂 Fall: **7.51 km/h**
- 🌸 Spring: **7.08 km/h**
- ❄️ Winter: **7.05 km/h**
- ☀️ Summer: **6.51 km/h**

> Runners were **slowest in summer**, likely due to **heat conditions**  
`[cite: marathon.ipynb]`

---

📌 *All analysis and visualizations were conducted in `marathon.ipynb` using Python, pandas, and seaborn.*
