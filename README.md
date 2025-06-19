# Installation
1. Clone this repository
```sh
git clone https://github.com/anaconduck/kelompok-putu-wahyu-dkk.git
cd RD_PRUNE
```

2. Install NVIDIA-DALI for imagenet experiments:

- Please refer to [official installation guide](https://docs.nvidia.com/deeplearning/dali/user-guide/docs/installation.html)


# Experiments 

## Dataset Preparation

Atur lokasi dataset yang diinginkan dalam tools/dataloaders.py (Baris 9-10):
```python
data_route = {'cifar': '/path/to/cifar',
              'imagenet': '/path/to/imagenet'}
```

## Cara Run

- ResNet-18 on CIFAR: 
```sh
python iterate.py --dataset cifar --model resnet18 --pruner rd --worst_case_curve --calib_size 1024
```
- ResNet-50 on ImageNet:
```sh
python iterate.py --dataset imagenet --model resnet50 --pruner rd --worst_case_curve --calib_size 256
```
