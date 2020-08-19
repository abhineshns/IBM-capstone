# Final Report
## Introduction/Business problem 

### Each day thousands of road accidents are happening in today’s world. Road accidents will consist a good percentage among all accidents in a given country. Many loses lives and so many getting injured everyday in road accidents. The road accident can happen because of many reasons. Many factors can influence the cause of road accidents like the condition of the road, condition of light and so on. Similarly depending on various factors severity of the road accidents can vary. With proper data of the past accidents we can model a good performing machine learning model that predict the severity of the accidents. Identifying the various factors that influence the severity of the road accidents and making this as our independent attributes of our model and the corresponding severity score will become the target variable.
### This model can be used to calculate the severity of future accidents and we can modify several factors in the road to reduce the severity of future possible accidents. So the effective use of the model eventually can save lives of several persons.

## Data
### For this project I have chosen a dataset that consist all the details of past accidents happened in a certain place. In the data the target variable is the severity of the accidents and we have 37 independent variables. We cannot select all these variables for model creation. So data cleaning is very essential here. First we have to select the required independent attributes for the model creation. So I choose certain variables that logically can influence the road accident severity. Those variables are:
 ### 'ADDRTYPE'- Collision address type 
### 'COLLISIONTYPE'- Collision type
### 'PERSONCOUNT'-Persons involved in the accident 
### 'VEHCOUNT'-Vehicle involved in the accident 
### 'JUNCTIONTYPE'- Junction type
### 'WEATHER'-Weather condition 
### 'ROADCOND'-Road condition
### 'LIGHTCOND'-Light condition 
### 'PEDCOUNT'-Pedestrian count
### The data set had some null values. To balance the dataset I removed all the records having a null value in it. Even after deleting this rows we had more than 185000 records which was enough to train a good model.
## Encoding 
### Many of the attributes was categorical in our dataset so encoding this values to numerical form is a must. Since all the categorical attributes are nominal, only nominal encoding techniques are possible here. So here I used One hot encoding and mean encoding for encoding the data.
### Over use of one hot encoding  may lead to multicollinearity or high cardinality. So I only applied one hot encoding on PEDCOUNT and JUNCTIONTYPE variables which is having lesser number of categories. For other nominal variables I applied mean encoding. 
# Model creation 

## Logistic regression
### Logistic regression is a supervised learning classification algorithm used to predict the probability of a target variable. The nature of target or dependent variable is dichotomous, which means there would be only two possible classes.
### In simple words, the dependent variable is binary in nature having data coded as either 1 (stands for success/yes) or 0 (stands for failure/no).
### Mathematically, a logistic regression model predicts P(Y=1) as a function of X. It is one of the simplest ML algorithms that can be used for various classification problems such as spam detection, Diabetes prediction, cancer detection etc.
### First we have to split the dataset into X(independent variables) and y(dependent variables). Before applying the logistic regression we have to normalize the dataset. 
### After normalising the data, we can do model creation. Now created the model and now we have to do model evaluation

## Model evaluation

### Now we have to test the efficiency of the model. Here I used Jaccard index, precision, recall and f1-score for the model evaluation.
### The Jaccard index showed a score of 0.744 and values of precision, recall and f1-score is showing good results.

## Support Vector Machine
### “Support Vector Machine” (SVM) is a supervised Machine learning algorithm which can be used for both classification or regression challenges. However, it is mostly used in classification problems. In the SVM algorithm, we plot each data item as a point in n-dimensional space (where n is number of features you have) with the value of each feature being the value of a particular coordinate. Then, we perform classification by finding the hyper-plane that differentiates the two classes very well.
### Support vector machine also showed a similar accuracy scores as logistic regression

## Conclusion

### We have created 2 models that predict severity of accident from the given independent variables. The algorithms showed an accuracy of 74%. So using this algorithms we can predict the severity of the future accidents. So we can change certain factors so that it eventually reduce the severity of the accident.     

### For the detailed report please check this blog link http://datageeks.unaux.com/2020/08/19/predicting-the-severity-of-road-accidents/
