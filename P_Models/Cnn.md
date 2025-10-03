Model/Algorithm Used:

The file uses a Convolutional Neural Network (CNN) for classification, implemented with TensorFlow/Keras. The architecture includes several Conv2D, MaxPooling2D, Flatten, Dense, and Dropout layers, and the model is trained for multiclass (5-class) diabetic retinopathy detection.

Model Structure:

3 Convolutional layers (with 32, 64, 128 filters)

MaxPooling, Flatten, Dense (128 units, ReLU), Dropout (0.5)

Output layer: Dense(5, softmax)

Accuracy:

At the end of training, the highest training accuracy = 0.9792 (97.92%)

The highest validation accuracy = 0.9505 (95.05%)