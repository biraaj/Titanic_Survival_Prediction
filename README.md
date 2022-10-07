# Titanic_Survival_Prediction
This is a ML work to predict survival of passengers in titanic by obtaining dataset from Kaggle challenge.

## DATA Informations
- https://www.kaggle.com/competitions/titanic/data

## Kaggle Tutorial
- https://www.kaggle.com/code/alexisbcook/titanic-tutorial/notebook

## Steps to Run the code
- Install Anaconda 3 [Link](https://docs.anaconda.com/anaconda/install/)
- Open Jupyter Notebook and run the code in each block to see the results.

## My Contributions

Submitting the default code I obtained an accuracy of **0.775**. Then by going through [Niklas Donges's blog](https://towardsdatascience.com/predicting-the-survival-of-titanic-passengers-30870ccc7e8) on medium for predicting the survival of titanic passengers I understood the essential step to cleaning data and applying various algorithms. First I checked the columns which contained NAN values and found out the age feature had many values missing. So to normalize the age and fill out missing values I combined the training and testing data to obtain the mean and then insert it where the values were missing. Plotting the age feature on the graph showed that it was well spread out over various age brackets. So I added age to our random forest decision and found the accuracy to be **0.779** which was a very minute improvement.

Gaining a small success in the previous method I thought of looking into more features and found out that **Embarked** can be used to provide a decision. Looking at the plot of embarked it was seen most of the passengers boarded from **Southampton(S)**. I filled in two missing values in embarked by adding the most frequent port, Southhampton. Now modifying the random forest I added embarked to the feature list and obtained an accuracy of **0.78468**. This is a little better than the previous one.

Since I was getting better accuracy by adding more features to the random forest I thought of looking into the **Fare** column. Here also I found out few missing values and filled them. Hereafter plotting a histogram from the Fare feature I found out that most of the fares were between **0-100** which was not well distributed. I added this feature to the random forest feature list and the accuracy came to be **0.77751** which is similar to the first submission.

After looking into all the submissions the feature list containing **[“Pclass”, “Sex”, “SibSp”, “Parch”, “Age”, “Embarked”]** gave the best accuracy as per my submissions. This was a very minute improvement but showed a lot of ways to improve further.