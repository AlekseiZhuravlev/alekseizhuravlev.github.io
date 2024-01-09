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

![Model architecture](visualization/Model_architecture.png)



## Results on Human3.6m dataset: 

### 10 seed frames + 10 frames prediction

<table>
  <tr>
    <td><img src="visualization/best_model_h36m/directions_1_10.gif" width="320" height="240"><br />directions</td>
    <td><img src="visualization/best_model_h36m/discussion_1_10.gif" width="320" height="240"><br />discussion</td>
  </tr>
    <tr>
        <td><img src="visualization/best_model_h36m/smoking_1_10.gif" width="320" height="240"><br />smoking</td>
        <td><img src="visualization/best_model_h36m/waiting_1_10.gif" width="320" height="240"><br />waiting</td>
    </tr>
    <tr>
        <td><img src="visualization/best_model_h36m/walking_1_10.gif" width="320" height="240"><br />walking</td>
        <td><img src="visualization/best_model_h36m/walkingtogether_1_10.gif" width="320" height="240"><br />walkingtogether</td>
    </tr>
</table>

### Autoregressive: 10 seed frames + 25 frames prediction

<table>
  <tr>
    <td><img src="visualization/best_model_h36m_autoregressive/directions_1_10.gif" width="320" height="240"><br />directions</td>
    <td><img src="visualization/best_model_h36m_autoregressive/discussion_1_10.gif" width="320" height="240"><br />discussion</td>
  </tr>
    <tr>
        <td><img src="visualization/best_model_h36m_autoregressive/smoking_1_10.gif" width="320" height="240"><br />smoking</td>
        <td><img src="visualization/best_model_h36m_autoregressive/waiting_1_10.gif" width="320" height="240"><br />waiting</td>
    </tr>
    <tr>
        <td><img src="visualization/best_model_h36m_autoregressive/walking_1_10.gif" width="320" height="240"><br />walking</td>
        <td><img src="visualization/best_model_h36m_autoregressive/walkingtogether_1_10.gif" width="320" height="240"><br />walkingtogether</td>
    </tr>
</table>


## Results on custom dataset:

### Autoregressive: 10 seed frames + 25 frames prediction

<table>
  <tr>
    <td><img src="visualization/best_model_ais_autoregressive/2021-08-04-singlePerson_000_20_10.gif" width="320" height="240"><br />singlePerson_000</td>
    <td><img src="visualization/best_model_ais_autoregressive/2021-08-04-singlePerson_001_20_10.gif" width="320" height="240"><br />singlePerson_001</td>
    </tr>
    <tr>
        <td><img src="visualization/best_model_ais_autoregressive/2022-05-26_2persons_001_30_10.gif" width="320" height="240"><br />2persons_001</td>
        <td><img src="visualization/best_model_ais_autoregressive/2022-05-26_2persons_002_30_10.gif" width="320" height="240"><br />2persons_002</td>
    </tr>
</table>

---
