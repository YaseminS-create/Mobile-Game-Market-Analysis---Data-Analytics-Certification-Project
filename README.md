# Mobile-Game-Market-Analysis---Data-Analytics-Certification-Project
This project analyzes the mobile gaming market using two datasets with over 17,000 strategy games and the highest-grossing mobile games worldwide. The goal was to uncover patterns in ratings, pricing, revenue, and developer success and to identify which strategy games broke into the top-grossing tier.

---

## Repository Structure

```
mobile-game-analysis/
│
├── notebooks/
│   ├── datenbereinigung_games.ipynb
│   └── Mobile_Game_Analyse.ipynb
│
├── Datensatz/
│   ├── 17k_strategy_games.csv
│   ├── Highest_Grossing_Mobile_Game.csv
│   ├── 17k_strategy_games_cleaned.csv
│   └── Highest_Grossing_Mobile_Game_cleaned.csv
│
└── README.md
```

---

## Tools and Libraries

| Category       | Tools                       |
| -------------- | --------------------------- |
| Language       | Python 3                    |
| Data Wrangling | pandas, numpy               |
| Visualization  | matplotlib, seaborn, plotly |
| Interactive UI | ipywidgets                  |
| Environment    | Jupyter Notebook            |

---

## Part 1: Data Cleaning

Notebook: `datenbereinigung_games.ipynb`

Both datasets were loaded, inspected, and cleaned before analysis. The original raw files were not modified.

### Strategy Games Dataset

* Standardized column names to snake_case
* Removed irrelevant columns (URL, ID, Subtitle, Icon URL, Description)
* Removed duplicates and cleaned text fields
* Parsed date columns with error handling
* Converted numeric fields (price, size, ratings) safely

**Feature Engineering:**

* File size in MB
* In-app purchases: min, max, average, count
* Language count
* Genre count
* Plausibility flags for price, size, and rating

---

### Highest-Grossing Dataset

* Standardized column names
* Cleaned text fields
* Parsed release dates
* Converted revenue to numeric

**Feature Engineering:**

* Publisher list and count
* Genre list and count
* Revenue in billions
* Revenue validity flag

---

## Part 2: Analysis

Notebook: `Mobile_Game_Analyse.ipynb`

### Strategy Games

* Distribution of user ratings
* Relationship between review count and rating
* Free vs paid games
* Developers with the most published games

---

### Highest-Grossing Games

* Average revenue by genre
* Dominant publishers in top charts

---

### Merged Analysis

The datasets were merged using normalized game names since no shared primary key was available.

This enabled:

* Identification of strategy games in the top-grossing list
* Comparison with non-top-grossing strategy games

**Compared metrics:**

* Average rating
* Review count
* Pricing model
* In-app purchase usage

---

## Interactive Dashboard

An interactive dashboard was built using ipywidgets and Plotly.

**Features:**

* Filter by genre
* Filter by price type
* Filter by grossing status

---

## How to Run

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/mobile-game-analysis.git
cd mobile-game-analysis
```

### 2. Install dependencies

```bash
pip install pandas numpy matplotlib seaborn plotly ipywidgets jupyter
```

### 3. Run notebooks

1. Start with:
   `datenbereinigung_games.ipynb`
   generates cleaned datasets

2. Then open:
   `Mobile_Game_Analyse.ipynb`
   performs analysis and visualization

---

## Key Findings

* Free-to-play with in-app purchases dominates the market
* Top-grossing strategy games have significantly higher review counts
* A small number of publishers control a large share of revenue
* Games available in multiple languages tend to perform better

---

## Notes

This project was completed as part of a Data Analytics certification.

Datasets were sourced from Kaggle and are used for educational purposes only.

Author

Yasemin

