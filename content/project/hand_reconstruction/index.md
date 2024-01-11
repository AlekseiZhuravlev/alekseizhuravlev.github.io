---
title: Implicit hand reconstruction
# type: project
summary: • Developed a NeRF-based 3D reconstruction of the human hand based on Interhand2.6m dataset; Introduced perceptual loss (LPIPS) to improve PSNR score by 14% over MSE-only loss

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

This work addresses the problem of reconstructing an animatable avatar of a human hand from a collection of images of a user performing a sequence of gestures. Our model can capture accurate hand shape and appearance and generalize to various hand subjects. 
For a 3D point, we can apply two types of warping: zero-pose canonical space and UV space. The encoded coordinates are then passed to a NeRF which outputs the expected color and density. We demonstrate that our model can accurately reconstruct a dynamic hand from monocular or multi-view sequences, achieving high visual quality on Interhand2.6m dataset.
</div>


## Method

<!-- <table>
  <tr>
    <td><img src="Architecture_hypernerf.png"></td>
    <td><img src="Architecture_livehand.png"></td>
  </tr>
</table> -->

![Model architecture](Architecture_livehand.png "Architecture of LiveHand, reimplemented from scratch")

- Warping of 3D points to zero pose canonical space - adapted the approach of HumanNeRF to human hand setting instead of full body
- Warping of 3D points to UV space (texture coordinates + distance to the mesh), based on LiveHand - developed from scratch without using C++ CUDA kernels
- Introduced perceptual loss (LPIPS) to enhance the visual quality; improved PSNR score by 14% over MSE-only loss



## Results

<center>
<table>
  <tr>
    <td><img src="cam400293.gif" width="320" height="240"><br /></td>
    <td><img src="cam400296.gif" width="320" height="240"><br /></td>
  </tr>
</table>

Single view multi-pose sequence

![Reconstructed avatar](multi_pose.png "Reconstructed avatar in multiple poses from different views")
</center>

## References

1. LiveHand: Real-time and Photorealistic Neural Hand Rendering. arXiv preprint arXiv:2302.07672
2. Neuman: Neural human radiance field from a single video. In European Conference on Computer Vision, pp. 402-418. Cham: Springer Nature Switzerland, 2022
