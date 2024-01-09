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

## Skeleton Structure



## Results on Human3.6m dataset

<table>
  <tr>
    <td><img src="lab_cv/best_model_h36m/directions_1_10.gif" width="320" height="240"><br />directions</td>
    <td><img src="lab_cv/best_model_h36m/discussion_1_10.gif" width="320" height="240"><br />discussion</td>
    <td><img src="lab_cv/best_model_h36m/eating_1_10.gif" width="320" height="240"><br />eating</td>
  </tr>
    <tr>
        <td><img src="lab_cv/best_model_h36m/greeting_1_10.gif" width="320" height="240"><br />greeting</td>
        <td><img src="lab_cv/best_model_h36m/phoning_1_10.gif" width="320" height="240"><br />phoning</td>
        <td><img src="lab_cv/best_model_h36m/posing_1_10.gif" width="320" height="240"><br />posing</td>
    </tr>
    <tr>
        <td><img src="lab_cv/best_model_h36m/purchases_1_10.gif" width="320" height="240"><br />purchases</td>
        <td><img src="lab_cv/best_model_h36m/sitting_1_10.gif" width="320" height="240"><br />sitting</td>
        <td><img src="lab_cv/best_model_h36m/sittingdown_1_10.gif" width="320" height="240"><br />sittingdown</td>
    </tr>
    <tr>
        <td><img src="lab_cv/best_model_h36m/smoking_1_10.gif" width="320" height="240"><br />smoking</td>
        <td><img src="lab_cv/best_model_h36m/takingphoto_1_10.gif" width="320" height="240"><br />takingphoto</td>
        <td><img src="lab_cv/best_model_h36m/waiting_1_10.gif" width="320" height="240"><br />waiting</td>
    </tr>
    <tr>
        <td><img src="lab_cv/best_model_h36m/walking_1_10.gif" width="320" height="240"><br />walking</td>
        <td><img src="lab_cv/best_model_h36m/walkingdog_1_10.gif" width="320" height="240"><br />walkingdog</td>
        <td><img src="lab_cv/best_model_h36m/walkingtogether_1_10.gif" width="320" height="240"><br />walkingtogether</td>
    </tr>
</table>


## Results on custom dataset
---
