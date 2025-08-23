# Spotify Data Analysis

## Overview

This project analyzes Spotify songs using their metadata and audio features to identify trends in music characteristics such as **popularity, danceability, energy, tempo, and genre**.
The workflow includes **data cleaning with Python**, generating a cleaned dataset (`cleaned_spotify.csv`), and building an **interactive Excel dashboard** with pivot tables and charts.

---

## Step 1 – Data Cleaning with Python

Run the Jupyter Notebook (or Python script) to clean the dataset and export a filtered CSV.

### Cleaning Process:

* Removed irrelevant columns (`Unnamed: 0`, `track_id`)
* Dropped rows with missing values in key fields (`track_name`, `artists`, `track_genre`, `popularity`)
* Filtered out songs with **popularity < 50**
* Reset index for consistency

The cleaned dataset is saved as:

```
cleaned_spotify.csv
```

---

## Step 2 – Preparing Excel for Analysis

1. Open **Excel** and load `cleaned_spotify.csv`

   * Go to **Data → Get Data → From Text/CSV**
   * Convert into a **Table** (Ctrl + T)

---

## Step 3 – Pivot Tables

Create pivot tables to analyze key trends:

1. **Top Genres by Song Count**

   * Rows: `track_genre`
   * Values: `track_name` (Count)

2. **Average Popularity vs Danceability per Genre**

   * Rows: `track_genre`
   * Values: `popularity` (Average), `danceability` (Average)

3. **Tempo Distribution**

   * Rows: `tempo` (grouped into ranges: e.g., 0–60, 60–120, etc.)
   * Values: `track_name` (Count)

4. **Mood Analysis (Energy vs Valence)**

   * Rows: `track_genre`
   * Values: `energy` (Average), `valence` (Average)

---

## Step 4 – Dashboard Creation

On a new Excel sheet, insert the following charts linked to pivot tables:

1. **Bar Chart** → Top genres by number of songs
2. **Bar + Line Combo Chart** → Popularity (bar) vs Danceability (line)
3. **Line Chart** → Tempo distribution (by grouped ranges)
4. **Line Chart** → Energy vs Valence (mood analysis)

Add **Slicers** for interactivity:

* Genre (`track_genre`)
* Popularity range

---

## Insights

The dashboard allows you to explore:

* Which **genres dominate** Spotify’s library
* Relationship between **danceability and popularity**
* How **tempo** varies across music genre
* Mood patterns based on **energy vs valence**

---

## Deliverables

* `Spotify Dataset.csv` → Original dataset
* `cleaned_spotify.csv` → Cleaned dataset for analysis

* `Spotify_Dashboard.xlsx` → Final Excel dashboard

---

Dataset Source: [Spotify Tracks Dataset by Maharshi Pandya on Kaggle](https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset)  
