# WideBot_Task3
## Problem Statement
Task 3 - Classification Using the same data in task 2, build a machine learning based classifier and show its performance on the test-set. Show precision, recall, f-score, accuracy for each class and for the whole test data. Please describe briefly the meaning of each result and metric for this specific task. Also, please write some enhancements that you may think about to achieve better results. Note: add a readme file that describes the whole training process in briefed points. Note: Use stories data only (not comments). Also, take the last 20% of each file as a test-set.

## Note: The dataset was too large to be uploaded on github. In order to run the notebook without errors, make sure to download the dataset:  https://www.kaggle.com/datasets/tariqmassaoudi/hespress and add it to the code directory. 

## Training
* For preprocessing: stopwords and punctuations were removed.
* The text was transformed using TF-IDF
* A logistic regression model was trained

## Scores
The model's performance on the stories test dataset is shown in the figure below: 

![storiestestscores](https://github.com/Aisha-Hagar/WideBot_Task3/assets/61799091/07872898-8fa7-404e-a5f5-57bc649aa018)

* Some classes have precision higher than recall such as Tamazight which indicates that most misclassifications were directed to one class
* Some classes have recall higher than precision such as art-et-culture which indicates that most misclassifications were distributed across multiple classes

Since the data is balanced, we can evaluate the performance of the model through the accuracy metric.

The confusion matrix shows with more details where the misclassifications occurred:

![confmat](https://github.com/Aisha-Hagar/WideBot_Task3/assets/61799091/06270f06-43fa-4273-84d1-4432ae58a6c4)

* Most Tamazight misclassification were classified as art-et-culture
* Most Societe misclassification were classified as regions
* Most regions misclassification were classified as Societe
* Most politique misclassification were classified as orbites
* Most orbites misclassification were classified as politique or marocains-du-monde
* Most orbites misclassification were classified as politique

## Enhancements
* More analysis to understand the similarities between the topics 
* Test different models
