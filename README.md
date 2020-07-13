# Predicting outcome of COVID-19 case

<img src="https://github.com/janinaschuhmacher/covid-19-data-analysis/blob/master/visualization/outcomes.png" alt="outcomes of COVID-19 cases">

<img src="https://github.com/janinaschuhmacher/covid-19-data-analysis/blob/master/visualization/outcome_per_age.png" alt="outcomes of COVID-19 cases">


The goal of this project is to train a model which predicts whether a patient will die or recover from Coronavirus. 
To train the model, a dataset of COVID-19 cases is used. As can be seen in the plots above, about eight percent of COVID-19 patients in this dataset died. However, the ratio increases significantally in older age groups. 

## How?
<img src="https://github.com/janinaschuhmacher/covid-19-data-analysis/blob/master/visualization/final_confustion_matrix.png" alt="confusion matrix of the final logistic regression model">
<img src=https://github.com/janinaschuhmacher/covid-19-data-analysis/blob/master/visualization/feature_importance.png alt="feature importance! >
Performance of different classifiers (k-nearest neighbours, logistic regression and randomforest classifier) were compared. 
Overall, the highly unbalanced nature of the dataset made it difficult to reach a good trade-off between precision and recall (as is visualized in the confusion matrix). Age emerged as the most predictive feature for the outcome of a COVID-19 disease. 
Other features in the dataset did not create a lot of additional value. 

## The data 

The dataset confirmed-positive-on data comes from https://howsmyflattening.ca/#/data/. 
It includes compiled daily reported data from public health units on confirmed positive cases of COVID-19 in Ontario. It includes data on patients from 1st January 2020 to 28th June 2020 and is updated daily. Currently, the dataset entails data from 37,947 patients. Case data is as initially reported.

The following are the features which we used for predicting the outcome variable (recovered or diseased).

* date of diagnosis
* age group - categorized to <20, 30s, 40s, 50s, 60s, 70s, 80s or 90s
* gender
* outbreak related - Yes or no entry
* Latitude and longitude of the reporting public health unit

