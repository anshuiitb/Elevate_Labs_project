# Elevate_Labs_project

# Trending Jobs Scraper + Predictor

This repository contains a Jupyter Notebook (`trending_jobs_notebook.ipynb`) that scrapes job listings from public job boards, analyzes them using NLP, and uses Google Trends data to **predict which job titles are likely to trend next week**.

---

## 📌 Features
- **Web Scraping**  
  - Scrapes job titles from **RemoteOK** and **WeWorkRemotely** (example sites).  
  - Can be extended to other job boards or APIs.  

- **Data Cleaning & NLP**  
  - Preprocesses job titles (lowercasing, regex cleanup).  
  - Uses **TF-IDF** + **KMeans clustering** to identify common job categories.  
  - Extracts frequent unigrams & bigrams as candidate keywords.  

- **Google Trends Integration**  
  - Fetches search interest for candidate job keywords via `pytrends`.  
  - Uses the past **7 days** of search data.  

- **Prediction**  
  - Trains a simple **Linear Regression model** per keyword.  
  - Forecasts average interest for the **next 7 days**.  
  - Outputs a ranked list of predicted trending job keywords.  

- **Exports**  
  - `scraped_job_titles.csv` → all collected job titles.  
  - `predicted_trending_jobs.csv` → ranked trending job predictions.  

---

## ⚙️ Installation
Clone this repo or copy the notebook, then install required packages:

```bash
pip install requests beautifulsoup4 pandas scikit-learn pytrends numpy matplotlib
