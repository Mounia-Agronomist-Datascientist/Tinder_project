# Tinder Project — Speed Dating EDA

## Context

This project is an **Exploratory Data Analysis (EDA)** conducted on a speed dating dataset originally collected at Columbia University. The central question addressed is:

> **Can we identify what drives people to select someone for a second date?**

The analysis was carried out as part of a data science project for Tinder, with the goal of better understanding the factors that lead to a mutual match between two participants.

---

## Dataset

- **File:** `DATA/Speed_dating_data.csv`
- **Source:** Columbia University Speed Dating Experiment
- **Size:** 8,378 rows × 195 columns
- **Encoding:** ISO-8859-1

Each row represents **one speed date** (a pair interaction during an event). The dataset includes:
- Demographic information (age, gender, race, field of study, income)
- Stated preferences before the event (importance of attractiveness, sincerity, intelligence, etc.)
- Ratings given during the event (attractiveness, fun, ambition, shared interests, etc.)
- Self-assessments
- Match outcome (`match` = 1 if both participants said yes)

> **Note:** The `DATA/` folder is excluded from version control (`.gitignore`). The dataset must be placed manually at `DATA/Speed_dating_data.csv` before running the notebook.

---

## Notebook Structure

The analysis is organized into 9 sections:

| Section | Title | Description |
|---------|-------|-------------|
| I | Data Overview | First look at the raw data (shape, types, distributions) |
| II | Data Cleaning & Preparation | Missing values, feature engineering (`gender_label`, `same_race`), column selection |
| III | General Descriptives | Participant profiles: gender, age, race, overall match rate |
| IV | Attraction Criteria by Gender | Stated importance of criteria (attractiveness, sincerity, fun…) compared between men and women |
| V | Perceived Attractiveness vs. Real Impact | Do high ratings on a criterion actually translate into more matches? |
| VI | Shared Interests vs. Same Race | Which factor is more associated with match: shared interests or shared background? |
| VII | Self-Assessment Accuracy | Do people accurately predict how others will rate them? |
| VIII | Date Order Effect | Does going early or late in the evening influence match success? |
| IX | Summary & Conclusion | Key observations and EDA takeaways |

---

## Key Findings

- **Overall match rate:** ~16.4% — participants are selective.
- **Gender differences in stated preferences:** Men declare higher importance for attractiveness and fun; women for sincerity, intelligence, and ambition.
- **Actual drivers of match:** High ratings on attractiveness, fun, and shared interests are positively associated with match outcomes.
- **Shared interests vs. same race:** Shared interests show a stronger association with match than sharing the same racial background.
- **Self-assessment:** Correlations between self-ratings and ratings received from others are positive but weak (r ≈ 0.04–0.08), suggesting limited self-awareness.
- **Timing effects:** Some variation in match rates across the evening exists, but remains moderate.

> All findings are **descriptive and associative** — no causal claims are made.

---

## Tech Stack

| Library | Usage |
|---------|-------|
| `pandas` | Data manipulation |
| `numpy` | Numerical operations |
| `matplotlib` / `seaborn` | Static visualizations |
| `plotly` | Interactive charts (Section I) |
| `scipy.stats` | Pearson correlation |

---

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/mounia-agronomist-datascientist/tinder_project.git
   cd tinder_project
   ```

2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn plotly scipy jupyter
   ```

3. Place the dataset at the following path:
   ```
   DATA/Speed_dating_data.csv
   ```

4. Launch the notebook:
   ```bash
   jupyter notebook projet_tinder.ipynb
   ```

---

## Author

**Mounia** — Data Scientist / Agronomist
Mounia Tonazzini
LinkedIn: www.linkedin.com/in/mounia-tonazzini
GitHub: Mounia-Agronomist-Datascientist

This project is part of the Jedha Data science Bootcamp.