Here’s a polished and complete version of your README content with the Environment Setup formatted properly and continuation for usage and instructions:

---

# Counterfeit Currency Detection Using CNN and SVM

## Project Description

This project implements two machine learning techniques to detect counterfeit currency notes:

1. **Support Vector Machine (SVM)** using Histogram of Oriented Gradients (HOG) features
2. **Convolutional Neural Network (CNN)** leveraging deep learning for image classification

The dataset consists of images of 500 rupee Indian currency notes labeled as real or fake. The goal is to accurately classify the authenticity of currency notes.

---

## Dataset Structure

* `REAL_SVM/` - Images of genuine currency notes
* `FAKE_SVM/` - Images of counterfeit currency notes
* `Features/` - Cropped images highlighting important features
* `final_label.csv` - CSV file with columns:

  * `image_path`: relative path to image
  * `label`: 0 for Real, 1 for Fake

---

## Environment Setup

### Required Python Packages

```bash
pip install numpy pandas opencv-python scikit-image scikit-learn tensorflow matplotlib joblib
```

---

## Usage

### 1. Train SVM Model

Run the script that extracts HOG features and trains an SVM classifier:

```bash
python svm_training.py
```

### 2. Train CNN Model

Run the script that prepares image data and trains a CNN:

```bash
python cnn_training.py
```

### 3. Prediction

Use the trained models to predict if a currency note is real or fake:

```bash
python predict.py --model svm --image path/to/image.jpg
```

or

```bash
python predict.py --model cnn --image path/to/image.jpg
```

---

## Folder Structure (Example)

```
CounterfeitCurrencyDetection/
│
├── REAL_SVM/
│   ├── real_note_1.jpg
│   ├── real_note_2.jpg
│   └── ...
│
├── FAKE_SVM/
│   ├── fake_note_1.jpg
│   ├── fake_note_2.jpg
│   └── ...
│
├── Features/
│   ├── feature_crop_1.jpg
│   └── ...
│
├── final_label.csv
├── svm_model.joblib
├── cnn_model.h5
├── svm_training.py
├── cnn_training.py
├── predict.py
└── README.md
```
