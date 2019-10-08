# Unsupervised Keypoint Learning <br/> for Guiding Class-Conditional Video Prediction
An official implementation of the paper "Unsupervised Keypoint Learning for Guiding Class-Conditional Video Prediction", NeurIPS 2019

<p align="left">
  <img src='img/model_overview.png' width="860" title="Overview">
</p>


## Requirements
- [PyTorch](https://github.com/pytorch/pytorch) 1.0
- [torchfile](https://github.com/bshillingford/python-torchfile)



## Datasets

[Penn_action](https://github.com/pytorch/pytorch)

1. split


## Train

#### 1. Train the keypoints detector & image translator
```
python train_kd_it.py configs/penn.yaml
```

#### 2. Make pseudo-keypoints labels
```
python make_labels.py configs/penn.yaml
```

#### 3. Train the motion generator
```
python train_mogen.py configs/penn.yaml
```


## Test
```
python test.py configs/penn.yaml
```

Download pretrained model
1. [Keypoints Detector & Image Translator](https://github.com/pytorch/pytorch)
2. [Motion Generator](https://github.com/pytorch/pytorch)


## Results
%![Penn action](images/results_flowers.jpg)
%![UvA-Nemo](images/results_birds.jpg)
%![MGIF](images/results_birds.jpg)



## Citation
Please cite our paper when you use this code.
```
@inproceedings{yunji_neurips_2019,
  title={Unsupervised Keypoint Learning for Guiding Class-Conditional Video Prediction},
  author={Kim, Yunji and Nam, Seonghyeon and Cho, In and Kim, Seon Joo},
  booktitle={Advances in Neural Information Processing Systems (NeurIPS)},
  year={2019}
}
```
