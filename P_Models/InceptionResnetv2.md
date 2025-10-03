Model/Algorithm Used:

This file uses the InceptionResNetV2 deep learning architecture for multiclass diabetic retinopathy classification. The pipeline follows a multistage training method, with the base model built from TensorFlow's pretrained InceptionResNetV2 (with ImageNet weights) and a custom classification head (AveragePooling, Flatten, Dropout, BatchNorm, Dense softmax output).

Accuracy:

The model achieves a test accuracy of 0.74 (74%) on the validation dataset, as shown by the final evaluation (classification report).