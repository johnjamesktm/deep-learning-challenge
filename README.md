# deep-learning-challenge  
Solution:  
https://colab.research.google.com/drive/1kowOkdKRFaCiK8nznqovZTjhpYSSi0yi?usp=sharing  
  
Optimized:  
https://colab.research.google.com/drive/1axC7v7Q7KSR2SGu73pRCZhYrVQPlF88d?usp=sharing  
  
## Report  
  
### Overview  
The analysis here attempts to find the best Neural Network model for the data we have. It will use Keras tuner to optimize the model by finding the appropriate number of layer, units and the activation functions for those layers.  
  
### Results  
* Data Preprocessing  
  * What variable(s) are the target(s) for your model?  
    * IS_SUCCESSFUL  
  * What variable(s) are the features for your model?
    * APPLICATION_TYPE
    * AFFILIATION
    * CLASSIFICATION
    * USE_CASE
    * ORGANIZATION
    * STATUS
    * INCOME_AMT
    * SPECIAL_CONSIDERATIONS
    * ASK_AMT
  * What variable(s) should be removed from the input data because they are neither targets nor features?
    * EIN
    * NAME
* Compiling, Training, and Evaluating the Model
  * How many neurons, layers, and activation functions did you select for your neural network model, and why?
  * Were you able to achieve the target model performance?
  * What steps did you take in your attempts to increase model performance?

### Summary
Keras tuner helps to find the optimal parameters to get the best model.
  
