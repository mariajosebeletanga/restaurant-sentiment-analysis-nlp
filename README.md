# restaurant-sentiment-analysis-nlp

# McGill Restaurant Sentiment Analysis

Text-based sentiment analysis of Google Maps reviews to evaluate restaurant quality and value for money around McGill University.

## 📌 Project Overview

Students frequently rely on Google star ratings when choosing where to eat. However, star ratings compress diverse customer experiences into a single number and often fail to reflect what students truly care about: price, food quality, and perceived value.

This project applies natural language processing (NLP) to Google Maps reviews to generate sentiment-based metrics that provide deeper insights beyond numerical ratings.

The goal is to better capture **value for money** through textual analysis.

---

## 📊 Data Collection

- Restaurants collected within a 500 meter radius of McGill University using the Google Maps API
- Initial dataset: 108 establishments
- Cleaned dataset: 90 unique restaurants and cafés
- Five most recent reviews per restaurant (450 reviews total)

---

## 🧠 Methodology

### Text Preprocessing
- Lowercasing
- Removal of punctuation and non-alphabetic characters
- Stopword filtering
- Tokenization
- Handling bilingual content (English + Montreal French)

### Sentiment Framework
- VADER sentiment analysis
- Extended with a custom restaurant-specific and Gen Z lexicon
- Custom polarity scoring from -5 (strongly negative) to +5 (strongly positive)
- Domain-specific lexicon overrides default VADER values

### Scoring Process
- Review-level sentiment normalized by text length
- Restaurant-level sentiment calculated as the average of five reviews
- Comparison of sentiment scores with Google star ratings using correlation analysis

---

## 📈 Key Findings

- Moderate positive correlation between star ratings and textual sentiment
- Several highly rated restaurants showed neutral or negative textual sentiment
- Some moderately rated restaurants ranked highest in sentiment due to affordability and food quality
- Text-based metrics capture nuances hidden in aggregate ratings

---

## 🎯 Impact

This project demonstrates how sentiment analysis can:

- Improve student decision-making
- Provide restaurants with clearer pricing and quality feedback
- Enhance recommendation systems beyond simple star averages

---

## 📂 Repository Structure

- `data/` – Cleaned review dataset and sentiment results
- `lexicon/` – Custom bilingual sentiment dictionaries
- `notebooks/` – Full NLP pipeline
- `report/` – Full project report

---

## 🛠 Tools & Technologies

- Python
- Pandas
- NLTK / VADER
- Custom Sentiment Lexicon
- Correlation Analysis
