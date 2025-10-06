Model/Algorithm Used:

This file uses the InceptionResNetV2 deep learning architecture for multiclass diabetic retinopathy classification. The pipeline follows a multistage training method, with the base model built from TensorFlow's pretrained InceptionResNetV2 (with ImageNet weights) and a custom classification head (AveragePooling, Flatten, Dropout, BatchNorm, Dense softmax output).

Dataset:

Diabetic Retinopathy 224x224 2019 Dataset from Kaggle.
The notebook processes 3,662 images divided into 5 classes of diabetic retinopathy severity: No DR, Mild, Moderate, Severe, and Proliferative DR.

Accuracy:

The model achieves a test accuracy of 0.74 (74%) on the validation dataset, as shown by the final evaluation (classification report).