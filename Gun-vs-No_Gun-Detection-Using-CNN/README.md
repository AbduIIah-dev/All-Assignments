# 🎯 Gun vs No-Gun Classification System

An end-to-end Computer Vision project featuring a Binary Convolutional Neural Network (CNN) built with TensorFlow/Keras and deployed using an interactive Gradio web interface.

---

## 📊 Model Performance & Metrics

To prevent overfitting and ensure strong generalization on unseen real-world data, early stopping and metric monitoring were applied during training.

* **Training Accuracy:** ~87.1%
* **Test Accuracy:** ~83.8%
* **Loss Metric:** Binary Cross-Entropy
* **Key Improvements:** Applied Data Augmentation, Dropout layers, and EarlyStopping callbacks to reduce original overfitting gap from ~18% down to ~3%.

---

## 🛠️ Project Architecture & Pipeline

1. **Preprocessing & Augmentation:**
   * Rescaling pixel intensities to `[0, 1]` range.
   * Applying random horizontal flips, rotations, and zoom transformations.
2. **Model Architecture:**
   * Custom Functional/Sequential CNN with Conv2D, MaxPooling2D, and Dense layers.
   * Sigmoid activation in the final layer for binary probability output.
3. **Training & Callbacks:**
   * `ModelCheckpoint`: Auto-saves the optimal model state based on lowest `val_loss`.
   * `EarlyStopping`: Prevents training redundancy with `restore_best_weights=True`.
4. **Deployment Interface:**
   * Lightweight web application built using **Gradio** for real-time visual inferencing.

---

## 🚀 How to Run Locally

### 1. Requirements
Ensure you have the following Python packages installed:
```bash
pip install tensorflow numpy pillow gradio scikit-learn
