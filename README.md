# Neural_Network_Charity_Analysis
## Overview of the Analysis
The purpose of this analysis was to help the foundation know where to put their investments.  Through machine learning, I identified a created a binary classifier that could predict whether applicants will be successful if they are funded by Alphabet Soup.  In order to complete this analysis, I began with a dataset in the form of a CSV, that contains over 34,000 organizations that Alphabet Soup has funded.  This dataset needed to be preprocessed in order to use it for the Neural Network Model. I cleaned the data, and used OneHotEncoder to create a categorical variable list.  After merging the encoded columns with the original columns, I created the feature and target arrays.  Then the data was scaled, and the preprocessing was done.  Once the preprocessing was done, I compiled, trained, and evaluated the model using the Keras model with the ReLu activation in hidden layers, and the Sigmoid activation in the output layer.  I performed this analysis in Google Collab.  For this model, the loss was about 56% and the accuracy rating was about 72%.  


In the third deliverable I was tasked with trying to optimize the model I had already created in order to get the accuracy score over 75%.  I used the same data, and the same model layout, but added more neurons and more layers to the models in order to try to make one perform with higher accuracy.  After 5 attempts at manipulating the model with higher node counts, and extra hidden layers, the highest accuracy reached was still about 72%.  In three of the models, I even used the Tanh activation instead of ReLu in hopes that would make the model perform better, but it did not. For the optimization deliverable, I used Jupyter Notebook.


## Results
### Data Preprocessing
* What variable(s) are considered the target(s) for your model?


  The variable that was considered the target was the 'IS_SUCCESSFUL' column.  This column was encoded to 0 for no and 1 for yes.  By using this column as the target, the question was answered as to whether or not the organization was successful with their funding from Alphabet Soup.


* What variable(s) are considered to be the features for your model?


  The feature columns were 'STATUS', 'ASK_AMT', 'APPLICATION_TYPE' which was broken down into the differents types of applications, 'INCOME_AMT' which was broken down into dollar amount ranges, 'SPECIAL_CONSIDERATIONS_N', and 'SPECIAL CONSIDERATIONS_Y'.
  
  ![Screenshot 2023-04-10 121253](https://user-images.githubusercontent.com/45715246/230943547-4882445a-d6ab-41fc-9b66-0f293cde7493.png)
  

* What variable(s) are neither targets nor features, and should be removed from the input data? 

  The variables that I removed which were not necessary were 'AFFILIATION', 'USE_CASE', 'ORGANIZATION', and 'CLASSIFICATION'.
  
  
### Compiling, Training, and Evaluating the Model


* How many neurons, layers, and activation functions did you select for your neural network model, and why?


  In the first model I used 2 hidden layers.  Hidden layer 1 had 80 neurons, and hidden layer 2 had 30 neurons.  I used these numbers because that is what was in the structure diagram in the starter code.  

![Screenshot 2023-04-11 154321](https://user-images.githubusercontent.com/45715246/231271765-f2b1fc26-2615-4a96-abb6-62fc14d977d6.png)


* Were you able to achieve the target model performance?
  
  
  In the first model I did not achieve the target model performance.  The accuracy of the first model was 72.4%.


![Screenshot 2023-04-10 123809](https://user-images.githubusercontent.com/45715246/230947913-b0b82161-120d-4e7f-8aaa-6441e78f0761.png)

* What steps did you take to try and increase model performance?


  I created 6 more models in an attempt to increase the model performance.  In the first attempt I added hidden layer 3 with 10 neurons which gave an accuracy score of 72.4% as well so there was no increase.  In the second attempt, I increased the layer 1 neurons to 100, the layer 2 neurons to 40 and kept layer 3 at 10.  This increased the accuracy score very minutely to 72.6%.  My third model had no changes in layers or neurons, instead I changed the "relu" activation to "tanh" for the 1st, 2nd, and 3rd layers.  This also produced an accuracy score of 72.6%.  The fourth attempt had an increase of neurons to layer 2 with 60 neurons, an increase of 30 neurons to layer 3, and then I added layer 4 with 10 neurons and keeping the "tanh" activation.  This accuracy score was about 72.7%.  In my fifth attempt, I increased layer 1 neurons to 200, layer 2 neurons to 120, layer 3 neurons to 60 and layer 4 to 30 neurons.  This models accuracy score was 72.5%. 
  
  
![Screenshot 2023-04-11 154718](https://user-images.githubusercontent.com/45715246/231272582-471ed1d5-5f70-45b0-8134-71660dbadfbb.png)
![Screenshot 2023-04-11 154539](https://user-images.githubusercontent.com/45715246/231272239-41e29a22-3344-4424-854c-56f459ee20f2.png)
![Screenshot 2023-04-11 154612](https://user-images.githubusercontent.com/45715246/231272369-3f08f17b-521d-4a29-ae69-78d94d2f0b86.png)


## Summary

  In summary, I could not manipulate the model to reach the target performance of 75% even after 5 attempts.  I'm not sure if I should have went much higher in amount of neurons to each layer, and added many more layers, but I think that maybe that would have helped to achieve the target performance goal.  I think that I stayed a little too small and that was my problem.  




