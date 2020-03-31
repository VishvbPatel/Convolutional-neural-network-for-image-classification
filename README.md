# Convolutional-neural-network-for-image-classification

This repository contains image classification by convolutional neural network with intel data provided from kaggle.
The data contains 6 categorical images as buildings, forest, glacier, mountain, sea, street. It is divided into training set, test set and prediction set.
     
The code for the dataset is as below.
https://www.kaggle.com/puneet6060/intel-image-classification#10004.jpg

Two seperate files have been added for preprocessing of training and testing dataset. 
Also code for saving the processed dataset interms of features and labels as X and y has been added.
In the third file with title of "Training and testing of Convolutional neural network", the convolutional model is trained and tested. Also the code for saving the code of keras model with optimum result has been added.
The libraries cv2 and os is used for preprocessing of the images. All the images have been converted into grey scale to reduce the dimension of the data and space of the data. 
In the keras sequential model 2 convolutional layers have been used with window size of (3,3) and activation function of      "relu". Both of the convolutional layers has 64 neurons. The pooling layer has pool size of (2,2) with pooling function of MaxPooling2D. Then there is one Dense layer of 64 neurons and before that flatten is used because the Dense layer only accepts 1D data. The output layer is also a Dense layer with "softmax" activation and 6 neurons. Then in "model.compile", "sparse_categorical_crossentropy" is used to reduce loss, "adam" is used as an optimizer and 'accuracy' is used for metrics. Then validation split is 0.1, epochs is 5 and batch size is 32 in the training of the model.
