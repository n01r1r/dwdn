# Deep Wiener Deconvolution: Wiener Meets Deep Learning for Image Deblurring

This repository is the PyTorch implementation of the paper:

**Deep Wiener Deconvolution: Wiener Meets Deep Learning for Image Deblurring**

Jiangxin Dong, Stefan Roth, and Bernt Schiele

To appear at NeurIPS 2020 (**Oral Presentation**)

[[Paper]](https://proceedings.neurips.cc/paper/2020/file/0b8aff0438617c055eb55f0ba5d226fa-Paper.pdf)/[[Supplemental]](https://proceedings.neurips.cc/paper/2020/file/0b8aff0438617c055eb55f0ba5d226fa-Supplemental.pdf)

## Requirements

Compatible with Python 3

Main requirements: PyTorch 1.1.0 or 1.5.0 or 0.4.1 are tested

To install requirements:

```setup
pip install torch==1.1.0 torchvision==0.3.0
pip install -r requirements.txt
```

## Evaluation

To evaluate the deep Wiener deconvolution network on test examples, run:

```eval
python main.py
```

## Pre-trained Model

./model/model.pt

## Bibtex

Please cite our paper if you use our source code.

```
@article{dong2020deep,
  title={Deep Wiener Deconvolution: Wiener Meets Deep Learning for Image Deblurring},
  author={Dong, Jiangxin and Roth, Stefan and Schiele, Bernt},
  journal={Advances in Neural Information Processing Systems},
  volume={33},
  year={2020}
}
```