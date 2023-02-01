# Tarun Badarvada Portfolio



## Personal & Academic Projects

-------------------------------------------------------------------------------------------------------------------------------
### Is Cinema Back to Normal?

#### Goal and significance related to data science/data analytics

After taking a look at past box office data, we want to know what we can expect next for cinema and how we can see the box office recover even further. Using the data we’ve collected, we can predict and give our best estimate for how the year 2023 in movies will likely perform. We can take data on the budgets of upcoming movies and look at previously released films that have been released in similar conditions (such as studio, time, director, lead actors, and level of hype from social media through views and likes) and make our predictions of how we can see cinema in 2023 play out. 

#### What is the problem you are trying to solve? How do you plan to solve it?

Through research and data analysis, we hope to determine whether the movie industry will be able to recover to pre-COVID levels. We will also analyze data to predict gross sales based on specific movie genres. Our group will look at box office sales from before and after COVID and see if there are any methods to predict future ticket sales. 
For analyzing the pre-covid box office data, we can take the average weekend ticket sales from 2015 to 2019 and use that as a benchmark for pre-pandemic data. Then for the post-covid data, we can take all the weekend box office opening across 2020, 2021, and 2022 to compare against the pre-pandemic data. We’ll be getting most of our data from BoxOfficeMojo.com to get all our box office numbers

-------------------------------------------------------------------------------------------------------------------------------

## Sources:

Box Office Mojo: https://www.boxofficemojo.com/

Box Office Mojo Weekends 2022: https://www.boxofficemojo.com/weekend/?ref_=bo_nb_di_secondarytab

