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

##### Random Forest Classifier

![image](https://user-images.githubusercontent.com/31902746/216193516-086061e9-b3b4-4c4e-a91c-cf62ee6e8353.png)

![download (1)](https://user-images.githubusercontent.com/31902746/216193552-1e8d7ec0-de62-4045-bb1d-ffd514ce5d36.png)


