# Neural_Network_Charity_Analysis
## Overview Of The Analysis
The purpose of this analysis was to design a neural network using TensorFlow to create a binary classification model that could predict if Alphabet Soup-funded organization will be successful based on the features in the dataset.
## Resources
* Data Source: charity_data.csv
* Software: Python 3.9.12, Jupyter Notebook 6.4.8, VSCode 1.72.0
## Results
What variable(s) are considered the target(s) for your model?

The column IS_SUCCESSFUL contains binary data referring to whether or not the charity donation was used effectively. This variable is then considered the target.

What variable(s) are considered to be the features for your model?

The following columns APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT are the features.

What variable(s) are neither targets nor features, and should be removed from the input data?

EIN and NAME are identifcations columns and will be removed.

How many neurons, layers, and activation functions did you select for your neural network model, and why?

The model is made up of two hidden layers with 80 and 30 neurons. The input data has 43 features and 25,724 samples. The output layer is made of a unique neuron as it is a binary classification. To speed up the training process we used the activation function ReLU for the hidden layers. Sigmoid was used on the output layer. For the compilation the optimizer is adam and the loss function is binary_crossentropy.

Were you able to achieve the target model performance?

No we were not as the model accuracy was under 75%.

What steps did you take to try and increase model performance?

We attempted to increase the performance of the model through several steps. We applied bucketing to the feature ASK_AMT and organized the different values by intervals. We then increased the number of neurons on one of the hidden layers. We also tried using a model with three hidden layers. Finally, we tried a different activation function (tanh). Unfortunately none of these steps gave an accurracy above 75%.

## Summary
The deep learning neural network model used failed to reach 75% accuracy so it's likely the wrong model to be used for this analysis. Alternatively we could try using the Random Forest Classifier to combine a multitude of decision trees to generate a classified output and then evaluate its performance by comparing it to our own model.
