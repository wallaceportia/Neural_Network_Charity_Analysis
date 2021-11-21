# Neural_Network_Charity_Analysis

## Overview

In this analysis we will assist Becks, an engineer and data analysis at the well know Alphabet Soup philanthropic organization design a neural network. Over the years Alphabet Soup has donated over 10 billion dollars to that should be used for projects such as life saving technologies and reforestation projects. It however has become painfully obvious that not all organization use the donations that they recieve in an impactful way.  the president of Alphabet Soup has tasked Becks to develope a mathematical data driven solution that can do this accurately.  Bec's has decided that due to the sophistication of this problem that it would be best to design and train a deep neural network. We will work with Becks and her team to complete the design of this network that will be used as a predictor of oranizaitons that are high risk, that is they are not using the money in the way that they should.

## Results: Using bulleted lists and images to support your answers, address the following questions.

#### Data Preprocessing

###### Target Variable

![Target Variable](https://github.com/wallaceportia/Neural_Network_Charity_Analysis/blob/main/Resources/Resource_pics/Split_feature_target.PNG)

The target variable is the what we are predicting which is weather or not an application will be successful and is the y predictor is "Is Sucessful". This predictor is isolated by splitting it from the features

###### Features 
![Features](https://github.com/wallaceportia/Neural_Network_Charity_Analysis/blob/main/Resources/Resource_pics/Unique_Features.PNG)
 
 These are the unique features or x values that will be used to determine y. The features are the X values that will be used to test and train the model in order to create an alogrithm 

###### Binning

![Binning Variable](https://github.com/wallaceportia/Neural_Network_Charity_Analysis/blob/main/Resources/Resource_pics/Binning_2.PNG)

Binning is an important part of preprocessing the data as it groups all "rare" categorical variable together in an "Other" columnn this, in turn reduces the columnns to further flatten the data that will be entered into the neural network

###### Nosiey Variable What variable(s) are neither targets nor features, and should be removed from the input data?

Nosiey variables are variables that can be removed that are not adding any value to to the data set.  In this set the column "Status" was removed. 

###### Compiling

![Compile Model](https://github.com/wallaceportia/Neural_Network_Charity_Analysis/blob/main/Resources/Resource_pics/Compile_Model.PNG)

The model is complied to give it proper functionality, the efficacy of the model is measured by it's accuracy as well as it's loss. The loss function given to this model is binary_crossentropy as this model is a binary classification.  We are also measuring "accuracy", so this is also passed in the complile function, the optimizer type  is optional however "adam" is the most popular and is ofter used for binary classification models, it also helps determine the learning rate.

![Train Model](https://github.com/wallaceportia/Neural_Network_Charity_Analysis/blob/main/Resources/Resource_pics/Train_Test_Split.PNG)

The train_test_split is called on the model as we will want to train the model on some of the data, leaving a portion for testing the validity of the model 

![Fit the Model](https://github.com/wallaceportia/Neural_Network_Charity_Analysis/blob/main/Resources/Resource_pics/Fit_Model.PNG)

The model is fitted with the scaled X data and ran with a specified number of epochs.  The epochs might be eqivalent to the batch size but an observation of the epochs shows where the model stops learning,

![Evaluate Model](https://github.com/wallaceportia/Neural_Network_Charity_Analysis/blob/main/Resources/Resource_pics/Evaluate_Model.PNG)

The model is evaluated to determine the accuracy and loss on the traning data and test data. In the optimized model the accuracy and the loss of the model is loss: 0.5831 - accuracy: 0.7254.  

![Neural Network](https://github.com/wallaceportia/Neural_Network_Charity_Analysis/blob/main/Resources/Resource_pics/Hyper_Hidden_Nodes.PNG)


![Deep Neural Network](https://github.com/wallaceportia/Neural_Network_Charity_Analysis/blob/main/Resources/Resource_pics/Hyper_Leaky.PNG)

* Three layers were added to the deep neural network. Although three layers is recommended for more complexed data that is data having large dimentions, it seemed best to try 3 hidden layers as two layers did not bring about a great difference in performance
* For the first layer 36 nodes were added because it is recommended that the first layer of nodes should be half the number of features of less.  Although there are 109 features, this number of neurons did not work well for this model
* The second layer contained 8 neurons.  This number of neurons was used as to avoid over powering the model, although in the second layer as much as half the number of the first layer could be used
* In the third layer only one neuron was used.
How many neurons, layers, and activation functions did you select for your neural network model, and why?

## Summary:

The model performance of over 75% was not achieved. To improve the performance of the model, several measures were taken in terms of tweaking the hyperparameters.  the batch size was decreased to 100.  Several different activation functions were also tried, including leaky_relu and tanh.  

* Leaky_relu was tried as it helps to increase the range of the ReLU function usually, the value of a is 0.01 or so.
* The tanh activation function was used because tanh is also like logistic sigmoid but may fuction slightly better as the range of the tanh function is from (-1 to 1)
* The number of epochs was also increased, this may or may not have helped improve the accuracy of the model.  Each time an epoch is completed this represents the a full pass of the data through the neurons.  It is possible that too many of these passes my cause overfitting.  

All in all the different tweaks did not cause any type of significant improvement in the results except by a few points. I will recommend that more data be collected to improve the model as neural networks function best with larger data sets. It is possible that a Random Forest would have given better results with this data.  I would have recommended using a Random Forest Model for this data. I


