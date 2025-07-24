# 🧠 Hindi Digit Classification using CNN and Data Augmentation

This project focuses on classifying handwritten **Devanagari (Hindi) digits** (०–९) using **Convolutional Neural Networks (CNNs)** with TensorFlow and Keras. By incorporating **image augmentation**, the model generalizes better, achieving near-perfect accuracy.

---

## 📊 Problem Statement

Recognizing handwritten digits is a classic computer vision task. While the Latin MNIST dataset is well known, Devanagari (Hindi) digits pose a unique challenge due to script complexity and shape similarity between characters.

This project aims to:
- Build a robust CNN model to classify Hindi digits (० to ९)
- Improve accuracy using real-time data augmentation
- Analyze misclassifications using confusion matrices

---

## 📦 Dataset

- **Source**: [Kaggle – Devanagari Characters and Numbers](https://www.kaggle.com/datasets/khushimehta1729/devanagri-characters-and-numbers)
- **Content**: Images of handwritten Devanagari characters and digits
- **Used Subset**: `digit_0` to `digit_9`
- **Image Format**: Grayscale, resized to 32×32
- **Total Samples**: 17,000+ digit images

---

## 🧠 Model Architecture

A simple yet effective CNN was used:

- **Input**: 32×32 grayscale images
- **Layers**:
  - `Conv2D(32)` + `MaxPooling`
  - `Conv2D(64)` + `MaxPooling`
  - `Flatten → Dense(128) → Dropout`
  - `Dense(10)` (Softmax Output)
- **Loss Function**: Sparse Categorical Crossentropy
- **Optimizer**: Adam
- **Evaluation Metric**: Accuracy

---

## 🔁 Data Augmentation

To increase model generalization and improve performance on visually similar digits (e.g. २ vs ३), the following augmentation techniques were applied:

- Rotation: ±10°
- Width/Height Shift: 10%
- Zoom: ±10%
- Shearing: 10%

---

## 📈 Results

| Configuration       | Test Accuracy | Test Loss |
|---------------------|---------------|-----------|
| 🔹 Without Augmentation | **99.32%**     | 0.017     |
| 🔸 With Augmentation    | **99.68%**     | 0.007     |

---

## ⚙️ Tools & Technologies

- Python 3.x
- TensorFlow & Keras
- OpenCV (for image loading/resizing)
- Matplotlib (visualization)
- Scikit-learn (confusion matrix, train-test split)
- Google Colab (execution environment)

---

## 🚀 Future Work

- Extend the model to full Devanagari characters (क–ज्ञ)
- Use transfer learning with pretrained CNNs like MobileNet or EfficientNet
- Build a web interface using **Gradio** or deploy in-browser with **TensorFlow.js**
- Apply advanced techniques like **ensemble learning** or **class weighting** for harder digits

---

## 🧑‍💻 Author

Made with ❤️ by 👤 [Anirudh Phophalia](https://github.com/AnirudhPhophalia)

---

## 📜 License

This project is licensed under the [MIT License](./LICENSE).

---

## ⭐ Acknowledgements

- Dataset by [Khushi Mehta](https://www.kaggle.com/khushimehta1729)
- CNN inspiration from classical MNIST digit classification
