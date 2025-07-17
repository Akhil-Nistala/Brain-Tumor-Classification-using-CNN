# 🧠 Brain Tumor Detection using CNN

This project uses a **Convolutional Neural Network (CNN)** to classify MRI brain scans into two categories: **Tumor** or **No Tumor**.

---

## 📌 Objective

The goal of this project is to **automate the detection of brain tumors** from MRI images using deep learning. Early detection of brain tumors is critical, and this model aims to assist medical professionals by providing an initial assessment.

---

## 📂 Dataset

* **Source**: [Brain MRI Images for Brain Tumor Detection](https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection)
* **Classes**:

  * `YES`: Tumor Present → Encoded as `1`
  * `NO`: No Tumor → Encoded as `0`

⚠️ Note: The dataset does not include metadata like patient age, gender, or scan origin.

---

## 🧠 What is a Brain Tumor?

A brain tumor is an abnormal growth of cells in the brain. It can be:

* **Benign** (non-cancerous)
* **Malignant** (cancerous)

MRI scans are crucial for tumor detection. This project automates image classification to detect tumors efficiently.

---

## 🧬 Model Architecture

We built a **CNN model** using Keras. Below is the structure:

### 🔧 Layers:

* **Convolutional Layers**: Extract features from MRI scans using 32 and 64 filters
* **Batch Normalization**: Stabilizes and speeds up training
* **Max Pooling**: Reduces image size and retains key features
* **Dropout**: Prevents overfitting
* **Flatten + Dense Layers**: Convert features into class predictions
* **Output Layer**: 2 neurons with `softmax` for binary classification

### 🛠 Compilation:

* **Loss Function**: `categorical_crossentropy`
* **Optimizer**: `Adamax`
* **Activation**: ReLU for intermediate layers, Softmax for output

---

## 📈 Training Details

* **Epochs**: 40
* **Batch Size**: 40
* **Input Shape**: 128x128 RGB images
* **Verbose**: 1 (progress shown per epoch)

During training, the model learns to minimize prediction error using both **training loss** and **validation loss** as feedback.

---

## 📉 Training Progress

* The loss steadily decreases over epochs
* Training and validation losses converge — indicating good generalization
* Helps assess when the model is underfitting or overfitting

### 📊 Loss Plot

A plot of training vs. validation loss helps visualize learning trends and detect overfitting early.

---




