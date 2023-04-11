# Neural_Network_Charity_Analysis
## Overview of the Analysis
The purpose of this analysis was to help the foundation know where to put their investments.  Through machine learning, I identified a created a binary classifier that could predict whether applicants will be successful if they are funded by Alphabet Soup.  In order to complete this analysis, I began with a dataset in the form of a CSV, that contains over 34,000 organizations that Alphabet Soup has funded.  This dataset needed to be preprocessed in order to use it for the Neural Network Model. I cleaned the data, and used OneHotEncoder to create a categorical variable list.  After merging the encoded columns with the original columns, I created the feature and target arrays.  Then the data was scaled, and the preprocessing was done.  Once the preprocessing was done, I compiled, trained, and evaluated the model using the Keras model with the ReLu activation in hidden layers, and the Sigmoid activation in the output layer.  I performed this analysis in Google Collab.  For this model, the loss was about 56% and the accuracy rating was about 72%.  


In the third deliverable I was tasked with trying to optimize the model I had already created in order to get the accuracy score over 75%.  I used the same data, and the same model layout, but added more neurons and more layers to the models in order to try to make one perform with higher accuracy.  After 6 attempts at manipulating the model with higher node counts, and extra hidden layers, the highest accuracy reached was still 72%.  In three of the models, I even used the Tanh activation instead of ReLu in hopes that would make the model perform better, but it did not. For the optimization deliverable, I used Jupyter Notebook.


## Results
### Data Preprocessing
* What variable(s) are considered the target(s) for your model?


  The variable that was considered the target was the 'IS_SUCCESSFUL' column.  This column was encoded to 0 for no and 1 for yes.  By using this column as the target, the question was answered as to whether or not the organization was successful with their funding from Alphabet Soup.


* What variable(s) are considered to be the features for your model?


  The feature columns were 'STATUS', 'ASK_AMT', 'APPLICATION_TYPE' which was broken down into the differents types of applications, 'INCOME_AMT' which was broken down into dollar amount ranges, 'SPECIAL_CONSIDERATIONS_N', and 'SPECIAL CONSIDERATIONS_Y'.
  
  ![Screenshot 2023-04-10 121253](https://user-images.githubusercontent.com/45715246/230943547-4882445a-d6ab-41fc-9b66-0f293cde7493.png)
  

* What variable(s) are neither targets nor features, and should be removed from the input data? 

  AFFILIATION USE_CASE   ORGANIZATION CLASSIFICATION
  
  
### Compiling, Training, and Evaluating the Model


* How many neurons, layers, and activation functions did you select for your neural network model, and why?

![Screenshot 2023-04-11 154321](https://user-images.githubusercontent.com/45715246/231271765-f2b1fc26-2615-4a96-abb6-62fc14d977d6.png)


* Were you able to achieve the target model performance?



![Screenshot 2023-04-10 123809](https://user-images.githubusercontent.com/45715246/230947913-b0b82161-120d-4e7f-8aaa-6441e78f0761.png)

* What steps did you take to try and increase model performance?

![Screenshot 2023-04-11 154503](https://user-images.githubusercontent.com/45715246/231272118-d52e768f-c813-4a5d-a204-0f6d095d6ac5.png)
![Screenshot 2023-04-11 154539](https://user-images.githubusercontent.com/45715246/231272239-41e29a22-3344-4424-854c-56f459ee20f2.png)
![Screenshot 2023-04-11 154612](https://user-images.githubusercontent.com/45715246/231272369-3f08f17b-521d-4a29-ae69-78d94d2f0b86.png)



## Summary





