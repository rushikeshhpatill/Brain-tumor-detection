# 🧠 Brain Tumor Detection Using Deep Learning & Computer Vision (MRI Images)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)
![Deep Learning](https://img.shields.io/badge/Deep%20Learning-CNN%20%7C%20Transfer%20Learning-orange)
![Computer Vision](https://img.shields.io/badge/Computer%20Vision-OpenCV-green?logo=opencv&logoColor=white)
![Framework](https://img.shields.io/badge/Framework-TensorFlow%20%2F%20PyTorch-red)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

An end-to-end Deep Learning and Computer Vision pipeline designed to automatically detect and classify brain tumors from Magnetic Resonance Imaging (MRI) scans. This project leverages image preprocessing techniques and Convolutional Neural Networks (CNNs) / Transfer Learning architectures to assist in early and accurate medical image analysis.

---

## 📋 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Dataset](#dataset)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Methodology & Pipeline](#methodology--pipeline)
- [Installation & Setup](#installation--setup)
- [Usage](#usage)
- [Model Performance](#model-performance)
- [Future Improvements](#future-improvements)
- [Disclaimer](#disclaimer)
- [License](#license)

---

## 🔍 Overview
Early detection of brain tumors is critical for effective treatment planning and improving patient survival rates. Manual examination of MRI scans can be time-consuming and prone to human error. This repository provides an automated computer vision solution that processes raw brain MRI scans, extracts spatial features, and classifies images into tumor categories (e.g., **Glioma**, **Meningioma**, **Pituitary**, or **No Tumor**).

---

## ✨ Features
- **Automated MRI Preprocessing:** Cropping extreme brain contours, skull stripping/noise reduction, contrast enhancement (CLAHE), and image normalization.
- **Data Augmentation:** Rotation, flipping, zooming, and brightness adjustments to prevent overfitting and handle class imbalance.
- **Deep Learning Models:** Custom CNN architecture alongside Transfer Learning baselines (e.g., VGG16, ResNet50, EfficientNet, MobileNetV2).
- **Explainable AI (XAI):** Grad-CAM (Gradient-weighted Class Activation Mapping) visualizations to highlight tumor regions influencing model predictions.
- **Interactive Inference:** Script/Web App (Streamlit/Flask) support for uploading new MRI images and getting real-time predictions.

---

## 📊 Dataset
The model is trained and evaluated on publicly available Brain MRI datasets (such as the [Kaggle Brain Tumor MRI Dataset](https://www.kaggle.com/) / BraTS):
- **Classes:**
  1. `Glioma Tumor`
  2. `Meningioma Tumor`
  3. `Pituitary Tumor`
  4. `No Tumor`
- **Data Split:** 70% Training | 15% Validation | 15% Testing

---

## 🛠️ Tech Stack
- **Programming Language:** Python 3.8+
- **Deep Learning:** TensorFlow / Keras *(or PyTorch)*
- **Computer Vision & Image Processing:** OpenCV (`cv2`), Pillow, Scikit-Image
- **Data Manipulation & Visualization:** NumPy, Pandas, Matplotlib, Seaborn
- **Evaluation Metrics:** Scikit-Learn
- **Deployment (Optional):** Streamlit / Gradio / Flask

---

## 📁 Project Structure
```text
Brain-Tumor-Detection-Using-Deep-Learning-MRI-Images-Detection-Using-Computer-Vision/
│
├── data/                       # Dataset directory (train, val, test)
├── models/                     # Saved trained model weights (.h5 / .pth)
├── notebooks/                  # Jupyter notebooks for EDA & experimentation
│   ├── 01_data_preprocessing.ipynb
│   └── 02_model_training.ipynb
├── src/                        # Source code scripts
│   ├── preprocess.py           # OpenCV contour cropping & augmentation
│   ├── model.py                # CNN & Transfer Learning architectures
│   ├── train.py                # Model training pipeline
│   ├── evaluate.py             # Confusion matrix, ROC-AUC, & metrics
│   └── gradcam.py              # Grad-CAM heatmap generation
├── app.py                      # Web interface for single-image inference
├── requirements.txt            # Project dependencies
└── README.md                   # Project documentation
