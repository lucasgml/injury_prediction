# injury_prediction
Applying machine learning methods for predicting knee ligament injuries

##### Overview

Applied four machine learning models (Decision Tree, Random Forest, SVM and MLP) for predicting if a patient will have a new injury based on several attributes

This dataset was collect as a part of a Master's degree thesis in physiotherapy and names of the patients were removed from data.csv. More data are being collected and this analysis will be updated as soon as it becomes available.

The attributes of the dataset are written in portuguese and the label is the feature "<i>Você sofreu uma nova lesão do ligamento cruzado anterior?</i>" (<i>Have you suffered a new injury on knee ligament?</i>)

##### PCA

The PCA was used to decrease the number of features in the model. My approach was to reduce the number of features by 28 considering those that had a high correlation.

##### Imbalanced data

My approach for solving balancing issues was using SMOTE for upsampling the minor class.

##### Results

Talking about the results, the models achieved between 86% and 96% of accuracy. 
Some notes were taken:

* Decision Tree had the worst accuracy
* Random Forest had a poor performance due to the curse of dimensionality. It always predicts only one class
* SVM and Neural Networks achieved the best results considering accuracy, recall, precision and F1-score
* I implemented a MLP with TensorFlow and it achieved very similar results to the sklearn implementation
* I collected some percentage predictions based on the outputs of the last layer (softmax activation function) of the TensorFlow's implementation. Find below a screenshot of these results

<img src=screenshots/screenshot.png>

