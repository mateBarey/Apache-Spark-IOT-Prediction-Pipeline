# Apache-Spark-IOT-Prediction-Pipeline

In this Notebook IOT weather data is collected from a csv and then made into a df using apache spark. 

Once its cleaned up from null values and trailing characters and 0's we use the Vector assembler and a filter to extract

the features we will be using to build our model and predict our labels. A correlation matrix is built to ensure independent

features for building a model. We then separate our data into a training and test set. In this exercise we want to predict a 

label that is "HOURLYPressureTendency".  The vecor Assembler is used again to build our features and a normalizer is also used 

to normalize the columns.We buld our Linear Regression instance with our label column and its parameters and then build our 

pipeline with the LR parameters, normalizer and extracted features. The model is then ready to be trained and is built using

our train_df. Once the model is built its predictive ability is now tested against the test data in df_test. The regression 

metrics are then outputted with our rmse as a measure for our accuracy. The same is done for various other refressors and 

classifiers as can be seen the best accuracy found for this model was using linear regression.

