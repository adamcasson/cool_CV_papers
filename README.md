# Cool Computer Vision Papers
List of computer vision papers I've come across that are cool, interesting, innovative, or all of the above

Repo start date: June 27, 2017

This collection will not be especially retroactive w.r.t. papers I’ve already read unless I pick them up again to study. Nor is it strictly a reflection of the latest and greatest state-of-the-art approaches for CV problems. It’s mostly a working collection of papers that have served a purpose for my research or simply piqued my interest since the start date of this repo.

## Table of Contents
* [Visual Question Answering](#visual-question-answering)
* [Pose Estimation](#pose-estimation)
* [Object Detection](#object-detection)
* [Relational Reasoning](#relational-reasoning)
* [3D Computer Vision](#3d-computer-vision)

## Papers

### Visual Question Answering
* Bottom-Up and Top-Down for Image Captioning and Visual Question Answering [[arXiv](https://arxiv.org/abs/1707.07998v2)][[pdf](https://arxiv.org/pdf/1707.07998v2.pdf)][[code](https://github.com/peteanderson80/bottom-up-attention)]
  * SotA for VQA 2.0 (as of August 20, 2017)

* Show, Ask, Attend, and Answer: A Strong Baseline For Visual Question Answering [[arXiv](https://arxiv.org/abs/1704.03162)][[pdf](https://arxiv.org/pdf/1704.03162.pdf)][[unofficial code](https://github.com/adamcasson/show_ask_attend_answer)]
  * Not state-of-the-art but they offer a simple architecture utilizing the popular stacked attention approach. No complex multi-modal fusion schemes just simple feature concatenation. Approaches SotA without training on additional data (e.g. Visual Genome).
  * Use of res5c ResNet features is needed for the SAN but requires a considerably large amount of data compared to using no attention mechanism with pool5 features. In other words, each image, when fed into the trainable portion of the network, is represented with a 14x14x2048 tensor rather than a 2048-D vector.
  * Will attempt to implement this in Keras soon.

* MUTAN: Multimodal Tucker Fusion for Visual Question Answering [[arXiv](https://arxiv.org/abs/1705.06676)][[pdf](https://arxiv.org/pdf/1705.06676.pdf)][[code](https://github.com/Cadene/vqa.pytorch)]
  * This seems to be the state-of-the-art VQA approach right now on VQAv1 dataset. Now that the VQAv2 dataset is out there’s a good chance a new SotA approach will surface from that corresponding challenge/workshop at CVPR.
  * The approach here is essentially the same as the previous SotA called [Multimodal Compact Bilinear Pooling (MCB)](https://arxiv.org/abs/1606.01847)
  * The big innovation is their multi-modal fusion scheme. The simplest approach to combine image and question features is simply concatenating the feature vectors. This seems like a naive and weak point in the common VQA approach so it’s appropriate that we see people trying to create more meaningful fusion schemes.

### Pose Estimation
* Realtime Multi-Person 2D Pose Estimation using Part Affinity Fields [[arXiv](https://arxiv.org/abs/1611.08050)][[pdf](https://arxiv.org/pdf/1611.08050.pdf)][[code](https://github.com/ZheC/Realtime_Multi-Person_Pose_Estimation)]
  * Claims to be the first realtime system for multi-person 2D pose detection.
  * The overall method can be broken into 3 steps: Simultaneous prediction of confidence maps of parts and affinity fields for parts, bipartite matching, and parsing all the parts.
  * The authors propose a novel non-parametric feature representation called parts affinity fields. These are 2D vectors at each pixel between the key points that make up a limb. This is useful because it encodes location and orientation of limbs.
  * The overall approach is bottom-up as opposed to the normal top-down approach (run a person detector, detect limbs of each person, etc.). This greatly improves efficiency and runtime is barely affected as the number of people in the image increase.

### Object Detection
* You Only Look Once: Unified, Real-Time Object Detection [[arXiv](https://arxiv.org/abs/1506.02640)][[pdf](https://arxiv.org/pdf/1506.02640.pdf)][[code](https://pjreddie.com/darknet/yolo/)]
  * Notes coming soon

### Relational Reasoning
* A Simple Neural Network Module for Relational Reasoning [[arXiv](https://arxiv.org/abs/1706.01427)][[pdf](https://arxiv.org/pdf/1706.01427.pdf)][[unofficial code](https://github.com/kimhc6028/relational-networks)]
  * Notes coming soon

### 3D Computer Vision
* Multi-view Supervision for Single-view Reconstruction via Differentiable Ray Consistency [[arXiv](https://arxiv.org/abs/1704.06254)][[pdf](https://arxiv.org/pdf/1704.06254.pdf)][[code](https://github.com/shubhtuls/drc)]
  * Notes coming soon