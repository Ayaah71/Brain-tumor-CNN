🧠 Brain Tumor Classification Using Deep Learning

This project focuses on brain tumor detection and classification from MRI images using deep learning techniques. Multiple CNN architectures and ResNet-based models were trained and evaluated to determine the most effective approach.

📌 Project Overview

Brain tumor detection is a critical task in medical image analysis. In this project, we:

Used a public MRI brain tumor dataset from Kaggle

Built and trained 3 custom CNN models

Implemented 2 ResNet-based models

Compared models using training, validation, and test performance

Selected the best-performing model based on generalization ability

The ResNet model achieved the highest performance among all models.

📊 Dataset

Source: Kaggle

Type: Brain MRI images

Classes: Brain tumor categories 

Preprocessing:

Image resizing

Normalization

Train / validation / test split

Data augmentation (if applicable)

🏗️ Models Implemented
1️⃣ Custom CNN Models (3)

Convolutional layers with ReLU activation

MaxPooling layers

Fully connected layers

Dropout for regularization

2️⃣ ResNet Models (2)

Transfer learning using pre-trained ResNet

Fine-tuning final layers

Improved feature extraction for MRI images

🏆 Best Model Performance (ResNet)
Metric	Accuracy (%)
Training Accuracy	93.90%
Validation Accuracy	88.87%
Test Accuracy	90.77%

✅ The ResNet model demonstrated strong generalization and outperformed the custom CNN architectures.

🛠️ Technologies Used

Python

TensorFlow / Keras (or PyTorch – edit if needed)

NumPy

Matplotlib / Seaborn

Scikit-learn

Created by:

Aya Mamdouh 
Rodina Mohamed 
Rokia Islam 
Negma Abdulrahman 
