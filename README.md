# Portfolio
This is a collection of my projects focused on AI, Data science and analytics.

# Sentiment Analysis on Drug Reviews
**Introduction**
This project focuses on using natural language processing (NLP) for sentiment analysis on drug reviews. The aim is to analyze patients’ reviews and classify them into positive, neutral, or negative sentiments. Sentiment analysis in the pharmaceutical industry can provide insights to healthcare professionals and stakeholders to improve patient drug experiences.

**Dataset**
The UCI Drug Review dataset was used, which contains 215,063 patient reviews. The reviews were categorized into three sentiment classes: positive, neutral, and negative based on the drug rating provided. The dataset exhibited class imbalance, which was addressed using the Synthetic Minority Over-sampling Technique (SMOTE).

**Methods**
Data Preprocessing: Text reviews were preprocessed by removing punctuation, converting to lowercase, tokenizing, lemmatizing, and removing stopwords.
Traditional Machine Learning Models: Implemented Naive Bayes and Decision Trees with TF-IDF for feature extraction. The decision tree model achieved a test accuracy of 0.82 after using bigrams to improve feature representation.
Deep Learning Models: Used LSTM and CNN architectures to capture long-range relationships and features in the text. The LSTM model achieved the best performance with a test accuracy of 0.73 and an F1-score of 0.7289.

**Results**
The best-performing traditional model was the Decision Tree with bigrams, achieving a test accuracy of 0.82.
The best deep learning model was the LSTM, achieving a test accuracy of 0.73 and an F1-score of 0.7289, outperforming the CNN model.

**Conclusion**
Deep learning models, particularly LSTM, outperformed traditional models in sentiment analysis of drug reviews. However, traditional models like Decision Trees can still be useful in resource-limited situations due to their simplicity and efficiency.

