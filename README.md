# Netflix Data Analysis Project 2025 🎬📊

A full Data Science project analyzing Netflix movies using Python.

Inspired by publicly available Netflix data science tutorials and further enhanced with additional analysis and visualizations.

---

## 📁 Project Structure

```
Netflix-Data-Analysis-Project-2025/
│
├── mymoviedb.csv                   ← Raw dataset (9000+ movies)
├── transformed_netflixdata.csv     ← Cleaned & transformed dataset
├── Netflix_Data_Analysis.ipynb     ← Main Jupyter Notebook
├── genre_distribution.png          ← Genre distribution chart
├── vote_category_distribution.png  ← Vote category count plot
├── yearly_releases.png             ← Yearly movie releases histogram
├── genre_popularity.png            ← Average popularity by genre
└── README.md                       ← This file
```

---

## 📦 Dataset: `mymoviedb.csv`

| Column | Description |
|--------|-------------|
| `Release_Date` | Date the movie was released |
| `Title` | Movie title |
| `Overview` | Brief description of the movie |
| `Popularity` | Popularity score (numeric) |
| `Vote_Count` | Total number of votes |
| `Vote_Average` | Average vote rating (out of 10) |
| `Original_Language` | Original language of the movie |
| `Genre` | Comma-separated genres |
| `Poster_Url` | URL of movie poster image |

---

## 🔍 Analysis Performed

1. **Data Loading** — Load `mymoviedb.csv` using Pandas
2. **Data Exploration** — `.head()`, `.info()`, `.describe()`, `.shape`
3. **Data Cleaning:**
   - Check for duplicates and missing values
   - Drop `Overview`, `Original_Language`, `Poster_Url`
   - Convert `Release_Date` to datetime → extract year
4. **Feature Engineering:**
   - Categorize `Vote_Average` (Excellent / Good / Average / Below Average / Poor / Very Poor)
   - Split `Genre` (comma-separated) → explode to individual rows
   - Convert `Genre` to categorical type
5. **Save transformed data** → `transformed_netflixdata.csv`
6. **Visualizations:**
   - 📊 Genre Distribution (bar plot)
   - 📊 Vote Category Distribution (count plot)
   - 🎬 Most Popular Movie
   - 🎬 Least Popular Movies
   - 📅 Yearly Movie Releases (histogram)
   - 🌟 Average Popularity by Genre (bar plot)

---

## ⚙️ How to Run

### Requirements
- Python 3.8+
- Jupyter Notebook or JupyterLab

### Step 1 — Install dependencies
```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### Step 2 — Launch Jupyter Notebook
```bash
jupyter notebook
```

### Step 3 — Open the notebook
In the browser tab that opens, click on `Netflix_Data_Analysis.ipynb`

### Step 4 — Run all cells
Click **Kernel → Restart & Run All**

---

## 📤 Expected Output

When you run the notebook, you will see:
- Dataset loaded with **9,827 rows and 9 columns**
- **0 duplicates** and **0 missing values**
- Genre expanded → **~19,000+ rows** after explode
- **4 charts** rendered inline in the notebook
- `transformed_netflixdata.csv` saved to the same folder

---

*Project recreated from TheiScale YouTube tutorial — Netflix Data Analysis 2025*
