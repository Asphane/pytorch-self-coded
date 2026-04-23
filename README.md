```markdown
# PyTorch Self-Coded Projects

A collection of self-coded deep learning projects using PyTorch, focusing on artificial neural networks (ANNs) for image classification and other machine learning tasks.

## 📁 Contents

- **ann_mnist_pytorch.ipynb** - ANN implementation for MNIST dataset (CPU)
- **ann_mnist_pytorch_gpu.ipynb** - ANN implementation for MNIST dataset (GPU-optimized)
- **breast_cancer.ipynb** - ANN for breast cancer classification
- **Dataset_dataloader.ipynb** - Custom Dataset and DataLoader implementations
- **requirements.txt** - Python dependencies

## 🚀 Features

- Custom PyTorch Dataset class implementation
- GPU support (CUDA)
- Fashion MNIST dataset integration via kagglehub
- Training pipeline with Adam optimizer
- Model evaluation and accuracy metrics
- Visualization of training data

## 📋 Requirements

- Python 3.8+
- PyTorch 2.0+
- pandas
- numpy
- scikit-learn
- matplotlib
- kagglehub

## 🔧 Installation

1. Clone the repository:
```bash
git clone https://github.com/Asphane/pytorch-self-coded.git
cd pytorch-self-coded
```

2. Create a virtual environment (optional but recommended):
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

## 🎯 Usage

Open any notebook in Jupyter or VS Code:

```bash
jupyter notebook ann_mnist_pytorch_gpu.ipynb
```

Or use VS Code's built-in notebook viewer.

## 📊 Model Architecture

- Input Layer: 784 neurons (28×28 images flattened)
- Hidden Layer 1: 128 neurons + ReLU
- Hidden Layer 2: 64 neurons + ReLU
- Output Layer: 10 neurons (10 classes)
- Optimizer: Adam
- Loss Function: CrossEntropyLoss

## 📈 Results

Trained on Fashion MNIST dataset for 100 epochs with ~80%+ accuracy on test set.

## 📝 License

MIT License

## ✨ Author

Bisakh Patra
```