-------------------------------------------------------------------------------------------------------------------------------
![image](https://user-images.githubusercontent.com/31902746/216191573-9b92a81a-8772-4ae8-bb25-5bad92e427dc.png)

![image](https://user-images.githubusercontent.com/31902746/216191621-88041ec5-a63a-4e67-aecd-1d1898d1fd1b.png)

![image](https://user-images.githubusercontent.com/31902746/216191808-cb7e02af-13aa-4a1c-bcc7-20c5895ee0ed.png)

![image](https://user-images.githubusercontent.com/31902746/216191846-60363616-9dbd-4b3c-ab3d-95b5ceccfa49.png)

![image](https://user-images.githubusercontent.com/31902746/216191899-795bb0d5-ec63-4829-9781-8ab127c28a94.png)

![image](https://user-images.githubusercontent.com/31902746/216191459-be76cc30-d295-4a00-b541-b89cf3d51944.png)

![image](https://user-images.githubusercontent.com/31902746/216191959-c4ff084d-1dd4-4e80-873e-da03d42882db.png)




## Presentation Slides

https://docs.google.com/presentation/d/1OtkcrwYwRG1nxtYuFE_pcdTRRjoSJSG7tPYnMHGGO4Q/edit?usp=sharing


-------------------------------------------------------------------------------------------------------------------------------

### Can You Predict a Heart Attack Before it Happens?

#### Introduction
"Heart disease is the leading cause of death for men, women, and people of most racial and ethnic groups in the United States,” according to the CDC. Heart disease take countless lives each year and costs the U.S. billions of dollars in health care and lost productivity. In the U.S., the most common type of heart disease leads to heart attack, making it an important target for prevention as a dangerous outcome of heart disease. Key to prevention and treatment of heart disease is the ability to predict its onset, which can be represented by heart attack risk. Given the urgent need for heart disease prevention and the wide clinical applications of prediction models since the rise of precision medicine, we aimed to build a model that could accurately predict an individual’s risk of heart attack, identify other target areas for preventative care, and generally help spread awareness of the importance of heart disease prevention.

#### Methodology
The dataset used is from Kaggle.com and contains data of 303 patients that may be relevant to heart attack risk, including their true heart attack risk. The dataset offers measures such as age, sex, chest pain type (an indicator of blood supply to the heart), resting electrocardiographic results, resting blood pressure, and cholesterol, max heart rate achieved, which contribute to the final target attributes indicating whether the patient's chances of getting a heart attack. The data contains 303 rows and 14 columns, representing 303 patients and 14 variables. To prepare our dataset, we imported our dataset from a .csv file as a Pandas DataFrame. We found the columns “caa”, “cp”, and “restecg” represented categorical variables but were given as "INT64" values. Thus, we used pd.get_dummies() to convert the label vectors into one-hot vectors. For our analysis, we explored three different algorithms to predict whether an individual is at more (1) or less (0) risk of having a heart attack. For training our model, we will split dataset using sklearn’s train_test_split library and used 70% of the data as our training set and 30% for our testing set. Once our data was split, we trained each algorithm: K Nearest Neighbor, Logistic Regression, Random Forest Classification. We then compiled prediction accuracy scores, confusion matrices, and classification reports for each model.

#### Results & Evaluations

##### KNN Classifier

![image](https://user-images.githubusercontent.com/31902746/216193117-f98b89cc-4342-43ea-857a-2f163054b8c8.png)

![download](https://user-images.githubusercontent.com/31902746/216193138-4c4897f8-94ef-49a1-8ba7-cc4952afcf71.png)

![image](https://user-images.githubusercontent.com/31902746/216193411-6edc3330-a425-43eb-8571-72b22573ea2e.png)

This model is neither precise nor accurate with a likelihood of many false negatives and false positives.​

K-Nearest Neighbor Results
Our classification reports suggests our K-Nearest Neighbors model is neither precise nor accurate. The model's ability to predict a high risk and low risk patient is roughly the same, with a range of 55 - .57, while the range of precision, is much greater for the two classification sets. For the heatmap above, total training set size = 91 patients. the results are explained as follows:

Upper left quadrant #1: represents patients who were at low risk for a heart attack, and our model predicted they were low risk. Of the 52 low risk patients, the model only accurately predicted 27 of them.

Upper right quadrant #2: represents patients who were at low risk for a heart attack, but our model predicted they were at a high risk of a heart attack. Of the 52 low risk patients, the model incorrectly predicted 25 of them.

Lower left quadrant #3: represents patients who were at a high risk of heart attack, but our model incorrectly predicted they were low risk. Of the 39 low risk patients, the model incorrectly predicted 15 of them.

Lower right quadrant #4: represents patients who were at a high risk of a heart attack, and our model accurately predicted they were at a high risk of a heart attack. Of the 39 low risk patients, the model correctly predicted 24 of them.

##### Random Forest Classifier

![image](https://user-images.githubusercontent.com/31902746/216193516-086061e9-b3b4-4c4e-a91c-cf62ee6e8353.png)

![download (1)](https://user-images.githubusercontent.com/31902746/216193552-1e8d7ec0-de62-4045-bb1d-ffd514ce5d36.png)

![image](https://user-images.githubusercontent.com/31902746/216193865-75a60edf-5a85-47ed-bc31-6a4e49ff7dc2.png)


Random Forest Classifier Results:
The Random forest classifier is a noticeable improvement over the K-Nearest Neighbour method. Our classification reports demonstrate that we're slightly more precise with our low risk classification, a trend which continues to propagate since our KNN report. We also notice that our accuracy is roughly similar, with a range of .87 - .90. In context, for every 9 out of 10 patients we are presented with, our random forest classifier will give the correct classification. Total patient test size equals 91 patients. We decided to visualize this information, in the heatmap above:

Upper left quadrant #1: represents patients who were at low risk for a heart attack, and our model predicted they were low risk. Of the 52 low risk patients, the model correctly predicted 45 of them.

Upper right quadrant #2: represents patients who were at low risk for a heart attack, but our model predicted they were at a high risk of a heart attack. Of the 52 low risk patients, the model incorrectly predicted 7 of them.

Lower left quadrant #3: represents patients who were at a high risk of heart attack, but our model incorrectly predicted they were low risk. Of the 39 low risk patients, the model incorrectly predicted 4 of them.

Lower right quadrant #4: represents patients who were at a high risk of a heart attack, and our model accurately predicted they were at a high risk of a heart attack. Of the 52 low risk patients, the model correctly predicted 35 of them.

** Note that we have a low number of patients in quadrants 2 and 3, which tell us our model is fairly accurate.

##### Logisitic Regression

![image](https://user-images.githubusercontent.com/31902746/216194015-2d9246e0-82bc-4b7b-b26e-ab38fa95e0a0.png)

![download (2)](https://user-images.githubusercontent.com/31902746/216194025-ecb1c0f5-6dcb-4b7e-a0a2-39000305cb09.png)

![image](https://user-images.githubusercontent.com/31902746/216194104-db90d4c4-2c55-485e-b17d-30de2653a570.png)

Logistic Regression Results:
Directing attention to the quantative results, produced by the classifcation report, Logistic Regression fall's between K-Nearest Neighbor (KNN) and Random Forest Classifer (RFC), which it is nearly idential. Although, LR clusters near RFC. The model's precision is also similar to RFC, although it falls short when prompted to classify patients who are at low risk of a heart attack. We have a noticable increase in incorrect classification here, indicating that if patients were to rely on this model, they would have a false positive, and potentially act on an incorrect diagnosis.

Upper left quadrant #1: represents patients who were at low risk for a heart attack, and our model predicted they were low risk. Of the 52 low risk patients, the model correctly predicted 39 of them.

Upper right quadrant #2: represents patients who were at low risk for a heart attack, but our model predicted they were at a high risk of a heart attack. Of the 52 low risk patients, the model incorrectly predicted 13 of them.

Lower left quadrant #3: represents patients who were at a high risk of heart attack, but our model incorrectly predicted they were low risk. Of the 39 low risk patients, the model incorrectly predicted 3 of them.

Lower right quadrant #4: represents patients who were at a high risk of a heart attack, and our model accurately predicted they were at a high risk of a heart attack. Of the 52 low risk patients, the model correctly predicted 36 of them.

--------------------------------------------------------------------------------------------------------------------------------------------------------------

### Q for Question Overview

Click here for the Video 

#### [![Q for Question Overview Video Link Here!](https://img.youtube.com/vi/ISZbOyt18_k/default.jpg)](https://www.youtube.com/watch?v=ISZbOyt18_k&ab_channel=TarunBadarvada)

#### What is Q for Question?

Question.io is a tool that aims to facilitate communication between students and teachers in the classroom. It provides a platform for students to ask questions during class and for teachers to answer them. The tool allows teachers to start a session at the beginning of each class and moderate the questions asked by students. Students can login to the session and ask their questions anonymously or not. The goal of this tool is to create a more open and engaging learning environment in the classroom.

#### Link to AppSmith Application
https://appsmith.cs3200.net/app/test-app/home-page-6387d010ffea3148102ab333

By Tarun Badarvada

