# Disaster Localization via Aerial Imagery

This project implements a custom Convolutional Neural Network (CNN) for classifying aerial images from the AIDER dataset into emergency-related categories. The model was trained from scratch using TensorFlow/Keras and achieved competitive results without using any pretrained architecture.

---

## Dataset: AIDER

- **Dataset Size:** 6,433 labeled images
- **Classes:** 5 categories
- **Train/Validation Split:**
  - **Training:** 5,469 images
  - **Validation:** 964 images
- **Source:** AIDER Dataset — [Original Paper Link](https://ieeexplore.ieee.org/abstract/document/9050881)

---

## Model Architecture: Custom CNN

A custom-designed CNN built from scratch. No transfer learning or pretrained backbones were used.

### Key Features:
- Multiple Conv2D layers with ReLU activation
- MaxPooling layers to reduce spatial dimensions
- Flatten + Dense layers for classification

---

## Training Summary

- **Epochs:** 25
- **Optimizer:** Adam
- **Loss Function:** Sparse Categorical Crossentropy
- **EarlyStopping:** Enabled (patience = 5)
- **Validation Monitoring:** `val_accuracy`

### Performance

| Metric              | Value     |
|---------------------|-----------|
| Best Train Accuracy | 84.6%     |
| Best Val Accuracy   | 85.1%     |
| Final Val Accuracy  | 83.4%     |
| Best Val Epoch      | 21        |

> The model showed consistent improvement and did not suffer from overfitting. Validation performance closely tracked training accuracy.

---

