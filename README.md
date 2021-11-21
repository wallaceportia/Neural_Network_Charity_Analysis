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

The model is complied to give it proper functionality, the efficacy of the model is measured by it's accuracy as well as it's loss. The loss function given to this model is binary_crossentropy as this model is a binary classification.  We are also measuring "accuracy", so this is also passed in the complile function, the optimizer type  is optional however "adam" is the most popular and is ofter used for binary classification models

![Train Model](https://github.com/wallaceportia/Neural_Network_Charity_Analysis/blob/main/Resources/Resource_pics/Train_Test_Split.PNG)

The train_test_split is called on the model as we will want to train the model on some of the data, leaving a portion for testing the efficacy of the model 

![Fit the Model]()

![Evaluate Model](https://github.com/wallaceportia/Neural_Network_Charity_Analysis/blob/main/Resources/Resource_pics/Evaluate_Model.PNG)

The model is evaluated to determine the accuracy and loss on the traning data and test data

How many neurons, layers, and activation functions did you select for your neural network model, and why?
Were you able to achieve the target model performance?
What steps did you take to try and increase model performance?
Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.
Summary:

There is a summary of the results (2 pt)
There is a recommendation on using a different model to solve the classification problem, and justification (3 pt)
