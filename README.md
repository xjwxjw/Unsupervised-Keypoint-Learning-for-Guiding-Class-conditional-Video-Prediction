# Unsupervised Keypoint Learning for Guiding Class-conditional Video Prediction
An official Tensorflow implementation of the paper "Unsupervised Keypoint Learning for Guiding Class-conditional Video Prediction", NeurIPS 2019

![Model architecture](model_overview.jpg)



## Requirements
- [PyTorch](https://github.com/pytorch/pytorch) 1.0
- [torchfile](https://github.com/bshillingford/python-torchfile)



## Datasets

Download original versions
1. [Penn_action](https://github.com/pytorch/pytorch)
2. [UvA_Nemo](https://github.com/pytorch/pytorch)
3. [MGIF](https://github.com/pytorch/pytorch)

Download preprocessed versions
1. [Penn_action](https://github.com/pytorch/pytorch)
2. [UvA_Nemo](https://github.com/pytorch/pytorch)
3. [MGIF](https://github.com/pytorch/pytorch)



## Train

### 1. Train keypoints-detector and keypoints-guided-image-translator
```
python train_first.py
```


### 2. Make pseudo keypoints labels
```
python make_labels.py
```

Download pseudo-labels extracted from pretrained model
1. [Penn_action](https://github.com/pytorch/pytorch)
2. [UvA_Nemo](https://github.com/pytorch/pytorch)
3. [MGIF](https://github.com/pytorch/pytorch)

### 3. Train keypoints motion generator
```
python train_second.py
```


## Test
```
python test.py
```

Download pretrained model
1. [first](https://github.com/pytorch/pytorch)
2. [second](https://github.com/pytorch/pytorch)


## Results
%![Penn action](images/results_flowers.jpg)
%![UvA-Nemo](images/results_birds.jpg)
%![MGIF](images/results_birds.jpg)



## Citation
Please cite our paper when you use this code.
```
@inproceedings{yunji_neurips_2019,
  title={Unsupervised Keypoint Learning for Guiding Class-conditional Video Prediction},
  author={Kim, Yunji and Nam, Seonghyeon and Cho, In and Kim, Seon Joo},
  booktitle={Advances in Neural Information Processing Systems (NeurIPS)},
  year={2019}
}
```



## Contact
Please contact [kim_yunji@yonsei.ac.kr](kim_yunji@yonsei.ac.kr) if you have any question about this work.
