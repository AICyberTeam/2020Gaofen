# Track 3: Automatic Bridge Detection in Optical Satellite Images

In Track 3 the goal is to locate the bridge in the largescale optical satellite images. The coordinates of the bridge are horizontal bounding box.

## Baseline Algorithm
Two-stage object detection method Faster RCNN based on ResNet-50 is developed for object detection tracks.

### Introduction
It is modified from [mmdetection](https://github.com/open-mmlab/mmdetection). The master branch works with **PyTorch 1.1** or higher.

- Linux
- Python 3.5+ ([Say goodbye to Python2](https://python3statement.org/))
- PyTorch 1.1
- CUDA 9.0+
- NCCL 2+
- GCC 4.9+
- [mmcv](https://github.com/open-mmlab/mmcv)

### Code
The code will be available soon.

### Result

|    Method   | Result (mAP) |
| ----------- | ----------- |
| Faster RCNN | 59.52 |