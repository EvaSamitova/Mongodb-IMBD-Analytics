# 📊 Visualizing Movie Details with MongoDB Atlas Charts

## Overview

This tutorial demonstrates how to use MongoDB Atlas Charts to visualize movie analytics data from the Mflix sample dataset.

The walkthrough focuses on:
- MongoDB Atlas integration
- Movie dataset exploration
- Filtering and aggregation
- Multi-series chart creation
- Data visualization workflows
- NoSQL analytics concepts

The dataset contains information about movies, ratings, genres, awards, reviews, and production details.

---

## 🎬 Sample Dataset Structure

Example document from the Mflix dataset:

```json
{
  "title": "Dracula",
  "year": 1931,
  "genres": ["Horror"],
  "runtime": 85,
  "imdb": {
    "rating": 7.6,
    "votes": 30184
  },
  "awards": {
    "wins": 2,
    "nominations": 1
  },
  "countries": ["USA"]
}
```

---

## 📈 Charts Created

### 1. Sorted Column Chart

This chart displays:
- Directors with at least 50 total awards
- Award totals grouped by movie genre
- Data sorted from highest to lowest

The visualization helps identify:
- High-performing directors
- Popular award-winning genres
- Genre distribution across directors

---

### 2. Scatter Plot Visualization

The scatter chart visualizes:
- Award-winning movies
- TomatoMeter ratings
- MPAA ratings
- Audience and critic review trends

This chart helps explore:
- Relationships between ratings and awards
- Movie classification patterns
- Review score distribution

---

## 🛠 Technologies Used

- MongoDB Atlas
- MongoDB Atlas Charts
- Python
- Pandas
- Jupyter Notebook
- NoSQL queries

---

## 🔍 Skills Demonstrated

- MongoDB database querying
- NoSQL data exploration
- Data visualization
- Aggregation and filtering
- Exploratory data analysis (EDA)
- Dashboard and chart creation
- Movie analytics workflows

---

## 📚 Learning Outcomes

Through this project, I practiced:
- Connecting MongoDB collections to analytics workflows
- Building interactive charts using Atlas Charts
- Querying movie datasets using filters and aggregation logic
- Visualizing structured and semi-structured data
- Combining MongoDB with Python and Pandas for analysis

---

## 🚀 Future Improvements

Potential future enhancements include:
- Interactive dashboards
- Advanced aggregation pipelines
- Sentiment analysis on movie reviews
- Machine learning recommendation systems
- Real-time analytics integration

---

## 📌 Dataset Source

MongoDB Atlas Sample Dataset — Mflix Movies Collection
