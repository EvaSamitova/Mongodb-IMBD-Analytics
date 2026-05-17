# 📊 Visualizing Movie Details with MongoDB Atlas Charts

| Key | Value |
|------|------|
| Assignment | MongoDB Atlas Charts Tutorial |
| Author | Eva Samitova |
| Technologies | MongoDB, Python, Pandas, Jupyter |
| Focus Area | NoSQL Analytics & Data Visualization |

---

## Introduction

This tutorial demonstrates how to connect MongoDB Atlas movie datasets with Python and visualize movie analytics data using MongoDB Atlas Charts and Pandas workflows.

The tutorial explores:
- MongoDB database connections
- Querying movie collections
- Using regex filters
- Retrieving movie records into Pandas
- Working with JSON-based movie documents
- Visualizing movie ratings and award data

The dataset contains movie information including:
- titles
- genres
- ratings
- directors
- cast members
- awards
- critic reviews
- release dates

---

# Connect to a MongoDB Server

The following example demonstrates how to establish a secure MongoDB connection using `pymongo` and `certifi`.

```python
import pymongo
import certifi

# Connect to the database using known good certificates
client = pymongo.MongoClient(secret_key, tlsCAFile=certifi.where())

print(f"Using MongoDB version {client.server_info()['version']}.")
```

---

# Read Data into Pandas

This example shows how to retrieve MongoDB collection data and convert it into a Pandas DataFrame for analysis.

```python
import pandas as pd

# Retrieve all records from a collection
cursor = da320_database["Metacritic"].find()

# Convert this information into a Pandas dataframe
metacritic = pd.DataFrame(cursor)

# Preview the data
metacritic.head()
```

---

# Query a Subset of Data

MongoDB queries can be combined with regex filtering to locate records matching specific keywords.

```python
query = { "description": { "$regex": "(China|Chinese)" } }

cursor = da320_database["Metacritic"].find(query)

metacritic = pd.DataFrame(cursor)

metacritic.head()
```

---

# Example Dataset Structure

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
    "wins": 2
  }
}
```

---

# Display Images Inside Pandas

This example demonstrates how to render image thumbnails directly inside a Pandas dataframe.

```python
from IPython.core.display import HTML

# Create a formatter to convert URLs into inline images
def path_to_image_html(path: str):
    return f"<img src=\"{path}\" width=\"120\" />"

# Tell Pandas to use the formatter for the thumbnail column
formatters = dict(thumbnail = path_to_image_html)

# Convert dataframe to HTML
html = metacritic.to_html(escape = False, formatters = formatters)

HTML(html)
```

---

# Sort Data in Pandas

```python
# Sort movies by release date
earliest_release_date_first = metacritic.sort_values(by=['release_date'])

earliest_release_date_first.head()
```

---

# Skills Demonstrated

- MongoDB Atlas connectivity
- NoSQL querying
- Regex-based filtering
- JSON document analysis
- Pandas workflows
- Jupyter Notebook usage
- Movie dataset analytics
- Exploratory data analysis (EDA)

---

# Learning Outcomes

Through this tutorial, I practiced:
- connecting MongoDB collections to Python
- retrieving and transforming movie datasets
- querying semi-structured data
- working with JSON documents
- combining MongoDB with Pandas for analytics workflows
- visualizing movie-related datasets

---

# Technologies Used

- Python
- MongoDB Atlas
- Pandas
- pymongo
- certifi
- Jupyter Notebook
