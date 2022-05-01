# Neural_Network_Charity_Analysis

## Overview of Analysis

The purpose of this analysis is to create a binary classification model that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. In order to build the binary classifier, data provided by Alphabet Soup was preprocessed for a neural network model. Then, this preprocessed data was compiled, trained, and evaluated in the model. Lastly, 3 approaches were made to optimize the model in an attempt to achieve a target predictive accuracy higher than 75%. These 3 models were evaluated and compared to each other by their respective model's loss and accuracy to determine the most accurate model for this analysis.

### Data-source:

charity_data.csv (provided by Alphabet Soup's business team, this dataset contains more than 34,000 organizations that have received funding from Alphabet Soup over the years)

### Tools:

Python, Jupyter Notebook, Terminal (Mac)

### Libraries: 

Pandas, scikit-learn, tensorflow


## Results

### Data Preprocessing

* What variable(s) are considered the target(s) for your model?
   
   * The target for this model is the determination whether or not an application is successful. This is the chosen target for the model beause it is the      measured input of the independent variable. Specifically, the target is the "IS_SUCCESSFUL" column in the dataset.

* What variable(s) are considered to be the features for your model?

    * The features of our model, are all other columns besides "IS_SUCCESSFUL". This would be variables such as various types of "INCOME_AMT(s)",               "ORGANIZATION", various types of "APPLICATION_TYPE(s)," and "ASK_AMT".

* What variable(s) are neither targets nor features, and should be removed from the input data?

    Variables/columns in the dataset were removed during preprocessing to eliminate any redundancies and uinsignificant information. This includes columns     the following columns: "NAME," "EIN," "STATUS," and "SPECIAL CONSIDERATIONS". These variables are neither target nor features for our model.

### Compiling, Training, and Evaluating the Model

* How many neurons, layers, and activation functions did you select for your neural network model, and why?

    * For my original neural network model, I selected 12 neurons for the first hidden layer, activated by a relu function, 6 neurons for the second hidden     layer, also activated by a relu function. Then, for the output layer, I incorporated oen neuron activated by a sigmoid function.
 
* Were you able to achieve the target model performance?

    * I was not able to achieve the target model performance, presuming a standard 95% target model perforance. Upon evaluation of the model using test         data, our accuracy resulted in a value of approximately 0.725 which is below the success threshold.

* What steps did you take to try and increase model performance?

    * In a second attempt to increase model performance, I added an additional third hidden layer, with 4 neurons and also activated by a relu function.       The logic behind this was the addition of hidden layers would improve accuracy because consecutive layers of the network learn successively more           sophisticated features, which build on the features from previous layers. The accuracy calculated from this model produced a value of 0.723, which is       less than the accuracy of our first optimization model, but roughly equivalent to it.

    * In a third attempt to increase model performance, I changed the activation function of the output layer from sigmoid in the previous optimization         model to a tanh activation function. The logic behind this is that tanh is similar to a sigmoid function because it is technically sigmoidal (s -           shaped), but the advantage is that the negative inputs will be mapped strongly negative and the zero inputs will be mapped near zero in the tanh graph.     Hence, this is a reason why is tanh may function better than sigmoid. The third attempt produced an accuracy value of approximately 0.724, which is not     an improvement of the previous two models.

## Summary

Overall, the best performing model to solve the classification model is our first optimization model, which including 2 hidden layers and neurons ranging in the order of 12 -> 6 -> 1 which activation function in the following order from hidden layers to output later, relu -> relu -> sigmoid. The 2 hidden layers is beneficial for this model because often times one or two hidden layers is sufficient for the large majority of issues that arise in developing a neural network model. The amount of neurons in this model for each layer is ideal because the number od hidden neurons should be about two to three the size of the input layer, plus the size of the output layer. The simple sigmoid activation function for this model is also ideal because it is a guarantee that the output of this unit will always be between 0 and 1.

A different approach to solving this classification problem can be taken by using a random forest model. Random forest models use a number of weak learner algorithms (decision trees) and combine their output to make a final classification (or regression) decision. Because they only handle tabular data, such as this dataset, they are more efficient than deep learning models which require more code and therefore are faster. Random forest models are also more robust against overfitting. After testing the random forest model, I calculated the accuracy value to be approximately 0.725. This value is virtually the same as our first optimization model which produced the highest accuracy value of the three optimization models tested in Deliverable 3.

Nonetheless, random forest uses less code which saves resources and time and is therefore my recommendation to solving the classification model for this analysis in determinin gwhether applicants will be successful if funded by Alphabet Soup.

