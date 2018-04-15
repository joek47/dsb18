# Deep Learning for Nuclei Detection
Stage 1 Data Science Bowl 2018, code based on [Mask RCNN](https://github.com/matterport/Mask_RCNN)

## Detected Nuclei
Here are some predictions on stage 1 test data:
![](https://i.imgur.com/uxx13ag.png)

## Hyperparameters That Improved Stage 1 Score
1. Larger min_dim and max_dim image size. There're significant improvements up to size 512. Here are the dimensions of most images in stage 1 train data.
  * (256, 256, 3) : 334
  * (1024, 1024, 3) : 16
  * (520, 696, 3) : 92
  * (360, 360, 3) : 91
  * (512, 640, 3) : 13
  * (256, 320, 3) : 112

2. Don't use Mini Mask or use bigger Mini Mask like (112,112) since there are high resolution images.
## Acknowledgements
CS6101 and Fast AI
