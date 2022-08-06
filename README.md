# Neural_Network_Charity_Analysis

## Overview:

 The purpose of this analysis is to use deep learning with a neural network model in order to analyze organizations that have been funded by Alphabet Soup.  The neural network was trained and optimized to predict the likelihood that new applicants would be successful if funded by Alphabet Soup.

## Results:

### Data Preprocessing

 - The target variable for this analysis is "IS_SUCCESSFUL".

 - The feature variables for this analysis are "APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION", "STATUS", "INCOME_AMT", "SPECIAL_CONSIDERATIONS", and "ASK_AMT".

 - The variables that are erroneous and need to be removed are "EIN" and "NAME".

### Compiling, Training, and Evaluating the Model

 - Hidden Layers: 2

 - The first hidden layer has 60 nodes, which were chosen because it is about 1.5 times the number of input features (43).  This uses a "relu" activation function due to its reliability and quick processing time.

 - The second hidden layer has 30 nodes, which is half of the first layer.  This layer also uses a "relu" activation function for the same reasons listed above.

 - The output layer has 1 node and uses a "sigmoid" activation function.  The single node was chosen because the output should only have two options, "TRUE" and "False".  The sigmoid function was chosen because if provides an output probability between 0 and 1, which will show the likelihood of TRUE vs FALSE.

 - The code for the model is shown below:

![This is an image](https://github.com/JDBrowder523/Neural_Network_Charity_Analysis/blob/main/Challenge/Images/code_total_params.png)

 - The model was not able to achieve the target output performance, as the accuracy was only 67%, which is below the target of 75%.  

 - The output is shown below:

![This is an image](https://github.com/JDBrowder523/Neural_Network_Charity_Analysis/blob/main/Challenge/Images/output_challenge_code.png)

#### IMPROVING THE MODEL

 - Attempt 1: First, I dropped the SPECIAL_CONSIDERATIONS column.  This produced an accuracy level of 69%, which showed improvement over the original model.

![This is an image](https://github.com/JDBrowder523/Neural_Network_Charity_Analysis/blob/main/Challenge/Images/output_drop_special_considerations.png)

 - Attempt 2: Second, I added a third hidden layer with 10 nodes and a "relu" activation function. This lowered the accuracy to 63%.  This was most likely due to overfitting of the model.

![This is an image](https://github.com/JDBrowder523/Neural_Network_Charity_Analysis/blob/main/Challenge/Images/code_2nd_hidden_layer.png)
![This is an image](https://github.com/JDBrowder523/Neural_Network_Charity_Analysis/blob/main/Challenge/Images/output_2nd_hidden_layer.png)

 - Attempt 3: Third, I changed the activation function of the first hidden layer to "tanh".  This lowered the accuracy to 54%.

![This is an image](https://github.com/JDBrowder523/Neural_Network_Charity_Analysis/blob/main/Challenge/Images/code_tanh_1st_hidden_layer.png)
![This is an image](https://github.com/JDBrowder523/Neural_Network_Charity_Analysis/blob/main/Challenge/Images/output_tanh_1st_hidden_layer.png)

## Summary:

 Overall, the neural networking model did not produce the desired accuracy of 75% and the attempts at optimizing the model caused the accuracy to decrease.  This is possibly due to overfitting of the model. 

 An alternative machine learning model that could be fitted to this data is Random Forest Classifier.   This type of machine learning would be applicable because the classification system we are using is binary in that the results for "IS_SUCCESSFUL" are either "TRUE" or "FALSE".
