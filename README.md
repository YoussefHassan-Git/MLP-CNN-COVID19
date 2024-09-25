# 🧬 COVID-19 Detection using CNN and MLP 
This project uses **Convolutional Neural Networks (CNN)** and **Multi-Layer Perceptron (MLP)** to detect COVID-19 from medical images. The dataset used for training contains chest X-rays, and the model aims to classify images into **COVID-positive** or **COVID-negative** categories.
## 📚 Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Model Architecture MLP](#model-architecture-mlp)
- [CNN Model Architecture](#cnn-model-architecture)
  
- [Training](#training)
- [Data Preprocessing](#data-preprocessing)
- [Model Performance](#model-performance)
- [Sample Images](#sample-images)
- [Training and Validation Graphs](#training-and-validation-graphs)
- [Testing Sample Output](#testing-sample-output)

  
---

## 🛠️ Project Overview

This project detects COVID-19 in chest X-ray images using deep learning models:
- **Convolutional Neural Network (CNN)** extracts spatial features from the X-ray images.
- **Multi-Layer Perceptron (MLP)** performs classification using the learned features from CNN.

---

## 📁 Dataset

The dataset consists of chest X-rays labeled as **COVID-positive** and **Normal** And **Pneumonia**. The data is pre-processed and split into training, validation, and test sets.


---

## ⚙️ Data Preprocessing

- Images were resized to 224x224 pixels to ensure uniformity.
- Pixel values were normalized to the range [0, 1] for better model convergence.

---

## 🏗️ Model Architecture MLP

The **Multi-Layer Perceptron (MLP)** model used in this project consists of an input layer, multiple hidden layers, and an output layer. The model is designed to classify images into one of three categories.

### 📑 Model Summary

- **Input Layer**: The input layer flattens the 3D image array of shape (224, 224, 3) into a 1D vector.
- **Hidden Layers**:
  - Three fully connected (`Dense`) hidden layers with **ReLU** activation.
  - The first hidden layer has **128 neurons**, the second has **64 neurons**, and the third has **128 neurons** again.
- **Output Layer**: The output layer uses a `Dense` layer with **3 neurons** (for 3 output classes) and a **softmax** activation function for multi-class classification.

---
## 🏗️ CNN Model Architecture

The **Convolutional Neural Network (CNN)** model is designed to automatically learn spatial hierarchies of features from input images. The model includes several convolutional layers, max-pooling layers, and fully connected layers, making it highly effective for image classification tasks.

### 📑 Model Summary

- **Input Layer**: Takes 224x224 RGB images as input.
- **Convolutional Layers**: Three convolutional layers with `ReLU` activation to extract features from images.
- **Pooling Layers**: Max-pooling layers used to down-sample the feature maps, reducing their spatial dimensions.
- **Fully Connected Layers**: Two fully connected layers with `ReLU` activation to perform the classification.
- **Output Layer**: A softmax layer with three output neurons for multi-class classification.


---

## 📈 Model Performance
`MLP`
The model achieved the following metrics on the test data:
- **Training Accuracy**: ~80%
- **Validation Accuracy**: ~83%
- **Testing Accuracy**: ~83%
---
`CNN`
The model achieved the following metrics on the test data:
- **Training Accuracy**: ~95%
- **Validation Accuracy**: ~87%
- **Testing Accuracy**: ~87%
---

## 📊 Training and Validation Graphs

 `MLP Model`
 
**Training and Validation Loss:**

![13eed7a9-5029-49be-b72a-eb89062c821c](https://github.com/user-attachments/assets/9ffbb201-bb6c-4fe1-86c6-5a49e6d863e9)


**Training and Validation Accuracy:**

![3a122eac-13eb-442e-93a8-aebef6c168c1](https://github.com/user-attachments/assets/58bb2f1c-c383-4564-99e2-18d54550f90e)
---
`CNN Model`


**Training and Validation Loss:**

![27ba904f-c66c-471b-bb9f-460295ca4c0e](https://github.com/user-attachments/assets/a59ddf41-ed68-4599-b9d0-cf35e08bc87f)

**Training and Validation Accuracy:**

![25c09469-a8e8-4f9e-9f17-48f754bb7697](https://github.com/user-attachments/assets/4b739ff1-5aa8-4d3e-891f-6a408b279204)


---

## 📷 Sample Images

![31891d00-0c4e-4c7c-8d50-7261929242ed](https://github.com/user-attachments/assets/2eecbf51-79bc-4880-8326-ac3f8d13bfd9)


## Testing Sample Output

![db63ff15-1042-4485-88dc-35cb8fb30742](https://github.com/user-attachments/assets/db4de75d-182e-493d-93eb-acc95a389d82)

