# Intel-Product-Review-Sentiment-Analysis

Welcome to the Intel Product Review Sentiment Analysis project! In this project, we will be using natural language processing techniques to analyze the sentiment of Intel product reviews.

## Table of Contents
- [Project Overview](#project-overview)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Usage](#usage)
- [Project Details](#project-details)
  - [Data Collection](#data-collection)
  - [Data Preprocessing](#data-preprocessing)
  - [Sentiment Analysis](#sentiment-analysis)
  - [Evaluation](#evaluation)
- [Conclusion](#conclusion)
- [References](#references)

## Project Overview

The goal of this project is to perform sentiment analysis on Intel product reviews in order to understand the overall sentiment of the reviews and how it changes over time. We will be using the Python Natural Language Toolkit (nltk) library to perform the sentiment analysis.

## Getting Started

### Prerequisites

In order to run the code in this repository, you will need to have the following software installed on your machine:

- Python 3
- Jupyter Notebook

You will also need to install the following Python libraries:

- nltk
- numpy
- pandas
- matplotlib
- seaborn
- pickle

### Installation

To install the required libraries, open a terminal window and run the following command:

```bash
pip install nltk numpy pandas matplotlib seaborn pickle
```
Once the libraries are installed, clone or download this repository to your local machine.

### Usage
To use this repository, open the Jupyter notebook file `Sentiment_Analysis.ipynb` in your local machine. Follow the instructions in the notebook to scrape reviews for a specific product and perform sentiment analysis on the reviews.

## Project Detials
The project is divided into the following sections:

### Data Collection
In this section, we will scrape reviews for different Intel product using the Selenium library. The `scraper.py` file contains the scraping code which will extract reviews from the links.txt file within the Scraper folder. Each dictionary represents a single review and contains the following information:
- `rating` : The rating of the product
- `content` : The review content
- `variant` : The variant purchased
- `name` : The reviewer name
- `date` : The review date
- `verified` : Status if the user is verified or not
- `sub_reviews` : The sub-review content if it exists

The extracted reviews are stored in a csv file named `final_reviews.csv`. To extract reviews for different products, the `links.txt` file should be edited with the required links. 

### [DataSet](https://drive.google.com/file/d/10sEg2LtHh5xGTxMgjU8AcIahqBr-Ww6d/view?usp=sharing)

### Data Preprocessing
In this section, we will preprocess the data by performing the following tasks:
- Checking for null values
- Removing stop words
- Upsampling minority classes
- Stemming the tokens

### Exploratory Data Analysis (EDA)
In this section we will try to explore the data. `Wordcloud` is used to visualize the most frequently used words associated with each category of reviews. `CountVectorizer` feature of sklearn is used to plot the top 20 most frequent bigrams.

### Sentiment Analysis
`TfidfVectorizer` is utilized to transform text data into numerical features that represent the importance of words in reviews relative to the entire dataset. We will use the `Logistic Regression model` to perform sentiment analysis on the preprocessed review text. We will also use the **`Pickle`** library to check the models prediction for a random sentiment.

### Evaluation
In this section, we will evaluate the performance of the sentiment analysis model. We will calculate the following evaluation metrics:

- Accuracy: the proportion of correctly classified reviews

## Conclusion
In this project, we have demonstrated how to perform sentiment analysis on Intel product reviews using the nltk library. We have also shown how to evaluate the performance of the sentiment analysis model.

## References
- Natural Language Toolkit (nltk): **[https://www.nltk.org/](https://www.nltk.org/)**
- Pandas: **[https://pandas.pydata.org/](https://pandas.pydata.org/)**
- Matplotlib: **[https://matplotlib.org/](https://matplotlib.org/)**
