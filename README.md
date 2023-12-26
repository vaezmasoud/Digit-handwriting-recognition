In this problem, we want to build a model that can recognize a handwritten English number.

To carry out this project, MNIST the dataset related to Tensorflow and Keras library in python has been used.

## image normalization and convert labels to one-hot encoding
In this step, the images from the MNIST dataset, whose pixel values are from 0 to 255, are divided by 255 for normalization. This action converts pixel values from 0 to 255 to 0 to 1.

The to_categorical function from the Keras library in TensorFlow is used to convert labels to One-Hot Encoding format.

**One-Hot Encoding** is a technique for converting tags into a binary format that is commonly used for classification problems. In this method, each label is converted into a binary vector in which all elements are 0 except for one element that corresponds to the index of the label and its value is 1.

For example, if the label of an image is from 0 to 9, the to_categorical function converts this label into a binary vector with 10 elements, such that the value 1 is present at the position corresponding to the label, and the remaining elements are 0.

## create model
In this step, we used a model building algorithm called 'Sequential'. Sequential is a layer-by-layer model in Keras that simply adds layers sequentially.

## Is it possible to calculate AUC and ROC Curve for this problem?
In this project, which is a multi-class classification problem, AUC (area under the ROC curve) and ROC (performance characteristic curve) criteria are not directly applicable. These criteria are meaningful for binary classification problems.

In other words, if the number of classes is more than two (such as the problem of recognizing digits from 0 to 9, which has 10 classes), measures such as AUC and ROC are not suitable for directly evaluating the performance of the model.

To evaluate the model in multi-category problems, you can use criteria such as accuracy, confusion matrix, and precision, recall, f1-score. These criteria are based on the number of true and false associations of different categories with reality.

To calculate these metrics in TensorFlow and Keras, you can use functions like evaluate on the model, which is used in the evaluation section.
