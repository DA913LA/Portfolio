# Portfolio
This is a collection of my projects focused on AI, Data science and analytics.

# Analysis of UK Accident Data
**Introduction**
This project analyzes UK accident data to explore contributing factors and predict accident severity. The goal is to provide actionable recommendations to the government for improving road safety.

**Data Description and Cleaning**
The dataset consists of accident, vehicle, casualty, and LSOA tables with 220,435 rows and 90 columns. Data cleaning involved imputing missing values, addressing underage drivers by replacing them with the average driver age, and converting dates to a proper datetime format. The relevant features were cleaned for further analysis.

**Insights**
Accidents by Time and Day: The highest frequency of accidents occurs on Fridays, likely due to workweek stress, and during rush hours (8 AM, 3-5 PM).
Motorcycle Accidents: Motorbikes over 50cc and up to 125cc are most involved in accidents during rush hour, especially on Sundays.
Pedestrian Accidents: Peak times for pedestrian involvement in accidents are also during rush hours, with fewer incidents on Sundays.
Accident Severity: Using the Apriori algorithm, factors like road surface condition and number of vehicles were found to impact accident severity, particularly in “slight” accidents.
Accident Clusters: K-means clustering identified accident hotspots in major cities like Hull, Scunthorpe, and Grimsby.
Outliers: Outliers in the dataset were found in urban areas and were not removed, as they reflect real-world occurrences.

**Prediction**
A Random Forest classifier was used to predict accident severity, achieving 83.41% accuracy initially. After addressing class imbalance using SMOTE, the accuracy increased to 93%, with improved precision and recall.

**Recommendations**
Increase traffic measures during rush hours, such as traffic officers and crossing guards.
Implement lower speed limits for motorcycles, especially those between 50cc-125cc and over 500cc.
Enhance surveillance in accident-prone cities (e.g., Hull, Scunthorpe) through speed cameras and police officers.
Strengthen emergency medical services to reduce fatalities by increasing the number of ambulances and reducing response times.


# Analysis of Census Data for Town Development
**Introduction**
This project analyzes census data to identify trends and insights that inform decisions on what to build and invest in on an empty plot of land. The town is located between two larger cities and relies on its neighboring cities for certain infrastructures. The analysis involves data cleaning, population demographics, birth rates, employment, and other key factors to guide investment recommendations.

**Data Cleaning**
The dataset includes columns like house number, street, age, occupation, marital status, and gender. Key cleaning steps:

Missing first names were filled with "unknown," and missing surnames were inferred from household data.
Missing ages were imputed based on occupation.
Inconsistent occupation entries were cleaned and a new column for "Employment status" was created.
Religion outliers (e.g., "Jedi") were replaced with placeholders.

**Key Insights**
Age Distribution: The population is mostly women aged 30-49. A lower number of students compared to young children suggests a declining birth rate and a trend of migration after education.
Birth Rate: The current birth rate is 156 per 1000 age-bearing women, a decline from 199 per 1000 four years prior, suggesting fewer babies born recently.
Employment: The unemployment rate is 10% of the working population. The largest unemployed group is aged 35-49.
Commuters: 77.5% of the population commutes, likely due to a lack of local jobs.
Overcrowded Housing: 51% of homes are overcrowded, largely due to singles, lodgers, and divorcees living in high-density housing.

**Recommendations**
Train Station: Due to the high commuter population, building a train station will benefit the town's residents.
Housing: Build more low-density housing to reduce overcrowding and accommodate the growing population and immigrant inflow.
Schools: With a growing population of young children, increased investment in schools is necessary.
Elderly Care: With an expected increase in retirees, end-of-life care facilities should be prioritized for future investment.


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

