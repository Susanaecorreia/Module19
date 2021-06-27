# Module19

# Overview of the analysis: Explain the purpose of this analysis.

The purpose of this project is to use deep-learning neural networks, with the TensorFlow platform in Python, to analyze and classify the success of charitable donations.

# Results: Using bulleted lists and images to support your answers, address the following questions.

  # Data Preprocessing

  
What variable(s) are considered the target(s) for your model?

   - The column IS_SUCCESSFUL is the target for our deep learning neural network.
  
What variable(s) are considered to be the features for your model?

  - The following columns APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT are the features for our model.
  
What variable(s) are neither targets nor features, and should be removed from the input data?

  - The columns EIN and NAME are identification information and have been removed from the input data.

  # Compiling, Training, and Evaluating the Model
  
How many neurons, layers, and activation functions did you select for your neural network model, and why?

  - This deep-learning neural network model is made of two hidden layers with 80 and 30 neurons respectively. The input data has 43 features and 25,724 samples.
The output layer is made of a unique neuron as it is a binary classification. To speed up the training process, we are using the activation function ReLU for the hidden layers. As our output is a binary classification, Sigmoid is used on the output layer.
For the compilation, the optimizer is adam and the loss function is binary_crossentropy.

Were you able to achieve the target model performance?

  - The model accuracy is under 75%. This is not a satisfying performance to help predict the outcome of the charity donations.

What steps did you take to try and increase model performance?

  - To increase the performance of the model, we applied bucketing to the feature ASK_AMT and organized the different values by intervals.
We increased the number of neurons on one of the hidden layers, then we used a model with three hidden layers.

# Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.

The deep learning neural network model did not reach the target of 75% accuracy. Considering that this target level is pretty average we could say that the model is not outperforming. Since we are in a binary classification situation, we could use a supervised machine learning model such as the Random Forest Classifier to combine a multitude of decision trees to generate a classified output and evaluate its performance against our deep learning model.
