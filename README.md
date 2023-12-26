In this problem, we want to build a model that can recognize a handwritten English number.

To carry out this project, MNIST the dataset related to Tensorflow and Keras library in python has been used.

##image normalization and convert labels to one-hot encoding
In this step, the images from the MNIST dataset, whose pixel values are from 0 to 255, are divided by 255 for normalization. This action converts pixel values from 0 to 255 to 0 to 1.

The to_categorical function from the Keras library in TensorFlow is used to convert labels to One-Hot Encoding format.

**One-Hot Encoding** is a technique for converting tags into a binary format that is commonly used for classification problems. In this method, each label is converted into a binary vector in which all elements are 0 except for one element that corresponds to the index of the label and its value is 1.

For example, if the label of an image is from 0 to 9, the to_categorical function converts this label into a binary vector with 10 elements, such that the value 1 is present at the position corresponding to the label, and the remaining elements are 0.
