# FAKE NEWS CLASSIFIER

## Introduction
The rapid spread of misinformation and fake news on digital platforms has become a growing concern, particularly in areas of politics, public health, and social issues. With millions of people consuming news online, the ability to automatically identify and flag fake news is critical to maintaining information integrity. 

This project aims to develop a machine learning model that can classify news headlines as real or fake based on their textual content. Using a labelled dataset of headlines, the project involves:

- Pre-processing the text
- Transforming it using TF-IDF vectorization
- Training a Naive Bayes classifier to detect patterns that distinguish fake news from real news  

The ultimate goal is to build a reliable and interpretable fake news detection system, supported by appropriate evaluation metrics and exploratory data analysis.

## Objective
To build a machine learning model that classifies news headlines as real or fake, helping to reduce the spread of misinformation online.

## Tools & Libraries Used
- **Python**
- **Pandas** – for data manipulation
- **Matplotlib & Seaborn** – for data visualization
- **NLTK** – for text pre-processing (tokenization, stop words, lemmatization)
- **Scikit-learn** – for model training and evaluation
- **WordCloud** – for visualizing frequent words in fake and real news

## Process

### 1. Loading the Data
- Used a dataset with headlines and their labels:
  - `0` = Fake
  - `1` = Real

### 2. Exploring the Data (EDA)
- Checked:
  - How many fake and real headlines there were
  - Length of the headlines  
- Findings:
  - Fake headlines were generally longer
  - Word clouds showed:
    - Fake headlines used words like *“new york”*, *“trump”*, *“breitbart”*
    - Real headlines used more informative and mixed words like *“report”*, *“official”*, *“video”*

### 3. Cleaning the Text (Pre-processing)
Text cleaning steps:
- Converted all words to lowercase
- Removed punctuation and symbols
- Removed common short words (stop words) like *“the”*, *“and”*, *“is”*
- Lemmatized words (e.g., *“running” → “run”*)

### 4. Turning Text into Numbers (TF-IDF)
- Used **TF-IDF** to convert text into numerical features for modeling
- TF-IDF gives higher scores to words important for distinguishing fake vs real news

### 5. Building the Model
- Used a **Naive Bayes** classifier, common for text classification
- Split data into training and testing sets (80/20)
- Trained the model on clean text and evaluated performance

### 6. Results and Insights
- Model performance:
  - **Accuracy:** 89% (almost 9 out of 10 correct)
  - **Fake news:**
    - Precision: 85%
    - Recall: 95%
  - **Real news:**
    - Precision: 94%
    - Recall: 83%
- Insights from EDA:
  - Fake news headlines tend to be longer and contain repeated media references (possibly to appear credible)
  - Real news headlines have more variety in language, reflecting editorial standards

## Conclusion
The project successfully built a model that predicts whether a headline is fake or real. With basic tools and a clean dataset, high accuracy was achieved. This demonstrates how machine learning and text pre-processing can help combat misinformation online.

