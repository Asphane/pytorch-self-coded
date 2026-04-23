# 🧠 PyTorch Self-Coded Projects

> A collection of self-coded deep learning projects using PyTorch, featuring artificial neural networks for image classification and machine learning tasks.

![PyTorch](https://img.shields.io/badge/PyTorch-2.0+-red?logo=pytorch&style=flat-square)
![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python&style=flat-square)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)
![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=flat-square)

---

## ✨ Highlights

- 🚀 **GPU-Optimized** - CUDA support for faster training
- 📊 **Custom DataLoaders** - Learn how to build PyTorch data pipelines
- 🎯 **Multiple Models** - MNIST, Fashion MNIST, and Cancer Classification
- 📈 **High Accuracy** - 80%+ accuracy on test datasets
- 💡 **Well-Documented** - Clean, commented code for learning

---

## 📂 Project Structure

```
pytorch-self-coded/
├── ann_mnist_pytorch.ipynb              # MNIST Classification (CPU)
├── ann_mnist_pytorch_gpu.ipynb          # MNIST Classification (GPU)
├── breast_cancer.ipynb                  # Binary Classification
├── Dataset_dataloader.ipynb             # Custom Data Pipeline Tutorial
└── requirements.txt                     # Dependencies
```

---

## 🎯 Projects Overview
```
| Project | Dataset | Architecture | Accuracy |
|---------|---------|--------------|----------|
| **MNIST (CPU)** | MNIST | 784→128→64→10 | ~97% |
| **MNIST (GPU)** | Fashion MNIST | 784→128→64→10 | ~80%+ |
| **Cancer Detection** | Breast Cancer | Multi-layer ANN | ~96% |
| **Data Pipeline** | Custom Dataset | Tutorial Series | - |
```
---

## 🛠️ Installation

### Prerequisites
- Python 3.8 or higher
- pip or conda
- (Optional) CUDA-capable GPU

### Quick Start


# Clone the repository
```bash
git clone https://github.com/Asphane/pytorch-self-coded.git
cd pytorch-self-coded
```
# Create virtual environment
```
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

# Install dependencies
```
pip install -r requirements.txt
```

---

## 📦 Requirements

```
torch>=2.0.0
torchvision
pandas>=1.0.0
numpy>=1.20.0
scikit-learn>=1.0.0
matplotlib>=3.5.0
kagglehub
```

---

## 🚀 Usage

### Open in Jupyter
```bash
jupyter notebook ann_mnist_pytorch_gpu.ipynb
```

### Open in VS Code
- Use VS Code's built-in Notebook extension
- Click "Run All" to execute all cells

### Basic Workflow
1. **Data Loading** - Fetch datasets using kagglehub
2. **Preprocessing** - Normalize and split data
3. **Model Creation** - Define neural network architecture
4. **Training** - Train with GPU acceleration
5. **Evaluation** - Calculate accuracy metrics

---

## 🧠 Model Architecture

### Standard ANN Configuration
```
Input Layer (784 neurons)
    ↓
Hidden Layer 1 (128 neurons + ReLU)
    ↓
Hidden Layer 2 (64 neurons + ReLU)
    ↓
Output Layer (10 neurons + Softmax)
```

### Training Configuration
- **Optimizer**: Adam
- **Loss Function**: CrossEntropyLoss
- **Learning Rate**: 0.001
- **Batch Size**: 32
- **Epochs**: 100

---

## 📊 Performance Metrics

| Model | Dataset | Train Accuracy | Test Accuracy | Training Time |
|-------|---------|---|---|---|
| Fashion MNIST (GPU) | Fashion MNIST | 89% | 80%+ | ~2-3 min |
| MNIST | MNIST | 98% | 97% | ~5 min |
| Breast Cancer | Cancer Dataset | 97% | 96% | <1 min |

---

## 🎓 What You'll Learn

✅ Custom PyTorch Dataset implementation  
✅ DataLoader for batch processing  
✅ GPU/CUDA acceleration  
✅ Neural network architecture design  
✅ Training loops and backpropagation  
✅ Model evaluation and metrics  
✅ Data visualization with Matplotlib  

---

## 🔧 Key Features

### ⚡ GPU Support
```python
device = torch.device('cuda' if torch.cuda.is_available() else 'cpu')
model = model.to(device)
```

### 📦 Custom Dataset Class
```python
class CustomDataset(Dataset):
    def __init__(self, features, labels):
        self.features = torch.tensor(features, dtype=torch.float32)
        self.labels = torch.tensor(labels, dtype=torch.long)
    
    def __len__(self):
        return len(self.features)
    
    def __getitem__(self, idx):
        return self.features[idx], self.labels[idx]
```

### 🎯 Automatic Dataset Download
```python
import kagglehub
path = kagglehub.dataset_download("zalando-research/fashionmnist")
```

---

## 📝 Example Usage

```python
# Import libraries
import torch
from torch.utils.data import DataLoader
```

# Load model
```
model = MyANN(num_features=784)
model = model.to(device)
```

# Training loop
```
for epoch in range(epochs):
    for features, labels in train_loader:
        features, labels = features.to(device), labels.to(device)
        
        outputs = model(features)
        loss = criterion(outputs, labels)
        
        optimizer.zero_grad()
        loss.backward()
        optimizer.step()
```

---

## 💡 Tips & Tricks

- 🎲 Use `torch.manual_seed(42)` for reproducibility
- 📊 Normalize pixel values to [0, 1] range for better convergence
- ⚡ Move data to GPU for faster training
- 📈 Use DataLoaders for efficient batch processing
- 🔍 Monitor loss and accuracy during training

---

## 🐛 Troubleshooting

**Issue: CUDA not available**
```bash
# Check CUDA availability
python -c "import torch; print(torch.cuda.is_available())"
```

**Issue: Module not found**
```bash
# Reinstall dependencies
pip install --upgrade -r requirements.txt
```

---

## 📚 Resources

- [PyTorch Official Docs](https://pytorch.org/docs/)
- [Fast AI Course](https://course.fast.ai/)
- [Deep Learning Book](http://www.deeplearningbook.org/)

---

## 👤 Author

**Bisakh Patra**

---

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

---

## ⭐ Show Your Support

If you found this helpful, please give it a star! Your support motivates further development.

```bash
git star Asphane/pytorch-self-coded
```

---

<div align="center">

**Made with ❤️ by Bisakh Patra**

⬆ Back to Top

</div>
```
