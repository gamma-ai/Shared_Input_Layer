# Numerai_Shared_Input_Layer
Required Packages:
Pandas
Keras
TensorFlow/TensorBoard
Sklearn
Numpy

GUIDE TO KERAS FUNCTIONAL API:->https://keras.io/getting-started/functional-api-guide/#first-example-a-densely-connected-network

"The Sequential model is probably a better choice to implement such a network, but it helps to start with something really simple.
*A layer instance is callable (on a tensor), and it returns a tensor
*Input tensor(s) and output tensor(s) can then be used to define a Model
*Such a model can be trained just like Keras Sequential models."

"All models are callable, just like layers
With the functional API, it is easy to reuse trained models: you can treat any model as if it were a layer, by calling it on a tensor. Note that by calling a model you aren't just reusing the architecture of the model, you are also reusing its weights."

Predicting the probablilities of a dataset of encrypted Stock Prices(We have no idea what the features are.The goal will be to build a model that can differentiate whether stock prices are go to rise or fall to buy or sell shares in a hedgefund. 
Achieving this goal will require to  build a model that Scales prices into two vectors, concatenates the vectors and then adds a logistic regression, this outputs a probability that the stock prices are low or high.


Download Data here :-> https://numer.ai/rounds

Conduct experimentation on Numerai Datasets to maintain a logarithmic loss of &lt;=.693 Via Shared Input Layer.

Training data - a CSV file containing rows of features and their binary target values. Use this to train your machine learning model.
Tournament data - a CSV file with the same structure containing rows for validation, test and live. Run your trained model against these rows to generate your predictions.


Each ID represents an asset and each era represents a unit period of time. There are 50 unlabeled features to train on and 5 unlabeled targets to predict on. The data itself has been obfuscated in such a way that certain structural relationships are preserved but the true labels of the features and targets remain secret.

Once you get to play around with the data more, you may also notice how clean it is. This is because we have already done the tedious cleaning and regularization work for you so you can focus on the modelling.

Example models - included in the datazip are two basic classifier scripts in Python and R to get you started. Try generating predictions with the example models before making your own.

Example predictions - also included are examples prediction files that are ready for submission. Hint: if you have having issues submitting your own predictions, compare them against these examples to make sure they are formatted correctly.

Submitting predictions - submit your predictions via the website or directly through the API. You can update your submissions as many times as you like while the submission window is open. However, you may no longer update your submission once you stake on it.

All predictions submitted to Numerai will be scored publically.

AUC - the primary scoring metric we use to evaluate your performance. You can learn more about this metric from sklearn.
Your live AUC score will be calculated and revealed once the round resolves. This score will be used to determine any payouts or bonuses. To note, test scores are never revealed to prevent overfitting to the test set.

Concordance - a secondary metric to we use to determine if validation, test and live predictions appear to be produced by the same model. Concordance is only used to determine staking eligibility and is revealed immediately upon submission.
Leaderboard - doing well consistently will earn you a place on the leaderboard. Users are ranked by reputation: the number benchmarks beat in the past 20 resolved rounds.

The code to calculate these metrics is open source. Check it out at numerai/submission-criteria.
