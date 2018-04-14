# Deep Learning for Nuclei Detection
Code for Data Science Bowl 2018, based on [Mask RCNN](https://github.com/matterport/Mask_RCNN)

Model was chosen based on validation loss. At stage 1, model at epoch 56 achieved 0.456 mean average precision at different intersection over union (IoU):

![Val loss](https://i.imgur.com/9Y5Fyr1.png)

## Hyperparameters that Improve Stage 1 Score
1. Larger min_dim and max_dim image size. There're significant improvements up to size 512. Here are the dimensions of most images in stage 1 train data.
  * (256, 256, 3) : 334
  * (1024, 1024, 3) : 16
  * (520, 696, 3) : 92
  * (360, 360, 3) : 91
  * (512, 640, 3) : 13
  * (256, 320, 3) : 112

2. Don't use Mini Mask or use bigger Mini Mask like (112,112) since there are high resolution images.

## Detected Nuclei
Here are some predictions on stage 1 test data:
![](https://i.imgur.com/uxx13ag.png)

## Possible improvements
Data augmentation and morphological mask processing can be used to improve the results
