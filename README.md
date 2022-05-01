# Neural_Network_Charity_Analysis

## Overview of Analysis

The purpose of this analysis is to create a binary classification model that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. In order to build the binary classifier, data provided by Alphabet Soup was preprocessed for a neural network model. Then, this preprocessed data was compiled, trained, and evaluated in the model. Lastly, 3 approaches were made to optimize the model in an attempt to achieve a target predictive accuracy higher than 75%. These 3 models were evaluated and compared to each other by theur respective model's loss an accuracy to determine the most accurate model for this analysis.

### Data-source:

charity_data.csv (provided by Alphabet Soup's business team, this dataset contains more than 34,000 organizations that have received funding from Alphabet Soup over the years)

### Tools:

Python, Jupyter Notebook, Terminal (Mac)

### Libraries: 

Pandas, scikit-learn, tensorflow


## Results

Data Preprocessing

* What variable(s) are considered the target(s) for your model?

The target for this model is whether or not the applicationis is successful. It is the target beause it is the neasyred input of the independent variable. In this case, it is the "IS_SUCCESSFUL" column in the dataset.

* What variable(s) are considered to be the features for your model?

The features of our model, are all other columns besides "IS_SUCCESSFUL". This would be variables such as "INCOME_AMT" or "ORGANIZATION".

* What variable(s) are neither targets nor features, and should be removed from the input data?

Variables/columns in the dataset were removed during preprocessing to remove redundancies and unimportant information. This includes columns such as "NAME," "EIN,", and "SPECIAL CONSIDERATIONS".

Compiling, Training, and Evaluating the Model

* How many neurons, layers, and activation functions did you select for your neural network model, and why?

For my original neural network model, I selected -__
 
* Were you able to achieve the target model performance?

I was not able to achieve the target model performance, assuming that is 95%. 

* What steps did you take to try and increase model performance?

As an attempt to increase model performance, 


## Summary

Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.
