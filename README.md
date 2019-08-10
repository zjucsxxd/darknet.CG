# Darknet 

Darknet is an open source neural network framework written in C and CUDA. It is fast, easy to install, and supports CPU and GPU computation.

This repository is borrowed heavily from https://github.com/pjreddie/darknet and https://github.com/AlexeyAB/darknet

# new features
 - [shufflenetv2](https://arxiv.org/abs/1807.11164):
[channel_shuffle layer](https://github.com/gmayday1997/darknet.CG/blob/master/src/channel_shuffle.c) and 
[channel_slice layer](https://github.com/gmayday1997/darknet.CG/blob/master/src/channel_slice.c) are added in this repo.

![img1](https://user-images.githubusercontent.com/16068384/39479361-9f1345c0-4d97-11e8-8201-4a45ac4a6c7e.png)

- [yolov3 slimming](https://arxiv.org/abs/1708.06519):
[prune.cpp](https://github.com/gmayday1997/darknet.CG/blob/master/src/prune.cpp) is added.

![img2](https://user-images.githubusercontent.com/8370623/29604272-d56a73f4-879b-11e7-80ea-0702de6bd584.jpg)

## How to use

- shufflenev2: 
  for example basic unit
  
| ![basicunit](https://img3.doubanio.com/view/status/raw/public/e99ac6d308ca60e.jpg) | ![darknetcfg](https://img3.doubanio.com/view/status/raw/public/2928419c25e8e21.jpg) |
|---|---|

- yolov3 slimming 
```
  ./darknet prune ./cfg/yolov3.cfg ./cfg/yolov3.weights -rate 0.3
```
![img3](https://img1.doubanio.com/view/status/raw/public/0d1e2ae81cea1fc.jpg)

the pruned cfg/weights are saved as ./cfg/yolov3_prune.cfg / .cfg/yolov3_prune.weights
