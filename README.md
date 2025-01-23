# 🌟 Natural Language Processing on Amazon Book Reviews 📚

## 🚀 Overview
This project leverages advanced **Natural Language Processing (NLP)** techniques to analyze Amazon book reviews. The goal is to reveal patterns, perform market segmentation, analyze sentiment, and deliver actionable insights for book recommendations and marketing strategies. 

By combining clustering algorithms and sophisticated sentiment analysis models, this project highlights how **data-driven insights** can:
- Enhance user experiences.  
- Optimize customer targeting.  
- Influence product development in the publishing industry.

---

## 📑 Table of Contents
1. [🎯 Business Objective](#-business-objective)
2. [🛠️ Data Preprocessing and Exploratory Data Analysis](#%EF%B8%8F-data-preprocessing-and-eda)
3. [📊 Clustering Methodology and Insights](#-clustering-methodology-and-insights)
4. [💡 Sentiment Analysis](#-sentiment-analysis)
5. [⚠️ Limitations and Next Steps](#%EF%B8%8F-limitations-and-next-steps)
7. [📈 Results](#-results)
8. [📚 References](#-references)

---

## 🎯 Business Objective

This project aims to:
- **Segment and Profile Markets:** Use clustering techniques like KMeans and Hierarchical Clustering to group books based on price, votes, and reviews.
- **Sentiment Analysis:** Analyze the sentiment of book reviews to classify them as positive or negative, offering users a quick snapshot of book quality.
- **Enhance User Experience:** Provide concise sentiment summaries to save time and boost user engagement.

---

## 🛠️ Data Preprocessing and EDA

### 📂 Dataset Overview
- **Source:** Amazon Book Reviews Dataset.
- **Original Size:** 20GB (27M rows of reviews) + 4GB metadata.
- **Sample Used:** ~21,000 reviews, downsized for computational feasibility.

### 🔄 Preprocessing Steps
1. **Merging Datasets:** Combined metadata with reviews using the ASIN (unique product ID).
2. **Handling Missing Values:**
   - Missing votes set to `0`.
   - Missing prices filled with median values.
   - Null styles replaced with "unknown."
3. **Feature Engineering:**
   - Extracted `year`, `month`, and `day_of_week` from review timestamps.
   - Calculated `total_review_count` per book.
4. **Column Transformations:** Resolved formatting inconsistencies and cleaned text data.
5. **Data Cleaning:** Removed unused columns and reformatted dictionaries (e.g., `style` column).

### 🔍 Exploratory Data Analysis
- Distribution of book ratings and formats.
- Genre analysis.
- Price and review correlations.

---

## 📊 Clustering Methodology and Insights

### 🔬 Methods Used
1. **KMeans Clustering**
   - Optimal clusters determined using elbow and silhouette plots.
   - Chosen clusters: **5**.
2. **Hierarchical Clustering**
   - Optimal clusters analyzed via silhouette scores.
   - Resulted in consistent **5 clusters**, similar to KMeans.

### 💡 Key Insights
- **Cluster 1:** High user engagement, significant votes on reviews.
- **Cluster 5:** Niche market of expensive books, average price: $690.15.
- Diverse patterns across clusters in terms of pricing, sentiment, and review credibility.

---

## 💡 Sentiment Analysis

### 🧠 Methodology
1. **Preprocessing Reviews:**
   - Converted text to lowercase, removed non-alphanumeric characters, and applied lemmatization.
2. **Sentiment Scoring:**
   - Calculated cosine similarity between reviews and ideal positive/negative sentiment vectors.
3. **Models Evaluated:**
   - Custom Word2Vec model.
   - Pre-trained Word2Vec (Google News).
   - Pre-trained GloVe (Global Vectors).
   - **Best Performing Model:** GloVe.

### 📊 Results
- Most reviews showed positive sentiment (range: 0.2 - 0.4).
- Strong correlation between 5-star ratings and positive sentiment.
- Non-fiction genres performed better than fiction.

---

## ⚠️ Limitations and Next Steps

### ⚠️ Limitations
- Multiple versions of the same book may skew results.
- Sentiment aggregation at the word level lacks context.
- Small sample size reduces statistical significance.

### 🔮 Next Steps
- Scale the analysis to the full dataset for greater insights.
- Develop advanced models to capture context and key sentence-level sentiment.
- Explore additional features like reviewer demographics and book themes.

---

## 📈 Results

### 📊 Clustering
- Generated clusters provided insights into user behavior and market segments.
- Cluster visualizations available in `/results/clustering/`.

### 📖 Sentiment Analysis
- Top genres by sentiment:
  1. Non-fiction
  2. Mixed media books
- Example visualization: Sentiment vs. Rating correlation graph.

### 📏 Performance Metrics
- **Model Score:** Difference in cosine similarities between positive and negative vectors.

---

## 📚 References
- Amazon Review Data: [Nijianmo et al.](https://nijianmo.github.io/amazon/)
- Bing Liu et al. "Mining and Summarizing Customer Reviews" (KDD-2004)
- McAuley et al. "Empirical Methods in NLP" (EMNLP, 2019)

---

## 🤝 Contributors
- Dhruv Shah
- Jenn Hong
- Santiago Mazzei
- Setu Shah
- Victor Floriano

---

Thank you for exploring this project! 🚀 Feel free to contribute or share your thoughts through issues and pull requests.

