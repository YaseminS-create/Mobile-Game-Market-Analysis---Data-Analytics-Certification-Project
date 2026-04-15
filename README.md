# Mobile-Game-Market-Analysis---Data-Analytics-Certification-Project
This project analyzes the mobile gaming market using two datasets with over 17,000 strategy games and the highest-grossing mobile games worldwide. The goal was to uncover patterns in ratings, pricing, revenue, and developer success and to identify which strategy games broke into the top-grossing tier.

Project Overview
This project analyzes the mobile gaming market using two datasets: a collection of over 17,000 iOS strategy games and a list of the highest-grossing mobile games worldwide. The goal was to understand patterns in ratings, pricing, monetization, and developer success, and to find out which strategy games made it into the top-grossing segment.

Repository Structure
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

Tools and Libraries
CategoryToolsLanguagePython 3Data Wranglingpandas, numpyVisualizationmatplotlib, seaborn, plotlyInteractive UIipywidgetsEnvironmentJupyter Notebook

Part 1: Data Cleaning
Notebook: datenbereinigung_games.ipynb
Both datasets were loaded, inspected, and cleaned before any analysis took place. The raw files were never modified.
Strategy Games Dataset

Standardized all column names to snake_case
Removed columns not needed for analysis (URL, ID, Subtitle, Icon URL, Description)
Removed duplicate records and trimmed all text fields
Parsed date columns with error handling
Converted numeric fields (price, size, ratings) safely
Engineered additional features including file size in MB, in-app purchase statistics (min, max, average, count), language count, genre count, and plausibility flags for price, size, and rating

Highest-Grossing Dataset

Standardized column names and cleaned text fields
Parsed release dates
Converted revenue to numeric
Engineered features including publisher and genre lists, publisher and genre count, revenue in billions, and a validity flag for revenue values


Part 2: Analysis
Notebook: Mobile_Game_Analyse.ipynb
Questions explored for Strategy Games

How are user ratings distributed across the dataset?
What is the relationship between review count and rating?
How many games are free versus paid?
Which developers have the most games in the dataset?

Questions explored for Highest-Grossing Games

Which genres generate the most revenue on average?
Which publishers dominate the top-grossing charts?

Merged Analysis
Both datasets were joined via normalized game names since no shared primary key was available. This made it possible to flag strategy games that also appear in the highest-grossing list and compare them against the rest on metrics like average rating, review count, pricing, and in-app purchase usage.
An interactive dashboard was built using ipywidgets and Plotly, allowing filtering by genre, price type, and grossing status.

How to Run
Clone the repository:
bashgit clone https://github.com/YOUR_USERNAME/mobile-game-analysis.git
cd mobile-game-analysis
Install dependencies:
bashpip install pandas numpy matplotlib seaborn plotly ipywidgets jupyter
Run the notebooks in order. Start with datenbereinigung_games.ipynb to generate the cleaned CSV files, then open Mobile_Game_Analyse.ipynb for the full analysis.

Key Findings
Free-to-play with in-app purchases is the dominant monetization model among top-grossing games. Highest-grossing strategy games show significantly higher review counts compared to other strategy games, suggesting that reach and visibility matter as much as game quality. A small number of publishers account for a disproportionate share of total revenue, pointing to high market concentration. Games available in more languages tend to perform better in terms of both ratings and review volume.

Notes
This project was completed as part of a Data Analytics certification. The datasets were sourced from Kaggle and are used here for educational purposes only.
