# 🔥 Forest Fire Sentiment Analysis (Karhutla)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Platform](https://img.shields.io/badge/Platform-Google%20Colab-orange)
![Library](https://img.shields.io/badge/Library-Scikit--Learn%20%7C%20Pandas%20%7C%20Seaborn-green)

This project aims to analyze public sentiment on social media (Twitter/X) regarding the issue of **Forest and Land Fires (Karhutla)** in Indonesia. It covers the entire Data Science pipeline, ranging from text preprocessing and lexicon-based automatic labeling to sentiment classification using Machine Learning.

## 📌 Background
Forest fires are a critical environmental issue that triggers various public reactions. This analysis classifies public opinion into three categories: **Positive**, **Negative**, and **Neutral** to understand how the community perceives the handling and impact of these events.

## 📂 Dataset
* **Source**: Twitter Data (`Data_Kebakaran_Hutan.csv`).
* **Key Features**: Tweet Text, Date, Time, Username.
* **Size**: ~1,000+ tweets (after deduplication).

## 🛠️ Methodology & Workflow
The project utilizes **Natural Language Processing (NLP)** techniques with the following steps:

1.  **Data Preprocessing**:
    * **Cleaning**: Removing URLs, HTML tags, mentions (@), emojis, numbers, and punctuation.
    * **Case Folding**: Converting text to lowercase.
    * **Normalization**: Converting non-standard/slang words into standard Indonesian words using an external dictionary.
    * **Tokenization**: Splitting sentences into individual words.
    * **Stopword Removal & Stemming**: Removing common words and reducing words to their root forms.

2.  **Data Labeling**:
    * Implemented a **Lexicon-Based** approach using the *InSet (Indonesian Sentiment Lexicon)* dictionary.
    * Scoring logic: `(Positive Score - Negative Score)` to determine the sentiment class.

3.  **Exploratory Data Analysis (EDA)**:
    * **WordCloud**: Visualizing the most frequent words before and after cleaning.
    * **Bar Chart**: Visualizing the distribution of sentiment classes.

4.  **Modeling (Machine Learning)**:
    * **Algorithm**: Support Vector Machine (SVM).
    * **Task**: Multi-class text classification (Positive, Negative, Neutral).

## 📊 Evaluation Results
The SVM model achieved excellent performance on the test data:

| Metric | Result |
| :--- | :--- |
| **Accuracy** | **~94.6%** |

*The result is based on the Confusion Matrix, showing a high number of correct predictions across all three sentiment classes.*

## 🚀 How to Run
This project was developed using **Google Colab**.

1.  Clone this repository:
    ```bash
    git clone https://github.com/nazarDA/SentimentAnalisisKarthula.git
    ```
2.  Open the `.ipynb` file in Google Colab or Jupyter Notebook.
3.  Ensure the dataset `Data_Kebakaran_Hutan.csv` is available (or adjust the `gdown` code in the notebook).
4.  Run the cells sequentially.

## 📚 Libraries Used
* `pandas` & `numpy` - Data manipulation.
* `matplotlib` & `seaborn` - Data visualization.
* `wordcloud` - Text visualization.
* `sklearn` - Machine Learning modeling (SVM) and evaluation.
* `googletrans` - Translation utilities (if applicable).

---
**Author:** [nazarDA]
