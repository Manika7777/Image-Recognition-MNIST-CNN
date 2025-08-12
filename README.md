# Image-Recognition-MNIST-CNN

A Convolutional Neural Network (CNN) model for handwritten digit recognition using the MNIST dataset.  
This project was developed as part of the **Vision AI in 5 Days Bootcamp** to demonstrate skills in computer vision, deep learning, and model evaluation.

---

## 📌 Project Overview
The goal of this project is to build, train, and evaluate a CNN that can accurately recognize handwritten digits (0–9) from the MNIST dataset.  
The model is trained using TensorFlow/Keras and evaluated using accuracy, loss curves, confusion matrix, and sample predictions.

---

## 📂 Dataset
- **Source:** [MNIST dataset](http://yann.lecun.com/exdb/mnist/) (available in Keras)
- **Size:** 70,000 images (60,000 training, 10,000 test)
- **Image size:** 28×28 pixels, grayscale
- **Classes:** Digits 0–9

---

## 🛠 Preprocessing
- Reshape images to `(28, 28, 1)` for CNN input
- Normalize pixel values to `[0, 1]`
- One-hot encode labels
- Applied **ImageDataGenerator** for augmentation:
  - Rotation
  - Width & height shift
  - Zoom

---

## 🧠 Model Architecture

The CNN model for MNIST digit recognition consists of the following layers:

1. **Conv2D** (32 filters, 3×3, ReLU activation) + **BatchNormalization** + **MaxPooling2D**
2. **Conv2D** (64 filters, 3×3, ReLU activation) + **BatchNormalization** + **MaxPooling2D**
3. **Conv2D** (128 filters, 3×3, ReLU activation) + **BatchNormalization**
4. **Flatten** + **Dropout** (rate = 0.5)
5. **Dense** (128 units, ReLU activation) + **BatchNormalization**
6. **Dense** (10 units, Softmax activation) — output layer for 10 digit classes

**Compilation Settings:**
- **Optimizer:** Adam
- **Loss Function:** Categorical Crossentropy
- **Evaluation Metric:** Accuracy

## 📊 Results
- **Test Accuracy:** ~99%

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/Manika7777/Image-Recognition-MNIST-CNN.git
   cd Image-Recognition-MNIST-CNN
2.Install dependencies:
   ```pip install -r requirements.txt
## ✨ Author
**Manika Sarkar**  
📧 Email: your.email@example.com  
🔗 [LinkedIn](https://www.linkedin.com/in/manika-sarkar-264426295/) | [GitHub](https://github.com/Manika7777)
