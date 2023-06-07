# deep-learning-challenge  
Solution:  
https://colab.research.google.com/drive/1axC7v7Q7KSR2SGu73pRCZhYrVQPlF88d?usp=sharing  
  
Optimized:  
https://colab.research.google.com/drive/1kowOkdKRFaCiK8nznqovZTjhpYSSi0yi?usp=sharing  
  
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
    * I ran Keras tuning.
  * Were you able to achieve the target model performance?
    * Close. Not exactly.
  * What steps did you take in your attempts to increase model performance?
    * Removed rows with SPECIAL_CONSIDERATIONS = 'Y' and STATUS = 0 and then removed the two columns.
    * I combined the following classes in INCOME_AMT
      * 0 and 1-9999 combined to 0-9999
      * 10000-24999 and 25000-99999 combined to 10000-99999
      * 5M-10M and 10M-50M combined to 5M-50M
    * Used cut-off of 1000 for APPLICATION_TYPE column to make class "Other"
    * Used cut-off of 800 for CLASSIFICATION column to make class "Other"
    * After the above changes the value_counts() became:
      * APPLICATION_TYPE       6
      * AFFILIATION            6
      * CLASSIFICATION         6
      * USE_CASE               5
      * ORGANIZATION           4
      * INCOME_AMT             6
      * ASK_AMT             8741
      * IS_SUCCESSFUL          2
    * Scaled only the "ASK_AMT" column
    * Applied random over sampling
    


### Summary
Keras tuner helped to find the optimal parameters to get the best model.
  
