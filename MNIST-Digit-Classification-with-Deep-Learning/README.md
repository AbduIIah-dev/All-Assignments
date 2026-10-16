# MNIST Handwritten Digit Classification

A Deep Learning project that recognizes handwritten digits from **0 to 9** using the **MNIST dataset**. The project includes data preprocessing, neural network training, model evaluation, and prediction on custom uploaded images through a **Gradio interface**.

## Overview

Handwritten digit recognition is a classic image classification problem in Deep Learning.

In this project, a neural network is trained on the MNIST dataset, where each handwritten digit is represented as a **28 × 28 grayscale image**. After training, the model can be used to predict digits from custom images uploaded through the Gradio interface.

The project demonstrates the complete workflow from **data preprocessing and model training to model inference and interactive deployment**.

## Project Workflow

```text
MNIST Dataset
      ↓
Data Preprocessing
      ↓
Image Normalization
      ↓
Deep Learning Model
      ↓
Model Training
      ↓
Model Evaluation
      ↓
Custom Image Upload
      ↓
Image Preprocessing
      ↓
Digit Prediction
      ↓
Gradio Interface
```

## Dataset

The project uses the **MNIST handwritten digit dataset**.

The dataset contains grayscale images of handwritten digits from **0 to 9**.

Each image has a resolution of:

```text
28 × 28 pixels
```

Therefore, each image contains:

```text
28 × 28 = 784 pixels
```

The pixel values are normalized from the original **0–255 range to 0–1** before being passed to the neural network.

## Data Preprocessing

The images are prepared before training and prediction.

The main preprocessing steps include:

* Converting images into the required format
* Resizing custom images to **28 × 28**
* Converting images to grayscale
* Reshaping the image into **784 input features**
* Normalizing pixel values between **0 and 1**

For custom image prediction, the preprocessing follows this pipeline:

```text
Uploaded Image
      ↓
Grayscale Conversion
      ↓
Resize to 28 × 28
      ↓
NumPy Array
      ↓
Reshape to 1 × 784
      ↓
Normalize Pixel Values
      ↓
Model Prediction
```

## Deep Learning Model

A neural network is trained to perform **multi-class classification** of handwritten digits.

The model learns visual patterns from the MNIST training images and predicts one of the ten possible classes:

```text
0  1  2  3  4  5  6  7  8  9
```

During prediction, the model produces an output for each class. The class with the highest predicted value is selected as the final prediction.

## Custom Image Prediction

After training the model, a custom handwritten digit image can be uploaded for prediction.

The uploaded image is processed to match the same input format used during model training.

For example:

```text
Custom Image
     ↓
Preprocessing
     ↓
Trained Neural Network
     ↓
Predicted Class
```

If the uploaded image contains a handwritten `7`, the model can return:

```text
Predicted Digit: 7
```

## Gradio Interface

The trained model is connected to a **Gradio interface** to make the prediction process interactive.

The user can upload an image through the interface, and the application processes the image and returns the predicted digit.

This provides a simple way to demonstrate the model without requiring users to run individual prediction commands manually.

## Technologies Used

* **Python**
* **NumPy** – numerical operations and array manipulation
* **Pandas** – data handling and analysis
* **TensorFlow / Keras** – Deep Learning model development
* **Pillow (PIL)** – image loading and preprocessing
* **Gradio** – interactive model interface
* **Matplotlib** – visualization and model analysis

## Repository Structure

```text
MNIST/
│
├── mnist.ipynb
├── README.md
└── requirements.txt
```

### `mnist.ipynb`

Contains the complete project workflow, including:

* Dataset loading
* Data exploration
* Preprocessing
* Model creation
* Model training
* Model evaluation
* Custom image prediction
* Gradio interface

### `requirements.txt`

Contains the Python libraries required to run the project.

### `README.md`

Provides an overview of the project, methodology, technologies, and usage.

## Installation

Clone the repository:

```bash
git clone <your-repository-url>
```

Navigate to the project directory:

```bash
cd MNIST
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

## Running the Project

Open the Jupyter Notebook:

```bash
jupyter notebook
```

Then open:

```text
mnist.ipynb
```

Run the notebook cells in order.

The notebook contains both the model training workflow and the Gradio interface for testing the model with custom images.

## Key Learning Outcomes

This project provided practical experience with:

* MNIST image classification
* Image preprocessing
* Grayscale images
* Image resizing
* NumPy arrays and reshaping
* Pixel normalization
* Neural networks
* Multi-class classification
* TensorFlow/Keras
* Model training and evaluation
* Custom image inference
* Gradio model interfaces

## Future Improvements

Possible improvements include:

* Adding prediction confidence scores
* Supporting a drawing canvas for handwritten digits
* Adding real-time webcam digit recognition
* Improving preprocessing for different image backgrounds
* Deploying the Gradio application publicly

## Conclusion

This project demonstrates a complete Deep Learning workflow for handwritten digit classification, starting from the MNIST dataset and ending with an interactive Gradio interface for predicting custom handwritten digit images.

It shows how a trained neural network can be integrated into a simple user-facing application for practical inference.

## Author

**Abdullah Sohail Nasi**

Data Science & Artificial Intelligence Learner
