---
title: Lab in Computer Vision
subtitle: Human Pose Forecasting
# type: project
summary: • Developed a human pose prediction model composed of convolutional layers and Squeeze-and-Excitation blocks; reduced the Mean Per Joint Position Error (MPJPE) by 2.9% over the baseline transformer model
date: '2023-10-31T00:00:00Z'

url_code: 'https://github.com/AlekseiZhuravlev/MotionMixerConv/'
url_pdf: 'https://drive.google.com/file/d/1uFtFNbG0R6z7cEVWbDfxI2-yMyg_wJ5K/view?usp=sharing'
slides: ""

image:
  preview_only: true


# Page settings
show_title: false

show_date: false
reading_time: false
share: false
profile: false
commentable: true
editable: false
pager: false
show_related: false
show_breadcrumb: false

header:
  navbar:
    enable: false
---


## Abstract

In this work we address the problem of 3D human pose forecasting. Given a pose representation, our model, Convolutional Mixer, first applies the convolution in temporal dimension, learning the dependency between the target joint position at previous and future time frames. Then, it performs convolution in pose dimension to assess the relation between adjacent joints. We perform experiments on Human3.6m dataset and evaluate the importance of each parameter of our model.  We also evaluate it on the custom dataset recorded in the AIS lab. Finally, we extend it to perform predictions in an autoregressive fashion, which allows us to perform inference over long time intervals. Our results show that the model performs well on various motion sequences, and generalizes to novel datasets and long predictions.


## Method

## Results on Human3.6m dataset

## Results on custom dataset
---
