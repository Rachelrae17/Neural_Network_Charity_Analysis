# Neural_Network_Charity_Analysis
Module 19

Overview: The purpose of this project is to use deep-learning neural networks with the TensorFlow platform in Python, to analyze and classify the success of charitable donations. The methods that were used for the analysis were, preprocessing the data for the neural network model,compile, train and evaluate the model,
optimize the model.Alphabet Soup, a non-profit organization focusing on environmental protection, regularly funds the activities of other similarly-minded organizations. Alphabet Soup has compiled a rich dataset of previous applications for funding and the results of the funding.


Results:

Data Preprocessing- 
The columns EIN and NAME are identification information and have been removed from the input data.
The column IS_SUCCESSFUL contains binary data refering to weither or not the charity donation was used effectively. This variable is then considered as the target for our deep learning neural network.
The following columns APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT are the features for our model.
Encoding of the categorical variables, spliting into training and testing datasets and standardization have been applied to the features.

![Steo 1](https://user-images.githubusercontent.com/95897182/167731267-da6c712f-587a-440e-a21c-2ebfbe7586aa.png)


Compiling, Training, and Evaluating the Model- 
This deep-learning neural network model is made of two hidden layers with 80 and 30 neurons respectively.
The input data has 43 features and 25,724 samples.The output layer is made of a unique neuron as it is a binary classification.
To speed up the training process, we are using the activation function ReLU for the hidden layers. As our output is a binary classification, Sigmoid is used on the output layer.For the compilation, the optimizer is adam and the loss function is binary_crossentropy.The model accuracy is under 75%. This is not a satisfying. performance to help predict the outcome of the charity donations.To increase the performance of the model, we applied bucketing to the feature ASK_AMT and organized the different values by intervals.We increased the number of neurons on one of the hidden layers, then we used a model with three hidden layers.
We also tried a different activation function (tanh) but none of these steps helped improve the model's performance.

![Step 2](https://user-images.githubusercontent.com/95897182/167731551-578632ae-4322-4789-9968-591ba89b2b85.png) 

Summary: 
The deep learning neural network model did reach the target of 73% accuracy. Considering that this target level is pretty average we could say that the model is not outperforming.Since we are in a binary classification situation, we could use a supervised machine learning model such as the Random Forest Classifier to combine a multitude of decision trees to generate a classified output and evaluate its performance against our deep learning model.There are several options for improving the model. One option would be to use the techniques mentioned above but in combination. Perhaps this would increase the accuracy above 75%, but that is yet to be determined. A second option would be to increase the size of the training dataset. Additional data would likely give the model more opportunity to learn and thereby increase the accuracy. A third option would be to use a different binary classifier, such as the Random Forest Classifier.



