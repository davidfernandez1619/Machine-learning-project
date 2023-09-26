# Machine learning  project: 

In this project, we had to create a machine learning model to predict the price of a [given set of diamonds](https://www.kaggle.com/competitions/diamonds-part-may-23/data?select=test.csv), using another data set as [training data](https://www.kaggle.com/competitions/diamonds-part-may-23/data?select=train.csv). 

Our job, before adjusting the model, was to preprocess the training data to take care of the null values, outliers, and encode our categoric values. Depending on the way you manage these values, you can get different prediction models. On this particular dataset, there weren't any null values, but we had some outliers and categoric values. 

After doing an EDA of our data, I mainly did four preprocessing combinations: 

## First combination: 

In my first preprocessing, I decided to leave the outliers, and do an ordinal encoding, using the same order as I observed in the visualization of our categoric values. You can see the whole EDA process and first preprocessing [here](https://github.com/davidfernandez1619/Machine-learning-project/blob/main/Notebooks/Training%20preprocessings/EDA%20and%20first%20combination.ipynb). 

After adjusting our model using decision tree, we got these metrics: 

<img width="402" alt="First combination" src="https://github.com/davidfernandez1619/Machine-learning-project/assets/38441372/c18f3dcc-1ddc-424d-9e30-83ee80ff7017">

As we can see, our R2 is pretty high, which means that approximately the 97% of the variation of our response variable (price) is explained by all the predictor variables (R2 ranges between 0 and 1). 

## Second combination: 

Here, I decided to get rid of my 'y' and 'z' columns and again, do an ordinal encoding. I got these metrics: 

<img width="405" alt="Second combination" src="https://github.com/davidfernandez1619/Machine-learning-project/assets/38441372/48007b76-5f96-47e9-ae1b-2dd6b943f8a2">

The R2 is slightly higher this time. 

## Third combination: 

In this third combination, I replaced the outliers by the mean, I changed the encoding method, using a get-dummies this time. These were the metrics I got: 

<img width="409" alt="Third combination" src="https://github.com/davidfernandez1619/Machine-learning-project/assets/38441372/94c36bd2-ce7f-456b-8150-d1a30616756e">

We can see how R2 decreases in this case. 

## Fourth combination: 

In my fourth and last combination, I decided to again replace the outliers by the mean, and I again did a get-dummies encoding, but this time I got rid of columns 'y' and 'z', obtaining the following outcome: 

<img width="409" alt="Fourth combination" src="https://github.com/davidfernandez1619/Machine-learning-project/assets/38441372/6117a68a-8051-49d8-8df7-eba7afa7b66d">

Our R2 is the lowest in this case. 

# Conclusion: 

Our metrics suggest that our first combination created the best model, since all the errors are low, and our R2 is the highest. 

Feel free to check the notebooks in order to see the processes I followed. 

Thank you!







