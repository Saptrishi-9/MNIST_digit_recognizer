## MNIST - Image Classification

#### About the Dataset: It is a collection of 70,000 handwritten digits used to train and test image processing systems.
#### Format: 28×28 pixel grayscale images.
#### Classes: 10 classes corresponding to digits 0 through 9.
#### Data Structure: Each image consists of 784 pixels (28x28) with intensity values ranging from 0 (black) to 255 (white).

### Pre-processing: 

Reduced Dimensions using PCA
Flatten the data for KNN and SVM, For CNN original data is used without PCA and flattening.

### Approches:

#### 1 - K Nearest Neighbour

Parameters: K=5 (number of neighbours)

Results: Train Accuracy: 97.7%
         Test Accuracy:  96.6%

#### 2 - SVM with RBF Kernel

Parameters:  C=8

Results: Train Accuracy: 99.9%
         Test Accuracy:  98.08%

#### 3 - CNN (Convolutional Neural Network)

1- Batch Normalization is used after every Conv2D layer.
2- l2 regularisation is used with every Conv2D layer except 1st one.
3- Padding is used in every Conv2D layer.
4- MaxPooling2D layer is also used twice.
5- After last MaxPooling2D layer a dropout layer is also added to prevent overfitting.

Results: Train Accuracy: 99.75%
         Test Accuracy: 99.11%


### KAGGLE SCORE: 0.9890


### ! I have split the training data into x_test and x_test and 'Test Accuracy' is calculated on x_test and not on the 'Test' data (which doesn't have labels).