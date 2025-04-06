# SLEEP-HEALTH-AND-LIFESTYLE-ANALYSIS
DSML Entri Capstone Project
Overview of Problem Statement:
  According to the National Institutes of Health (NIH), quality sleep is as important to good health as diet and exercise. Regularly missing adequate quality sleep can raise the risk of a range of health issues, such as heart disease, stroke, obesity and dementia. The NIH recommends seven to nine hours of sleep a night for the average person. 
  Sleep health refers to the quality, duration, timing, and regularity of sleep, as well as the behaviors and habits that promote optimal sleep. It encompasses both the physiological aspects of sleep and the psychological and environmental factors that influence sleep patterns. It is essential for one's overall well-being and is associated with numerous physical, cognitive, and emotional benefits.
  When sleep health is prioritized, it can lead to improved mood, cognitive function, immune function, cardiovascular health, and overall quality of life. Conversely, chronic sleep deprivation or poor sleep quality can contribute to a range of negative outcomes, including increased risk of obesity, diabetes, cardiovascular disease, depression, and impaired cognitive performance. Therefore, adopting habits and behaviors that support good sleep health is crucial for optimal functioning and well-being.

  
 # **Objective:**

⌛ How is Fitness tied to Sleep Health

Fitness plays a significant role in sleep health, as regular physical activity has been shown to positively influence both the quality and duration of sleep. Regular exercise has been associated with shorter sleep onset latency, meaning it may help individuals fall asleep more quickly after going to bed (including those with sleeping disorders. Beyond its direct effects on sleep, regular exercise is associated with numerous health benefits, including reduced risk of stress, obesity, cardiovascular disease, and depression, all of which can impact sleep health.

Data Description:
Source: The dataset can be downloaded from the link :(https://www.kaggle.com/code/giulianoverdone/up-to-date-sleep-health-and-lifestyle-analysis?select=Sleep_Data_Sampled.csv
Recognizing Variables in the Dataset

Person ID: An identifier for each individual.
Sex: The sex of the person (Male/Female).
Age: The age of the person in years.
Occupation: The occupation or profession of the person
Sleep Duration (hours): The number of hours the person sleeps per day.
Quality of Sleep (scale: 1-10): A subjective rating of the quality of sleep, ranging from 1 to 10.
Physical Activity Level (minutes/day): The number of minutes the person engages in physical activity daily.
Stress Level (scale: 1-10): A subjective rating of the stress level experienced by the person, ranging from 1 to 10.
BMI Category: The BMI category of the person (e.g., Underweight, Normal, Overweight).
Blood Pressure (systolic/diastolic): The blood pressure measurement of the person, indicated as systolic pressure over diastolic pressure.
Heart Rate (bpm): The resting heart rate of the person in beats per minute.
Daily Steps: The number of steps the person takes per day.
Sleep Disorder: The presence or absence of a sleep disorder in the person (Healthy, Insomnia, Sleep Apnea)

Sleep Disorder
Healthy: The individual does not exhibit any specific sleep disorder.
Insomnia: The individual experiences difficulty falling asleep or staying asleep, leading to inadequate or poor-quality sleep.
Sleep Apnea: The individual suffers from pauses in breathing during sleep, resulting in disrupted sleep patterns and potential health risks.

CONCLUSION :
The Random Forest Classifier achieved 97% accuracy, the highest among all six models. This demonstrates its strong ability to predict Sleep Disorders based on various features.
When tested with unseen data, the Random Forest Classifier successfully predicted all three target classes: "Healthy," "Insomnia," and "Sleep Apnea." This indicates that the model effectively identifies patterns and distinguishes between different sleep conditions.

The dataset was well-balanced, with no missing values or duplicates. Various preprocessing techniques such as encoding, feature selection, and scaling contributed to all models achieving over 90% accuracy, except for the Gaussian Naïve Bayes model.

Hyperparameter tuning had no significant impact on the performance of the Random Forest Classifier and Decision Tree Classifier. These models remained the top performers, each achieving over 96% accuracy.

Gaussian Naïve Bayes showed a dramatic improvement after hyperparameter tuning, with accuracy increasing from 52% to 90%, highlighting the importance of tuning for this model.
