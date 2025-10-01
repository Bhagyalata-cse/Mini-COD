# Mini-COD      ![Coming soon](https://img.shields.io/badge/Coming%20soon-red)


A Lightweight Model for Camouflaged Object Detection
> **Authors:**
> > [*Bhagyalata Modak*]([https://orcid.org/0009-0009-4822-6408]),
> > Wang...


## 1. Preface
- This repository provides code for "_**A**_"

### 2.1. Introduction
### 2.2. Framework Overview

### 2.3. Quantitative Results


## 3. Proposed Baseline

### 3.1. Training/Testing
The training and testing experiments are conducted using [PyTorch](https://github.com/pytorch/pytorch) with one NVIDIA GeForce RTX 4090 GPU with 24 GB memory.
## Prerequisites
Install Prerequisites with the following command:
```bash
conda create -n MiniCOD python = 3.10
conda install pytorch==2.5.1 torchvision==0.20.1 cudatoolkit=12.1 -c pytorch
pip install -r requirements.txt
```


### 2. Prepare data

We use data from publicly available datasets:
+ downloading testing dataset and move it into `./Dataset/TestDataset/`, 
    which can be found in [Google Drive](https://drive.google.com/file/d/1SLRB5Wg1Hdy7CQ74s3mTQ3ChhjFRSFdZ/view?usp=sharing) or [Baidu Drive](https://pan.baidu.com/s/1F3tVEWYzKYp5NBv3cjiaAg) (extraction code: fapn). 

+ downloading training/validation dataset and move it into `./Dataset/TrainValDataset/`, 
    which can be found in [Google Drive](https://drive.google.com/file/d/1Kifp7I0n9dlWKXXNIbN7kgyokoRY4Yz7/view?usp=sharing) or [Baidu Drive](https://pan.baidu.com/s/1uyQz0b_r_5yCee0orSw7EA) (extraction code: fapn).

### 3. Train

To train FSNet with costumed path:

```bash
python MyTrain_Val.py --save_path './train_path/MiniCOD/check/'
```
### 4. Test

To test with trained model:

```bash
python MyTesting.py --pth_path './train_path/MiniCOD/check/Net_epoch_best.pth'
```

downloading our weights and move it into `./train_path/MiniCOD/check/`, 
    which can be found from [Google Drive](https://drive.google.com/file/d/1Bgi8MThe1eEE9fYyaHuLHacO1Cs_e9Ta/view?usp=share_link).
    
 You can also download prediction maps from [Google Drive](https://drive.google.com/file/d/1kT9l9NrwWCffP4EQ7ITBd834389xY8iV/view?usp=share_link).


### 4. Evaluation 

We use public one-key evaluation, which is written in MATLAB code ([link](https://drive.google.com/file/d/1_h4_CjD5GKEf7B1MRuzye97H0MXf2GE9/view?usp=sharing)). 
Please follow this the instructions in `./eval/main.m` and just run it to generate the evaluation results in `./res/`.


## Citation

