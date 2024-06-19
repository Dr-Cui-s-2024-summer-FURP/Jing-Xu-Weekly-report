## Introduction and Installation for PyTorch

### Introduction

PyTorch is an open-source deep learning framework developed by Facebook's AI Research team. It provides a flexible and efficient tool for building and training deep learning models. PyTorch is well-known for its dynamic computation graph and powerful GPU acceleration, making it an ideal choice for research and development of deep learning applications.

Key features of PyTorch include:

- **Dynamic Computation Graph**: Unlike TensorFlow's static computation graph, PyTorch uses a dynamic computation graph, which means the graph is built at runtime. This makes the code easier to debug and more flexible.
- **Powerful GPU Support**: PyTorch seamlessly leverages NVIDIA's CUDA library to accelerate computations, thus speeding up the training of deep learning models.
- **Rich Libraries and Tools**: PyTorch offers many pre-trained models, data processing tools, and other useful libraries, making it easier to build and train models.

### Installation

Before installing PyTorch, ensure the system has the following software installed:
- Python 3.6 or higher
- pip (Python package manager)

Here are the steps to install PyTorch:

#### Installing PyTorch with Conda 
(I use conda to install, you can use pip or just like me, making sure you have install Anaconda)

1. **Create a new Conda environment** (optional)：

    ```bash
    conda create -n pytorch_env python=3.11
    conda activate pytorch_env
    ```
2. **Choose the appropriate installation command for environment [PyTorch website](https://pytorch.org/get-started/locally/)**:

    If the computer has NVIDIA GPU and want to take advantage of CUDA acceleration, select the PyTorch version with CUDA support.
else choose the CPU version.

3. **Install PyTorch**：

    just copy from PyTorch website to terminal, like
    ```
    conda install pytorch torchvision torchaudio pytorch-cuda=11.8 -c pytorch -c nvidia
    ```

### Verify Installation

After installation, verify by runnning the following command：

```python
import torch
torch.cuda.is_available()
```

if PyTorch is installed successfully, it will return True

