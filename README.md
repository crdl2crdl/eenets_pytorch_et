# EENets_PyTorch
This repository contains PyTorch implementation of EENets: Early Exit Convolutional Neural Network. ([paper](https://drive.google.com/file/d/1tnLPd2Jiqm3WdVYKYAMv6dF_XpjS9vfu/view) and [the slides](https://drive.google.com/open?id=1IJKm0XygD2yPA1jCSgNdAhApGWM76lFf))

## Getting Started

The codes are developed with python35 environment on Windows 10. The development environment consists of 
 * i7-6700HQ CPU processor with 16GB RAM 
 * NVIDIA GeForce GTX 950M 4GB

### Prerequisites

Pytorch environment can be installed via [the website](https://pytorch.org/get-started/locally/).

### Datasets

The models can be trained and tested with MNIST dataset.
training.pt and test.pt should be under "./data/mnist" the folder like:
```
./data/mnist
   + training.pt
   + test.pt
```

Note that MNIST dataset cannot be used in the original ResNet models because their architecture is designed for 32x32 dimensial inputs.
Similarly, ResNet based EENet models do not support MNIST dataset. 

### Training

The main.py includes command line arguments, to see all of them:
```
$ python main.py --help
usage: main.py [-h] [--batch-size N] [--test-batch-size N] [--epochs N]
               [--lr LR] [--momentum M] [--no-cuda] [--seed S]
               [--log-interval N] [--save-model] [--filters N]

PyTorch MNIST Example

optional arguments:
  -h, --help           show this help message and exit
  --batch-size N       input batch size for training (default: 32)
  --test-batch-size N  input batch size for testing (default: 1)
  --epochs N           number of epochs to train (default: 10)
  --lr LR              learning rate (default: 0.01)
  --momentum M         SGD momentum (default: 0.5)
  --no-cuda            disables CUDA training
  --seed S             random seed (default: 1)
  --log-interval N     how many batches to wait before logging training status
  --save-model         For Saving the current Model
  --filters N          initial filter number of the model
```

Example training command:
```
$ python main.py --filters 2 --epochs 30
```

## The Code Contents

ResNet based EENet model classes are implemented in the "EENets.py" file. 
The "main.py" creates and initializes a model by calling EENet methods. Training and testing details are also written in this file.
The "utils.py" and "flops_counter.py" are helping codes for AverageMeter and counting the number of floating point operations, respectively. "flops_counter.py" are taken from [this repo](https://github.com/sovrasov/flops-counter.pytorch).

## Authors

* **Edanur Demir** - *EENets: Early Exit Convolutional Neural Networks* - [eksuas](https://github.com/eksuas)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

