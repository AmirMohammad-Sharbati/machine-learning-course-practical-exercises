# Machine Learning Course Assignments

![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?logo=scikitlearn&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?logo=tensorflow&logoColor=white)

A collection of five practical assignments from a Machine Learning course, spanning classical ML, deep learning, computer vision, and NLP. Each assignment includes hands-on implementations, from-scratch algorithms, and real-world applications.

---

## 📚 Table of Contents

- [Repository Structure](#-repository-structure)
- [Assignments](#-assignments)
  - [1. Supervised Learning](#1-supervised-learning)
  - [2. Unsupervised Learning](#2-unsupervised-learning)
  - [3. Neural Networks & Optimization](#3-neural-networks--optimization)
  - [4. Computer Vision](#4-computer-vision)
  - [5. Natural Language Processing](#5-natural-language-processing)
- [Key Highlights](#-key-highlights)

---

## 📁 Repository Structure

```
ml-course-assignments/
│
├── 1-supervised-learning/
│   ├── titanic-random-forest/
│   │   ├── titanic.ipynb
│   │   └── titanic.csv
│   └── regression-and-perceptron/
│       ├── Regression_and_Perceptron.ipynb
│       └── skyfuel_final_model.pkl
│
├── 2-unsupervised-learning/
│   ├── kmeans-image-segmentation/
│   │   ├── K-Means.ipynb
│   │   ├── matryoshka.jpg
│   │   ├── shrek.jpg
│   │   ├── st.basils.jpg
│   │   └── expected-results/
│   ├── gmm-customer-segmentation/
│   │   ├── GMM.ipynb
│   │   ├── Mall_Customers.csv
│   │   ├── segmented_customers.csv
│   │   └── expected-results/
│   └── pca-image-compression/
│       ├── PCA.ipynb
│       └── image.jpg
│
├── 3-neural-networks/
│   └── Neural_Networks_and_Optimization.ipynb
│
├── 4-computer-vision/
│   ├── cnn-finetuning/
│   │   └── CNN_Finetuning.ipynb
│   └── cnn-from-scratch-and-nst/
│       ├── CNN_and_NST.ipynb
│       └── images/
│           ├── neural-transfer/
│           └── sample/
│
├── 5-nlp/
│   └── Word_Embeddings_and_FineTuning.ipynb
│
├── LICENSE
└── README.md
```

---

## 📖 Assignments

### 1. Supervised Learning

> **Topics:** Regression, Classification, Ensemble Learning (Random Forest)

| Notebook | Description |
|----------|-------------|
| **Titanic Survival Prediction** | End-to-end classification pipeline using **Random Forest** on the famous Titanic dataset. Includes data visualization, preprocessing, feature engineering, model training, and evaluation (confusion matrix, accuracy, precision, recall). |
| **Regression & Perceptron** | Two-part notebook: (1) **Polynomial Regression** on synthetic fuel consumption data to analyze overfitting/underfitting across different polynomial degrees, (2) **Perceptron from scratch** for binary classification on the Iris dataset. |

---

### 2. Unsupervised Learning

> **Topics:** Clustering (K-Means, GMM), Dimensionality Reduction (PCA)

| Notebook | Description |
|----------|-------------|
| **K-Means Image Segmentation** | Implementation of **K-Means from scratch** for color-based image segmentation. Uses the Elbow Method to find optimal K and visualizes segmented images. |
| **GMM Customer Segmentation** | Implementation of **Gaussian Mixture Models from scratch** using the EM algorithm. Segments customers based on demographics and behavior. Includes BIC-based model selection and 2D/3D cluster visualization. |
| **PCA Image Compression** | Implementation of **PCA from scratch** for image compression. Divides images into patches, projects them to lower dimensions, and reconstructs the compressed image. Also visualizes eigenpatches. |

---

### 3. Neural Networks & Optimization

> **Topics:** MLPs, Backpropagation, Optimizers (SGD, Momentum, Adam, AdamW), Regularization (L1/L2, Dropout), Batch Normalization

| Notebook | Description |
|----------|-------------|
| **Neural Networks & Optimization** | A comprehensive **MLP framework built from scratch** using NumPy. Implements Linear layers, ReLU, Tanh, Dropout, BatchNorm, and Softmax Cross-Entropy. Includes gradient checking, multiple optimizers, and extensive ablation studies comparing optimizers, regularization techniques, and batch normalization. |

---

### 4. Computer Vision

> **Topics:** CNNs, Transfer Learning, Fine-tuning, Neural Style Transfer (NST)

| Notebook | Description |
|----------|-------------|
| **CNN Fine-tuning** | Image classification on the **Flowers dataset** using **TensorFlow/Keras**. Builds a **VGG-style CNN from scratch** and **fine-tunes ResNet50** in stages. Compares approaches using accuracy, precision, recall, F1, and ROC/AUC. |
| **CNN from Scratch & Neural Style Transfer** | Two-part notebook: (1) a **convolutional layer from scratch** to understand convolution mechanics, (2) **Neural Style Transfer** with a pretrained VGG19 to apply artistic styles to images. |

---

### 5. Natural Language Processing

> **Topics:** Word Embeddings, TF-IDF, Word2Vec, GloVe, Transformers, BERT, PEFT (LoRA, DoRA)

| Notebook | Description |
|----------|-------------|
| **Word Embeddings & Fine-Tuning** | Two-part notebook: (1) **Word embeddings from scratch** including TF-IDF, CBOW, and Skip-Gram on the Harry Potter series, plus exploration of GloVe analogies, (2) **Parameter-efficient fine-tuning** comparing Full FT, LoRA, and DoRA on AG News. Analyzes weight geometry (ΔM, ΔD) during training. |

---

## ✨ Key Highlights

- **From-Scratch Implementations:** K-Means, GMM, PCA, Perceptron, MLP, Convolutional layers, TF-IDF, Word2Vec
- **Comprehensive Experiments:** Ablation studies on optimizers, regularization, and fine-tuning strategies
- **Real-World Applications:** Image segmentation, customer segmentation, image compression, style transfer, text classification
- **Modern Techniques:** Transfer learning with **TensorFlow/Keras and PyTorch**, parameter-efficient fine-tuning (LoRA, DoRA), and Neural Style Transfer
- **Thorough Evaluation:** Confusion matrices, ROC/AUC, BIC, log-likelihood, and weight geometry analysis

---

## 📝 License

This project is licensed under the [MIT License](LICENSE). Datasets used are publicly available and are subject to their respective licenses.

---

## 👨‍💻 Author

Developed by [**Amir Mohammad Sharbati**](https://github.com/AmirMohammad-Sharbati) as part of the Machine Learning course at Sharif University of Technology.