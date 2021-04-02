# Track 2: Ship Detection in SAR Images

Track 2 is for the detection of ships in SAR images, whose purpose is to locate the ship in SAR images. In each image, the coordinates of ships are described in a predefined format. The horizontal bounding boxes of ships are provided in XML files.

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
| Faster RCNN | 36.13 |