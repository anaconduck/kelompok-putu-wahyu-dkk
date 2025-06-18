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

Set the desired dataset location in the [tools/dataloaders.py](/tools/dataloaders.py) (L9-10):
```python
data_route = {'cifar': '/path/to/cifar',
              'imagenet': '/path/to/imagenet'}
```

## Cara Run

- ResNet-32 on CIFAR: 
```sh
python iterate.py --dataset cifar --model resnet32_cifar --pruner rd --worst_case_curve --calib_size 1024
```
- ResNet-50 on ImageNet:
```sh
python iterate.py --dataset imagenet --model resnet50 --pruner rd --worst_case_curve --calib_size 256
```


# Referensi

```
@InProceedings{Xu_2023_ICCV,
    author    = {Xu, Kaixin and Wang, Zhe and Geng, Xue and Wu, Min and Li, Xiaoli and Lin, Weisi},
    title     = {Efficient Joint Optimization of Layer-Adaptive Weight Pruning in Deep Neural Networks},
    booktitle = {Proceedings of the IEEE/CVF International Conference on Computer Vision (ICCV)},
    month     = {October},
    year      = {2023},
    pages     = {17447-17457}
}
```
