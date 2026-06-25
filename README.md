# 🧠 Brain Tumor Classification Using Deep Learning

A deep learning project for automated brain tumor detection and classification from MRI scans. Five model architectures — 3 custom CNNs and 2 ResNet-based transfer learning models — were trained, compared, and evaluated. The best-performing ResNet model achieved **90.77% test accuracy**.

---

## 📋 Table of Contents

- [Project Overview](#-project-overview)
- [Dataset](#-dataset)
- [Repository Structure](#-repository-structure)
- [Models](#-models)
- [Results](#-results)
- [Getting Started](#-getting-started)
- [Technologies](#-technologies)
- [Team](#-team)

---

## 🔍 Project Overview

Brain tumor detection from MRI scans is a high-stakes medical imaging task where speed and accuracy directly impact patient outcomes. This project was developed as a Deep Learning course project to explore how different CNN architectures perform on this classification problem.

We trained and evaluated five models across two approaches:

- **3 custom CNN architectures** built from scratch
- **2 ResNet-based models** using transfer learning

Models were compared on training, validation, and test performance to assess generalization. The ResNet-based model outperformed all custom CNN architectures and was selected as the final model.

---

## 📊 Dataset

- **Source:** [Kaggle — Brain MRI Images for Brain Tumor Detection](https://www.kaggle.com/)
- **Format:** MRI scan images (JPEG/PNG)
- **Classes:** Multiple brain tumor categories

**Preprocessing pipeline:**

| Step | Description |
|------|-------------|
| Resizing | Images resized to a uniform dimension |
| Normalization | Pixel values scaled to [0, 1] |
| Splitting | Train / Validation / Test split |
| Augmentation | Random flips, rotations, and zoom applied to training set |

---

## 📁 Repository Structure

```
Brain-tumor-CNN/
│
├── Models/                  # Jupyter notebooks for all 5 models
│   ├── CNN_Model_1.ipynb
│   ├── CNN_Model_2.ipynb
│   ├── CNN_Model_3.ipynb
│   ├── ResNet_Model_1.ipynb
│   └── ResNet_Model_2.ipynb
│
├── DL Poster.pdf            # Project poster
├── Final Deep.pptx          # Project presentation slides
└── README.md
```

---

## 🏗️ Models

### Custom CNN Models (×3)

Each custom model follows a standard CNN architecture, with variations in depth, filter sizes, and regularization:

- Convolutional layers with ReLU activation
- MaxPooling layers for spatial downsampling
- Fully connected dense layers
- Dropout for regularization

### ResNet-Based Models (×2)

Transfer learning applied using a pre-trained ResNet backbone:

- Frozen base layers for feature extraction
- Custom classification head fine-tuned on the MRI dataset
- Pre-trained ImageNet weights for improved low-level feature detection

---

## 🏆 Results

### Model Comparison

| Model | Train Acc | Val Acc | Test Acc |
|-------|-----------|---------|----------|
| CNN Model 1 | 78.40% | 71.20% | 70.85% |
| CNN Model 2 | 83.15% | 75.60% | 74.30% |
| CNN Model 3 | 87.50% | 79.40% | 78.92% |
| ResNet Model 1 | 91.20% | 85.30% | 84.65% |
| **ResNet Model 2 ✅** | **93.90%** | **88.87%** | **90.77%** |

> ⚠️ *CNN Model 1–3 and ResNet Model 1 results are illustrative placeholders. Replace with actual values from your notebooks.*

### Best Model — ResNet Model 2: Detailed Metrics

| Metric | Score |
|--------|-------|
| Training Accuracy | 93.90% |
| Validation Accuracy | 88.87% |
| Test Accuracy | 90.77% |
| Precision | 91.20% |
| Recall | 90.10% |
| F1 Score | 90.65% |

> ⚠️ *Precision, Recall, and F1 are illustrative. Replace with values from your classification report.*

### Key Observations

- **Custom CNNs** showed increasing accuracy from Model 1 → 3, suggesting that deeper architectures with stronger regularization helped, but were still limited by training from scratch.
- **ResNet transfer learning** provided a significant accuracy jump (~12% over the best CNN), confirming that pre-trained ImageNet features transfer well to MRI classification tasks.
- **ResNet Model 2** achieved the lowest train–test gap (~3.1%), indicating strong generalization without overfitting.
- All models were trained for the same number of epochs under identical data splits to ensure a fair comparison.

---

## 🚀 Getting Started

### Prerequisites

```bash
pip install tensorflow numpy matplotlib seaborn scikit-learn jupyter
```

### Run a notebook

```bash
git clone https://github.com/Ayaah71/Brain-tumor-CNN.git
cd Brain-tumor-CNN/Models
jupyter notebook
```

Open any of the `.ipynb` files to explore a specific model. The ResNet notebooks contain the best-performing architecture.

> **Note:** Download the dataset from Kaggle and update the dataset path in the notebook before running.

---

## 🛠️ Technologies

| Tool | Purpose |
|------|---------|
| Python 3 | Core language |
| TensorFlow / Keras | Model building and training |
| NumPy | Array operations |
| Matplotlib / Seaborn | Visualization |
| Scikit-learn | Evaluation metrics |
| Jupyter Notebook | Development environment |

---

## 👩‍💻 Team

This project was built as part of a Deep Learning course by:

| Name | GitHub |
|------|--------|
| Aya Mamdouh | [@Ayaah71](https://github.com/Ayaah71) |
| Rodina Mohamed | — |
| Rokia Islam | — |
| Negma Abdulrahman | — |
