# SLEEP-HEALTH-AND-LIFESTYLE-ANALYSIS
DSML Entri Capstone Project

### 1. Overview of Problem Statement:

According to the National Institutes of Health (NIH), quality sleep is as important to good health as diet and exercise. Regularly missing adequate quality sleep can raise the risk of a range of health issues, such as heart disease, stroke, obesity and dementia. The NIH recommends seven to nine hours of sleep a night for the average person.Sleep health refers to the quality, duration, timing, and regularity of sleep, as well as the behaviors and habits that promote optimal sleep. It encompasses both the physiological aspects of sleep and the psychological and environmental factors that influence sleep patterns. It is essential for one's overall well-being and is associated with numerous physical, cognitive, and emotional benefits.When sleep health is prioritized, it can lead to improved mood, cognitive function, immune function, cardiovascular health, and overall quality of life. Conversely, chronic sleep deprivation or poor sleep quality can contribute to a range of negative outcomes, including increased risk of obesity, diabetes, cardiovascular disease, depression, and impaired cognitive performance. Therefore, adopting habits and behaviors that support good sleep health is crucial for optimal functioning and well-being.

  
 2.Objective:

⌛ How is Fitness tied to Sleep Health

Fitness plays a significant role in sleep health, as regular physical activity has been shown to positively influence both the quality and duration of sleep. Regular exercise has been associated with shorter sleep onset latency, meaning it may help individuals fall asleep more quickly after going to bed (including those with sleeping disorders. Beyond its direct effects on sleep, regular exercise is associated with numerous health benefits, including reduced risk of stress, obesity, cardiovascular disease, and depression, all of which can impact sleep health.


3.Data Description:
Source: The dataset can be downloaded from the link :(https://www.kaggle.com/code/giulianoverdone/up-to-date-sleep-health-and-lifestyle-analysis?select=Sleep_Data_Sampled.csv

Recognizing Variables in the Dataset
 * Person ID: An identifier for each individual.
 * Sex: The sex of the person (Male/Female).
 * Age: The age of the person in years.
 * Occupation: The occupation or profession of the person
 * Sleep Duration (hours): The number of hours the person sleeps per day.
 * Quality of Sleep (scale: 1-10): A subjective rating of the quality of sleep, ranging from 1 to 10.
 * Physical Activity Level (minutes/day): The number of minutes the person engages in physical activity daily.
 * Stress Level (scale: 1-10): A subjective rating of the stress level experienced by the person, ranging from 1 to 10.
 * BMI Category: The BMI category of the person (e.g., Underweight, Normal, Overweight).
 * Blood Pressure (systolic/diastolic): The blood pressure measurement of the person, indicated as systolic pressure over diastolic pressure.
 * Heart Rate (bpm): The resting heart rate of the person in beats per minute.
 * Daily Steps: The number of steps the person takes per day.
 * Sleep Disorder: The presence or absence of a sleep disorder in the person (Healthy, Insomnia, Sleep Apnea)

Sleep Disorder-Target
 * Healthy: The individual does not exhibit any specific sleep disorder.
 * Insomnia: The individual experiences difficulty falling asleep or staying asleep, leading to inadequate or poor-quality sleep.
 * Sleep Apnea: The individual suffers from pauses in breathing during sleep, resulting in disrupted sleep patterns and potential health risks.

 
4. Data Collection
   
 * The dataset used for this project was sourced from Kaggle.
 * The dataset was downloaded in CSV format and used for further processing.


5. Data Preprocessing and Analysis

  1.Loading and Cleaning Data:
  
  Steps Taken:
  * Loaded the dataset using pandas.
  * Examined missing values and duplicates.
  * Handled the missing values using imputaion.
  * Checked the descriptive statistics of the data .
  * Removed irrelevant features and duplicate entries.
  * This data set doesn't have any missing values or duplicates.
  * Checked for skewness of the data.

 Insights:
  * Proper data preprocessing ensured that the dataset was clean and ready for machine learning models.

  2️. Outlier Detection & Treatment
  
  Steps Taken:
  * Used boxplots to visualize and detect outliers in numerical variables.
  * Create a funcion "handling_outliers" based on IQR method for handling outliers. 
  * Clipped extreme values using "handling_outliers" function.
  * Visually checked whether the outliers are handled properly or not using boxplots.
  * Checked for skewness of the data after clipping. The skewness values were within the range so didn't go for any transformation techniques.
    
 Insights:
  * Outlier detection helped in identifying extreme values that could negatively affect model performance.
  * Clipping ensured that the dataset maintained its integrity while avoiding overfitting to extreme values.

     
6. Exploratory Data Analysis (EDA)
   
   1.Univariate Analysis
   
  * Analysed numerical variables using Histplot
  * count plot for categorical column-Sleep Disorder.
  * count plot for categorical column-BMI Category
    
   2.Bivariate Analysis
   
  * Correlation Heatmap for checking correlation between the features.
  * Scatter plot-Age vs Sleep Duration
  * Scatter Plot- Age vs Sleep Duration
  * Bar chart of Heart Rate vs Stress Level
  * Bar chart of Stress Level vs Sleep Duration
  * violin plot of BMI Category vs Stress Level
  * Horizontal bar chart of Occupation vs Stress Level

  3.Multivariate Analysis
  * pairplot
        
 Insights:
  * After encoding the number of features increased  to 45.
  * Using all these 45 features for model building is not advisable, so went for feature selection.

7. Feature Encoding
   
 Steps Taken: 
  * Encoded categorical variables (e.g: "Gender","Occupation","BMI Category", "Blood Pressure") using one-hot encoding.
  Insights:
  * After encoding the number of features increased  to 45.
  * Using all these 45 features for model building is not advisable, so went for feature selection.

    
8. Feature Selection
   
   1.Feature Importance Analysis:
   * Feature Selection Using Random Forest Random Forest is an ensemble learning method.
   * Feature importance scores from  Random Forest Classifier helped to select 12 most important features by setting the threshold as 0.02.

  
9.Split Data into Training and Testing Sets
  * Split the dataset into: X_selected → Features y → Target variable (Sleep Disorder)
  * Split the dataset into 80% training and 20% testing data.
  * Ensured stratified splitting to maintain class distribution.


10. Feature Scaling
  * Standardized numerical features using StandardScaler.
  * Ensured consistent scaling across features to prevent magnitude bias.
  * Used X_tain_scaled and X_test _scaled for 

11.Model Building

  1.   Support Vector Machine(SVC-Support Vector Classifier)
  2.   KNeighbors Classifier
  3.   Naive Bayes
  4.   Decision Tree Classifier
  5.   Random Forest Classifier
  6.   Gradient Boosting Classifier

 Steps Taken:
 * Used X_tain_scaled and X_test_scaled for the models Support Vector Machine(SVC-Support Vector Classifier),KNeighbors Classifier and  Naive Bayes.
 * Used X_tain and X_test for the tree based models Decision Tree Classifier,Random Forest Classifier and Gradient Boosting Classifier.
   
    
12.Model Evaluation

 1.Evaluated models based on:
  * Accuracy: Measures overall correctness.
  * Precision: Measures true positives out of all predicted positives.
  * Recall: Measures true positives out of actual positives.
  * F1 Score: Harmonic mean of precision and recall.
    
 Insights:
  * Found that Random Forest Classifier is the best-performing model, achieving  the highest accuracy, precision, and recall scores.


13. Hyperparameter Tuning & Optimization
    1. Hyperparameter Tuning applied on:
    *   Random Forest Classifier
    *   Decision Tree Classifier
    *   Gaussian Naïve Bayes
      
    * Found that Random Forest Classifier is the best-performing model, achieving  the highest accuracy after hyper parameter tuning.

 Steps Taken:Random Forest classifier Optimization 
  *Used RandomizedSearchCV for hyperparameter tuning to reduce execution time.
  *Best Parameters Found:n_estimators= 200, min_samples_split= 5, max_depth= 15.
  *Best Accuracy: 0.9716666666666667
  
 14. Save the Model
  * save the model as "The_Best_Model.joblib".
 

 15.Pipeline For ML Model
 
  * Created a scikit-learn pipeline combining:
  * SimpleImputer for missing values.
  * Onehot encoder for ecding categorical features.
  * StandardScaler for feature scaling.
  * RandomForestClassifier with optimized hyperparameters.
  * Saved the pipeline as  'Sleep_Health_Analysis_pipeline.joblib file for future predictions.


 16. Test with Unseen Data
 *  Applied the model to unseen data samples.


 17.Conclusion :

* The Random Forest Classifier achieved 97% accuracy, the highest among all six models. This demonstrates its strong ability to predict Sleep Disorders based on various features.
* When tested with unseen data, the Random Forest Classifier successfully predicted all three target classes: "Healthy," "Insomnia," and "Sleep Apnea." This indicates that the model effectively identifies patterns and distinguishes between different sleep conditions.
* Hyperparameter tuning had no significant impact on the performance of the Random Forest Classifier and Decision Tree Classifier. These models remained the top performers, each achieving over 96% accuracy.
* Gaussian Naïve Bayes showed a dramatic improvement after hyperparameter tuning, with accuracy increasing from 52% to 90%, highlighting the importance of tuning for this model.

 18.Future Work
*  Model Updates: Periodically update the model with new data to ensure it adapts to changing trends and behaviors over time.
*  Imbalanced Data Handling: Implement resampling techniques, like oversampling or undersampling, to address any class imbalances in the dataset, ensuring the model is not biased.
*  Feature Engineering: Consider adding more features or engineering existing ones to capture more nuanced patterns that could enhance the model's predictive power.
