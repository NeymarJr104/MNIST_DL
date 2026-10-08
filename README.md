# MNIST Digit Classification Using Deep Learning

A deep learning project that uses **TensorFlow** to classify handwritten digits from the **MNIST dataset**. The project implements a fully connected neural network from scratch using TensorFlow operations.

## 📌 Project Overview

The model takes a handwritten digit image of size **28 × 28 pixels**, converts it into a 784-dimensional input vector, and predicts which digit it represents from **0 to 9**.

### Workflow

```text
MNIST Image (28 × 28)
        ↓
Flatten Image
        ↓
784 Input Features
        ↓
Hidden Layer 1 (128 neurons)
        ↓
Sigmoid Activation
        ↓
Hidden Layer 2 (256 neurons)
        ↓
Sigmoid Activation
        ↓
Output Layer (10 classes)
        ↓
Softmax
        ↓
Predicted Digit (0–9)
```

## ✨ Features

- Handwritten digit classification
- MNIST dataset using TensorFlow/Keras
- Image normalization
- Custom neural network implementation
- Two hidden layers
- Sigmoid activation functions
- Softmax output for 10 digit classes
- Cross-entropy loss
- Stochastic Gradient Descent (SGD)
- Mini-batch training
- Model accuracy evaluation
- Visualization of test images and predictions

## 🛠️ Technologies Used

- **Python**
- **TensorFlow**
- **NumPy**
- **Matplotlib**

## 🧠 Model Architecture

| Layer | Configuration |
|---|---|
| Input | 784 features |
| Hidden Layer 1 | 128 neurons |
| Activation | Sigmoid |
| Hidden Layer 2 | 256 neurons |
| Activation | Sigmoid |
| Output Layer | 10 neurons |
| Output Activation | Softmax |
| Optimizer | SGD |
| Learning Rate | 0.001 |
| Batch Size | 256 |
| Training Steps | 3000 |

## 📊 Dataset

The project uses the **MNIST handwritten digit dataset** provided through `tensorflow.keras.datasets`.

Each image:

- Size: **28 × 28 pixels**
- Input features after flattening: **784**
- Number of classes: **10**
- Classes: **0–9**

Pixel values are normalized from the original `0–255` range to approximately `0–1`:

```python
x_train, x_test = x_train / 255., x_test / 255.
```

## ⚙️ Training

The dataset is converted into a TensorFlow data pipeline with:

- Shuffling
- Batching
- Repeating
- Prefetching

The model is trained using **Stochastic Gradient Descent (SGD)** and gradients are calculated using TensorFlow's `GradientTape`.

```python
optimizer = tf.optimizers.SGD(learning_rate)
```

## 📈 Evaluation

After training, the model predicts the classes of the MNIST test dataset and calculates the classification accuracy.

The notebook also displays five test images along with the model's predicted digit.

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
cd YOUR_REPOSITORY
```

### 2. Install dependencies

```bash
pip install tensorflow numpy matplotlib
```

### 3. Open the notebook

Open:

```text
Mnist_DL.ipynb
```

using **Jupyter Notebook**, **JupyterLab**, or **VS Code**.

### 4. Run all cells

Execute the cells sequentially to:

1. Load the MNIST dataset
2. Preprocess the images
3. Create the neural network
4. Train the model
5. Evaluate test accuracy
6. Display predictions

## 📁 Project Structure

```text
MNIST-DL/
│
├── Mnist_DL.ipynb
└── README.md
```

## 🔮 Future Improvements

The current implementation can be improved by:

- Replacing Sigmoid with **ReLU** activation
- Using **Adam optimizer**
- Using Xavier/Glorot weight initialization
- Adding validation data
- Adding training/validation accuracy graphs
- Increasing model robustness
- Implementing a **Convolutional Neural Network (CNN)** for better image classification performance

## 🎯 Learning Outcomes

This project demonstrates:

- Fundamentals of neural networks
- Forward propagation
- Backpropagation
- Gradient-based optimization
- Loss functions
- Classification accuracy
- TensorFlow `GradientTape`
- MNIST image preprocessing
- Basic deep learning workflow

## 👨‍💻 Author

**Aryan Vinod Mane**

Computer Engineering Student

GitHub: [NeymarJr104](https://github.com/NeymarJr104)
