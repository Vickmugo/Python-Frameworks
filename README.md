# Python-Frameworks
Interactive exploration and analysis of the CORD-19 COVID-19 research dataset. Includes data cleaning, visualization of publication trends and journals, keyword analysis with word clouds, and a Streamlit app for interactive browsing.
---

# 📑 **CORD-19 Metadata Analysis Documentation**

## 📘 **Project Overview**

This project analyzes the **CORD-19** dataset, a large collection of COVID-19 research papers, using **Python**, **Pandas**, and **Matplotlib**, and presents interactive visualizations via a **Streamlit app**.
The goal is to clean and explore the metadata to understand publication trends, top journals, and keyword patterns.

---

## 📂 **File Structure**

```
CORD19_Metadata_Analysis.ipynb   # Jupyter Notebook for cleaning, analysis, visualization
cord19_app.py                    # Streamlit app for interactive exploration
metadata.csv                     # Dataset metadata file (from Kaggle)
README.md                        # Documentation (this file)
```

---

## ⚙ **Setup Instructions**

### 1. **Requirements**

Install the necessary Python packages:

```bash
pip install pandas matplotlib wordcloud streamlit
```

### 2. **Dataset**

* Download the [CORD-19 Research Challenge](https://www.kaggle.com/allen-institute-for-ai/CORD-19-research-challenge) dataset from Kaggle.
* Extract `metadata.csv` into your project folder.

### 3. **Run the Jupyter Notebook**

* Open `CORD19_Metadata_Analysis.ipynb` in Jupyter Notebook or Google Colab.
* Upload or point to your `metadata.csv`.
* Run all cells to clean, explore, and visualize the data.

### 4. **Run the Streamlit App**

```bash
streamlit run cord19_app.py
```

---

## 🔎 **Analysis Performed**

1. **Data Inspection**

   * Checked DataFrame dimensions (`.shape`).
   * Displayed column data types (`.dtypes`).
   * Checked missing values (`.isnull().sum()`).
   * Summarized numerical statistics (`.describe()`).
   * Identified columns with high missing percentages.

2. **Data Cleaning**

   * Dropped rows missing essential fields (title, abstract).
   * Filled missing journal names with `"Unknown"`.
   * Converted `publish_time` to `datetime`.
   * Extracted `year` from `publish_time`.
   * Added `abstract_word_count` for analysis.

3. **Analysis & Visualization**

   * Counted papers by publication year.
   * Found top journals publishing COVID-19 research.
   * Generated a word cloud of frequent words in paper titles.
   * Plotted distributions of papers by source.

---

## 📊 **Key Visualizations**

* **Publications Over Time**: Bar chart showing research trends per year.
* **Top Journals**: Bar chart of journals with the most papers.
* **Title Word Cloud**: Highlights the most common keywords in paper titles.
* **Source Distribution**: Shows which repositories contributed the most papers.

---

## 🌐 **Streamlit App Features**

* Interactive **year range slider** to filter papers.
* Sample data display.
* Dynamic charts updating based on year selection.
* Word cloud generation for selected subsets.

---

## 📈 **Insights & Observations**

* A significant spike in publications occurred in 2020–2021.
* Certain journals dominated COVID-19 publications.
* Keywords like “COVID,” “SARS-CoV-2,” and “Coronavirus” are most frequent.

---

## 🛠 **Challenges & Lessons Learned**

* Handling missing values was crucial to avoid inaccurate statistics.
* Large datasets may require optimizing memory usage (`low_memory=False`).
* Creating interactive apps with Streamlit offers an engaging way to explore data.

---

## 🚀 **Next Steps**

* Add **topic modeling** (e.g., using LDA) for deeper insights.
* Include **citation count analysis** if citation data is available.
* Deploy the Streamlit app to a cloud platform (e.g., Streamlit Community Cloud or Heroku).


