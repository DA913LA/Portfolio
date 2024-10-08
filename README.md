# Portfolio
This portfolio showcases a collection of my projects centered around artificial intelligence, data science, and analytics.

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

# Analyzing Second Hand Car Sales Data with Supervised and Unsupervised Learning Models
**Introduction**
This project explores predictive models for second-hand car prices using both numerical and categorical features. Multiple regression models (Linear Regression, Random Forest Regressor, and Artificial Neural Networks) are employed, along with k-Means clustering, to evaluate performance in predicting car prices.

**Methodology**
Dataset: The dataset includes details such as manufacturer, engine size, year of manufacture, mileage, and price.

Data Preprocessing: Data cleaning involved removing outliers and duplicates. Boxplots and heatmaps were used to explore relationships between features.
Regression Models

Single Numerical Features: Year of manufacture was the best predictor with an R² score of 0.77 using polynomial regression.

Multiple Linear Regression & Random Forest: Random Forest outperformed multiple linear regression with a higher R² score of 0.92 and a lower MSE of 12,167,556.

Random Forest (Numerical + Categorical): Including categorical features further improved accuracy, achieving an R² score of 0.998 and an MSE of 261,289.62.
Artificial Neural Networks (ANN): An ANN model was constructed with two hidden layers, achieving the lowest MSE of 4,997.49, outperforming previous models.
Clustering Models

k-Means Clustering: Applied to different numerical feature combinations. The best result was obtained using 'Year of manufacture' and 'Mileage' with a silhouette score of 0.62 and a Davies-Bouldin index of 0.51.

k-Means vs. Hierarchical Clustering: Hierarchical clustering had a slightly higher silhouette score (0.58) but required more clusters (k=3).

**Conclusion**
Year of manufacture and mileage were the most influential features in predicting car prices. Among models, the ANN performed best, and the inclusion of both numerical and categorical features significantly enhanced prediction accuracy.

# Image Recognition to Identify Flower Species Using CNNs
**Introduction**
This project applies Convolutional Neural Networks (CNNs) to classify images of flowers into five species daisy, dandelion, rose, sunflower, and tulip. The TensorFlow flowers dataset contains 3670 images, and the CNN is designed to accurately classify these species, despite the variations in color, texture, and background. The goal is to optimize the model using regularization and hyperparameter tuning.

**Dataset and Preprocessing**
Dataset 3670 images of five flower species.
Data Splitting 80% training, 20% testing.
Data Augmentation Applied horizontalvertical shifts, flips, rotation, and zoom to prevent overfitting. Images were normalized to pixel values between 0 and 1.

**Model Architecture**
The CNN architecture includes

Conv2D layers with small 3x3 filters and ReLU activation.
MaxPooling layers for spatial invariance.
Dropout layers to prevent overfitting (0.25 and 0.5).
Dense layers with softmax for classification.
Model Training
Regularization Dropout (0.5) was applied to reduce overfitting.
Hyperparameter Tuning Learning rate, batch size, and dropout rates were tuned. Optimal hyperparameters were selected after experimenting with multiple combinations.
Hyperparameter Tuning Results
Best Results A combination of 10 epochs, 0.001 learning rate, 0.5 dropout, and 128 batch size yielded the highest validation accuracy of 0.8822.
Overfitting Analysis Training and validation accuracy and loss curves showed no signs of overfitting, confirming that regularization and hyperparameter tuning were effective.

**Conclusion**
The CNN model effectively identified flower species with high accuracy. Regularization techniques and careful tuning of hyperparameters led to significant improvements in the model’s performance without overfitting. The final validation accuracy achieved was 88.22%.

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

