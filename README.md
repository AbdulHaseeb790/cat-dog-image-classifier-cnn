# Cat vs Dog Image Classifier using CNN

## Overview

This project implements a Convolutional Neural Network (CNN) using TensorFlow and Keras to classify images as either a cat or a dog.

The model is trained on a labeled image dataset and learns visual features such as edges, shapes, textures, and object patterns to perform binary image classification.

---

## Project Objective

The goal of this project is to understand:

- Image preprocessing
- Convolutional Neural Networks (CNNs)
- Feature extraction
- Model training and evaluation
- Binary image classification

---

## Dataset

Dataset Structure:

```text
dataset/
└── cats_dogs_light/
    ├── train/
    └── test/
```

- Images are resized to 224 × 224 pixels
- Pixel values are normalized between 0 and 1
- Two classes:
  - Cat
  - Dog

---

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Google Colab

---

## Model Architecture

```text
Input Image (224 × 224 × 3)
        │
        ▼
Conv2D (32 Filters)
        │
MaxPooling2D
        │
        ▼
Conv2D (64 Filters)
        │
MaxPooling2D
        │
        ▼
Conv2D (128 Filters)
        │
MaxPooling2D
        │
        ▼
Flatten
        │
Dense (128)
        │
Dense (1, Sigmoid)
```

---

## Training Configuration

| Parameter | Value |
|------------|---------|
| Optimizer | Adam |
| Loss Function | Binary Crossentropy |
| Batch Size | 32 |
| Image Size | 224 × 224 |
| Output Activation | Sigmoid |

---

## Model Performance

Final Results:

| Metric | Value |
|----------|----------|
| Training Accuracy | ~80% |
| Validation Accuracy | ~71% |

The model successfully learned basic visual patterns and was able to classify unseen cat and dog images with reasonable accuracy.

---

## Prediction Example

```python
prediction = model.predict(img_array)

if prediction[0] > 0.5:
    print("Dog")
else:
    print("Cat")
```

---

## Workflow

```text
Image
  ↓
Preprocessing
  ↓
CNN Feature Extraction
  ↓
Classification Layer
  ↓
Prediction
```

---

## What I Learned

Through this project, I learned:

- Image preprocessing techniques
- CNN architecture fundamentals
- Feature extraction using convolution layers
- Pooling operations
- Model evaluation using accuracy and loss
- Binary image classification using TensorFlow and Keras

---

## Future Improvements

- Data Augmentation
- Dropout Layers
- Transfer Learning with VGG16
- Transfer Learning with ResNet50
- Model Deployment using Streamlit

---

## Author

Abdul Haseeb Jamali

Software Engineering Student

Learning Artificial Intelligence and Machine Learning through practical projects.
