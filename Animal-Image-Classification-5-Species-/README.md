# 🐾 Animal Image Classification (5 Species)

A Deep Learning project that builds and trains a **Convolutional Neural Network (CNN)** from scratch using **TensorFlow / Keras** to classify images into 5 distinct animal species: **cat, cow, deer, dog, and lion**. 

The dataset is programmatically fetched via `kagglehub`, validated for image integrity, preprocessed using Keras data utilities, and evaluated with a visual confusion matrix and classification metrics.

---

## 📁 Dataset Directory Layout

The project uses the `miadul/animal-image-classification-5-species` dataset, automatically structured into training, validation, and testing subdirectories:

```text
animals_dataset/
│
├── train/
│   ├── cat/
│   ├── cow/
│   ├── deep/  # Deer class directory
│   ├── dog/
│   └── lion/
│
├── validation/
│   ├── cat/
│   ├── cow/
│   ├── deep/
│   ├── dog/
│   └── lion/
│
└── test/
    ├── cat/
    ├── cow/
    ├── deep/
    ├── dog/
    └── lion/
