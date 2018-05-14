# Deep Learning for Nuclei Detection
[Data Science Bowl 2018](https://www.kaggle.com/c/data-science-bowl-2018/)

Automate the process of identifying nuclei, which will allow for more efficient drug testing, shortening the 10 years it takes for each new drug to come to market.

## Detected Nuclei
Here are some predictions on stage 1 test data:
![](https://i.imgur.com/uxx13ag.png)

## Config
1. Larger min_dim and max_dim image size. There're significant improvements up to size 512. Here are the dimensions of most images in stage 1 train data.
  * (256, 256, 3) : 334
  * (1024, 1024, 3) : 16
  * (520, 696, 3) : 92
  * (360, 360, 3) : 91
  * (512, 640, 3) : 13
  * (256, 320, 3) : 112

2. Don't use Mini Mask or use bigger Mini Mask like (112,112) since there are high resolution images.

## Results
Leaderboard mAP - Stage 1 0.456, Stage 2 0.503

Based on [Mask RCNN](https://github.com/matterport/Mask_RCNN)
