👁️ Diabetic Retinopathy (DR) Detection using Deep Learning
This project implements and compares two distinct deep learning approaches for the multi-class classification of Diabetic Retinopathy severity using fundus images: a Custom Convolutional Neural Network (CNN) and a Transfer Learning model based on EfficientNetB0.

🔬 Models Implemented
The repository includes two main Jupyter notebooks, each detailing the implementation of a separate model:

1. Custom CNN Model (CNN.ipynb)
This notebook defines a Sequential CNN model built from scratch.

Model/Algorithm Used: Convolutional Neural Network (CNN) for 5-class classification.

Structure:

3 Convolutional layers (with 32, 64, 128 filters).

MaxPooling layers.

Flatten layer.

Dense hidden layer (128 units, ReLU activation).

Dropout layer (0.5) for regularization.

Output layer: Dense(5, softmax) for multi-class prediction.

2. EfficientNetB0 Transfer Learning (efficientnetb0.ipynb)
This notebook utilizes a powerful pre-trained architecture, EfficientNetB0, for high-performance feature extraction.

Approach: Transfer Learning using pre-trained weights (e.g., ImageNet).

Customization: The pre-trained EfficientNetB0 base is typically frozen, and custom Dense layers are added on top for the final 5-class classification.

Advanced Preprocessing: The notebook includes techniques tailored for fundus images, such as:

autocrop_black: Removing black borders.

circular_crop: Applying a circular mask to focus on the retinal area.

Image resizing to the required input size (e.g., (224, 224)).

📂 Dataset
Feature	Description
Dataset	APTOS 2019 Blindness Detection dataset
Goal	Multi-class classification of Diabetic Retinopathy severity.
Classes	5 classes (0 to 4): 0: No DR, 1: Mild, 2: Moderate, 3: Severe, 4: Proliferative DR.
📈 Model Performance Highlights
The models were evaluated on the validation set of the APTOS 2019 dataset.

Model	Validation Accuracy	Training Accuracy
Custom CNN	0.9505 (95.05%)	0.9792 (97.92%)
EfficientNetB0	[Placeholder: typically higher, e.g., 97.5%]	[Placeholder: e.g., 99.1%]
Note: The EfficientNetB0 notebook contains detailed metrics, including Confusion Matrices and Cohen's Kappa score, which is a critical metric for imbalanced medical datasets.

🚀 Setup and Usage
To replicate the results or train the models:

Clone the Repository:

Bash

git clone [Your Repository URL]
cd [your-repo-name]
Set Up Environment: Install necessary libraries. This project requires TensorFlow/Keras and standard data science tools.

Bash

pip install tensorflow pandas numpy matplotlib scikit-learn opencv-python
Prepare Data: Download the APTOS 2019 dataset and organize the images and CSV labels according to the paths specified in the notebooks.

Run Notebooks: Open and run the notebooks sequentially:

Bash

jupyter notebook CNN.ipynb
jupyter notebook efficientnetb0.ipynb