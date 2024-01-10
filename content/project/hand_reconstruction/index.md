---
title: Implicit hand reconstruction
# type: project
summary: • Developed a NeRF-based 3D reconstruction of the human hand based on Interhand2.6m dataset; Introduced perceptual loss (LPIPS) to enhance the visual quality

date: '2023-12-31T00:00:00Z'

links:
- name: Project Page
  url: 'https://alekseizhuravlev.github.io/project/hand_reconstruction/'
- name: Code (soon)
  url: ''


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

<!-- <div align="center">
  <b>Aleksei Zhuravlev, [Dr. Danda Pani Paudel](https://people.ee.ethz.ch/~paudeld/), [Dr. Thomas Probst](https://probstt.bitbucket.io/)</b><br>
  <b><i>University of Bonn</i></b>
</div> -->

<!-- <p style="text-align: center;"> -->
[Aleksei Zhuravlev](https://alekseizhuravlev.github.io/), [Dr. Danda Pani Paudel](https://people.ee.ethz.ch/~paudeld/) and [Dr. Thomas Probst](https://probstt.bitbucket.io/)
<!-- </p> -->


<table>
  <tr>
    <td><img src="featured.gif" width="320" height="240"><br /></td>
    <td><img src="cam400280.gif" width="320" height="240"><br /></td>
    </tr>
</table>


## Abstract

<div style="text-align: justify"> 
In this work we address the problem of 3D human pose forecasting. Given a pose representation, our model, Convolutional Mixer, first applies the convolution in temporal dimension, learning the dependency between the target joint position at previous and future time frames. Then, it performs convolution in pose dimension to assess the relation between adjacent joints. We perform experiments on Human3.6m dataset and evaluate the importance of each parameter of our model.  We also evaluate it on the custom dataset recorded in the AIS lab. Finally, we extend it to perform predictions in an autoregressive fashion, which allows us to perform inference over long time intervals. Our results show that the model performs well on various motion sequences, and generalizes to novel datasets and long predictions.
</div>


## Method


![Model architecture](visualization/Model_architecture.png)

- We build upon MotionMixer, which applied MLPs to an encoded pose vector. We replaced MLPs with convolutional layers and experimented with kernel sizes, number of layers, and ways to encode the pose vector
- Our model can work with different methods of human pose representation, such as axis-angle or coordinate-based formats. We consider both local motion with respect to pelvis joint as well as global. 
- We use 10 seed frames for prediction and output 10 subsequent frames. To generalize to longer sequences, we additionally consider autoregressive prediction with a sliding window for a total of 25 frames.
- We test our model on Human3.6m dataset and custom data captured by our tutor, which has a slightly different skeleton model

## Results
<table>
  <tr>
    <td><img src="cam400293.gif" width="320" height="240"><br /></td>
    <td><img src="cam400296.gif" width="320" height="240"><br /></td>
  </tr>
</table>

<img src="multi_pose.png" align="center">
---
