# 🏨 Hotel Recommendation System

An end-to-end project that **collects, analyses and recommends** hotels: data is scraped from the web, explored visually, and served through a Streamlit app that matches hotels to a free-text description of what the user wants.

## Pipeline

```
Web scraping (Scrapy)  →  Data cleaning & EDA (Pandas, Seaborn)  →  Recommendation app (Streamlit + spaCy)
     hoteldata.json            HotelDataVisualization.ipynb               streamlit_app.py
```

1. **Collect** — a Scrapy spider (`items.py`, `pipelines.py`, `settings.py`) gathers hotel listings into `hoteldata.json`.
2. **Analyse** — `HotelDataVisualization.ipynb` cleans the data, summarises it into `hotel_summary.csv` and visualises patterns, including word clouds of what guests talk about.
3. **Recommend** — in `streamlit_app.py` the user picks a location and describes the stay they want in plain English; spaCy compares that text with guest reviews using semantic similarity and returns the best-matching hotels.

## What this project shows

- Building a dataset from scratch rather than starting from a ready-made CSV
- Exploratory analysis and visual storytelling
- Applying NLP (semantic similarity on reviews) to build a useful, user-facing product

## Tech stack

Python · Scrapy · Pandas · NumPy · Matplotlib · Seaborn · WordCloud · spaCy · Streamlit

## Run locally

```bash
pip install streamlit pandas numpy spacy
python -m spacy download en_core_web_sm
streamlit run streamlit_app.py
```

---

Made by [Vanshika Gupta](https://github.com/itsvanshika) · [LinkedIn](https://linkedin.com/in/itsvanshikaa)
