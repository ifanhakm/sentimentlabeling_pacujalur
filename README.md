# Pacu Jalur Trend Sentiment Analysis

[![Language](https://img.shields.io/badge/Language-Python-blue.svg)](https://www.python.org/)
[![Library](https://img.shields.io/badge/Library-Hugging%20Face%20🤗-yellow.svg)](https://huggingface.co/)

This project performs sentiment analysis on the viral "Pacu Jalur" meme trend that emerged on platform X (formerly Twitter) using `tweet-harvest`. The goal is to automatically gauge public opinion and capture a quantitative snapshot of the sentiment surrounding this unique Indonesian cultural phenomenon.

The core of this project is the automation of the data labeling process. Instead of manually classifying tweets, a pre-trained Indonesian sentiment analysis model from the Hugging Face hub (`mdhugol/indonesia-sentiments-classification`) was implemented to efficiently label over 500 tweets.

---

## Project Pipeline

The project was executed through the following steps:

1.  **Data Scraping:** Tweets containing the keyword "Pacu Jalur" were collected from X (Twitter) using the `snscrape` library.
2.  **Data Cleaning:** A preprocessing function was applied to clean the raw tweet text by removing usernames, URLs, hashtags, and other noise to prepare it for the model.
3.  **Automated Labeling:** A pre-trained sentiment analysis model from Hugging Face was used to automatically classify each cleaned tweet into one of three categories: `positive`, `negative`, or `neutral`.
4.  **Data Analysis & Visualization:** The resulting sentiment distribution was analyzed and visualized to understand the overall public opinion regarding the trend.

---

## Tech Stack

* **Core Language:** Python
* **Data Scraping:** `snscrape`
* **Data Manipulation:** `pandas`
* **Natural Language Processing:** Hugging Face `transformers`, `torch`
* **Data Visualization:** `matplotlib`, `seaborn`
* **Environment:** Jupyter Notebook

---

## How to Reproduce

To replicate this analysis, you can follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/](https://github.com/)[your-username]/Pacu-Jalur-Sentiment-Analysis.git
    cd Pacu-Jalur-Sentiment-Analysis
    ```

2.  **Install dependencies:**
    It's recommended to use a virtual environment.
    ```bash
    pip install pandas snscrape torch transformers
    ```

3.  **Launch the Jupyter Notebook:**
    ```bash
    jupyter notebook SentimentAnalysis_PacuJalur.ipynb
    ```
