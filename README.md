# cool_CV_papers
List of computer vision papers I've come across that are cool, interesting, innovative, or all of the above

Repo start date: June 27, 2017

This collection will not be especially retroactive w.r.t. papers I’ve already read unless I pick them up again to study. Nor is it strictly a reflection of the latest and greatest state-of-the-art approaches for CV problems. It’s mostly a working collection of papers that have served a purpose for my research or simply piqued my interest since the start date of this repo.

## Papers

### Visual Question Answering (VQA)
* Show, Ask, Attend, and Answer: A Strong Baseline For Visual Question Answering [[arXiv](https://arxiv.org/abs/1704.03162)][[pdf](https://arxiv.org/pdf/1704.03162.pdf)]
  * Not state-of-the-art but they offer a simple architecture utilizing the popular stacked attention approach. No complex multi-modal fusion schemes just simple feature concatenation. Approaches SotA without training on additional data (e.g. Visual Genome).
  * Use of res5c ResNet features is needed for the SAN but requires a considerably large amount of data compared to using no attention mechanism with pool5 features. In other words, each image, when fed into the trainable portion of the network, is represented with a 14x14x2048 tensor rather than a 2048-D vector.
  * Will attempt to implement this in Keras soon.

* MUTAN: Multimodal Tucker Fusion for Visual Question Answering [[arXiv](https://arxiv.org/abs/1705.06676)][[pdf](https://arxiv.org/pdf/1705.06676.pdf)][[code](https://github.com/Cadene/vqa.pytorch)]
  * This seems to be the state-of-the-art VQA approach right now on VQAv1 dataset. Now that the VQAv2 dataset is out there’s a good chance a new SotA approach will surface from that corresponding challenge/workshop at CVPR.
  * The approach here is essentially the same as the previous SotA called [Multimodal Compact Bilinear Pooling (MCB)](https://arxiv.org/abs/1606.01847)
  * The big innovation is their multi-modal fusion scheme. The simplest approach to combine image and question features is simply concatenating the feature vectors. This seems like a naive and weak point in the common VQA approach so it’s appropriate that we see people trying to create more meaningful fusion schemes.

### Pose Estimation
* Realtime Multi-Person 2D Pose Estimation using Part Affinity Fields [[arXiv](https://arxiv.org/abs/1611.08050)][[pdf](https://arxiv.org/pdf/1611.08050.pdf)][[code](https://github.com/ZheC/Realtime_Multi-Person_Pose_Estimation)]
  * Notes coming soon

### Object Detection
* You Only Look Once: Unified, Real-Time Object Detection [[arXix](https://arxiv.org/abs/1506.02640)][[pdf](https://arxiv.org/pdf/1506.02640)]
  * Notes coming soon