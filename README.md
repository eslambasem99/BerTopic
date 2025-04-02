# BERTopic for Topic Modeling

## 📌 Introduction
Topic modeling is one of the most important techniques in **Natural Language Processing (NLP)**. It is used to extract topics from unstructured text data. In this project, you will be able to implement a complete **BERTopic**-based topic modeling system, starting from data loading and cleaning to building an effective model for topic analysis.

## 📊 Project Features
- Load and process a news dataset containing **31,000 articles** from multiple sources.
- Apply data cleaning strategies such as removing links, numbers, and unnecessary symbols.
- Utilize **BERTopic** to extract topics using advanced techniques like **Transformers**.
- Reduce dimensionality and analyze data using **Dimensionality Reduction** and **Clustering**.
- Analyze topic evolution over time and discover trends in the data.
- Use visualization tools such as **Histogram** and **Heatmap** to understand topic distribution and relationships.
- Improve the model by merging similar topics and reducing noise.
- Implement techniques like **Stopwords Removal** to enhance model accuracy.
- Practical application of classifying new articles based on extracted topics.
- Provide insights on handling large datasets and utilizing cloud computing resources for performance optimization.

## 🛠 Requirements
Before running the project, ensure you have installed the following dependencies:

```bash
pip install bertopic pandas seaborn matplotlib scikit-learn
```

## 🚀 How to Use
1. **Load Data**
   - Use any text dataset, such as news articles, blogs, or tweets.
   - Ensure the dataset contains columns like (`text`, `source`, `date`).

2. **Run the Project**
   - Open **Google Colab Notebook** or **Jupyter Notebook**.
   - Import and clean the dataset using Pandas.
   - Apply **BERTopic** for topic modeling.
   
```python
from bertopic import BERTopic
import pandas as pd

# Load data
data = pd.read_csv("news_dataset.csv")

# Apply BERTopic
topic_model = BERTopic()
topics, probs = topic_model.fit_transform(data["text"].tolist())

# Display extracted topics
print(topic_model.get_topic_info())
```

3. **Analyze Results**
   - Visualize extracted topics using different charts.
   - Analyze topic trends over time using `visualize_barchart()` and `visualize_topics_over_time()`.

```python
import matplotlib.pyplot as plt

topic_model.visualize_barchart()
topic_model.visualize_topics_over_time()
plt.show()
```

## 📷 Example Outputs
- A list of extracted topics ranked by importance.
- Analytical charts illustrating topic evolution over time.
- Automatic clustering of similar texts into distinct topics.

## 🤝 Contribution
If you would like to improve this project, feel free to submit a **Pull Request** or open a new **Issue**!

## 📜 License
This project is licensed under the **MIT License**, allowing you to use and modify it freely.

---
✨ **This project was developed to facilitate large-scale text analysis using modern techniques!**

