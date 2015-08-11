# Handwritten-Digits-Classification
A novel appraoch to classify handwritten digits and comparison with traditional methods.
Classified MNIST dataset of handwritten digits through Multilayer Perceptron (MLP) feed forward and back
propagation algorithm. Accuracy ~ 96% on test data. Incorporated regularization on weights and tuned hyper-parameters

Model	| Parameters | 	Accuracy
------|------------|-----------
Multilayer Perceptron Neural Network	| 1 hidden layer |	96.45%
Naive Bayes Classifier |	Bernoulli RV features | 	83.98%
Hybrid Bayes-Neural Network	| At hidden layer, Multinoulli RV features	| 89.02%
Hybrid Bayes-Neural Network	| At output layer; Multinoulli RV features	| 90.66%
Hybrid Bayes-Neural Network	| At hidden layer; Guassian RV features	| 91.63%
Hybrid Bayes-Neural Network	| At output layer, Guassian RV features	| 93.27%

###Multi-layer Perceptron Neural Network (Accuracy: 96.45%)
 
Each pixel of the input image is used as features to the models. A single hidden layer model with sigmoid units is used. The weights of neural network are learnt using back-propagation algorithm and regularization is implemented to prevent over-fitting. Effects of various hyper-parameters of the neural network on its accuracy are also presented.

###Hybrid Bayer-Neural Network (Guassian features)<br>
(Accuracy when connected at hidden layer: 91.63% )<br>
(Accuracy when connected at output layer: 93.27% )<br>

The network is built on the motivation that intermediate layers or output layer of the neural network can be considered as the features extracted from the input. These features are then considered independent nodes of naive bayes network. The nodes of the neural network are considered to be guassian random varialbe features. Parameter estimation for all the features are done using likelihood method.<br>Classification is done with this constructed naive bayes model.<br>The connection between the bayes and neural network is tested both at hidden layer and output layer.

###Confusion Matrix

**Multilayer Perceptron Neural Network**
![Model_Accuracy](/results/mlpnn_confusion.png)
**Naive Bayes**
![Model_Accuracy](/results/conf_matrix_naive_bayes.png)
**Bayes-Neural Network (at hidden layer, Multinoulli RV features)**
![Model_Accuracy](/results/conf_matrix_nn_bayes_hid.png)
**Bayes-Neural Network (at output layer, Multinoulli RV features)**
![Model_Accuracy](/results/conf_matrix_nn_bayes_out.png)
**Bayes-Neural Network (at hidden layer, Guassian RV features)**
![Model_Accuracy](/results/conf_matrix_norm_nnbayes_hid.png)
**Bayes-Neural Network (at output layer, Guassian RV features)**
![Model_Accuracy](/results/conf_matrix_norm_nn_bayes_out.png)
