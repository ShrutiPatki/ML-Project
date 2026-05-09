Pneumonia Detection using Deep Learning
Overview

This project focuses on pneumonia classification from chest X-ray images using deep learning models. Multiple architectures were implemented and compared to study their performance, generalization, and interpretability.

The models used in this project are:
Custom CNN
ResNet18
DenseNet121 (Transfer Learning)

The project also includes:
ROC-AUC analysis
Grad-CAM visualization
Threshold analysis
Data augmentation experiments
Dataset

Dataset used:

mmenendezg/pneumonia_x_ray

Classes:
Normal
Pneumonia

The dataset was divided into training, validation, and test sets. Images were resized and normalized before training.

Models Implemented
1. Custom CNN
A lightweight CNN built from scratch using:
Convolutional layers
MaxPooling
Global Average Pooling
Dropout regularization

This model was used as a baseline architecture.

2. ResNet18
A ResNet18-inspired model using:
Residual blocks
Skip connections
Batch normalization

ResNet18 helps improve gradient flow and allows deeper feature learning.

3. DenseNet121
DenseNet121 was implemented using transfer learning with pretrained ImageNet weights.
The pretrained layers were frozen and used for feature extraction, while a new classification layer was trained on the pneumonia dataset.
DenseNet121 achieved the best overall performance.

Training Details
Libraries used:
TensorFlow / Keras
NumPy
Matplotlib
Hugging Face Datasets

Optimization:
Adam optimizer
Binary/Categorical Cross-Entropy loss
Evaluation Metrics

The models were evaluated using:
Accuracy
Precision
Recall (Sensitivity)
Specificity
ROC-AUC

ROC-AUC was used to measure how well the models separate pneumonia and normal classes across different thresholds.
Grad-CAM Analysis
Grad-CAM was used to visualize important regions in the X-rays influencing model predictions.

Observation:

224×224 images produced clearer and more localized heatmaps compared to 128×128 images.
Results Summary
Model	Validation Accuracy	Validation AUC-ROC
Custom CNN	~94%	~0.98
ResNet18	~90%	~0.97
DenseNet121	~96%	~0.99

Key observations:

DenseNet121 showed the best generalization
ResNet18 showed some overfitting
The Custom CNN performed better than expected for a smaller model
Repository Structure
.
├── final_project (1).ipynb
├── Final_project_v2_with_data_augmentation.ipynb
├── README.md

Main notebook:
final_project (1).ipynb
Additional experimentation notebook:
Final_project_v2_with_data_augmentation.ipynb
Running the Project
Install dependencies:
pip install tensorflow datasets matplotlib numpy
Launch Jupyter Notebook:
jupyter notebook

Open:
final_project (1).ipynb
and run the cells sequentially.

Future Work
Possible improvements:
Fine-tuning DenseNet121
More hyperparameter tuning
Additional architectures such as EfficientNet
Improved Grad-CAM analysis
More advanced augmentation techniques
Authors

Machine Learning Project
Pneumonia Classification using Deep Learning
