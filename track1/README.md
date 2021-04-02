# Track 1: Airplane Detection and Recognition in Optical Images

Track 1 is for the detection and recognition of airplanes in optical remote sensing images. For each image in the dataset, there is an XML file with the same name for describing annotation information. Each airplane instance in images is annotated by the corresponding category information and location with an oriented bounding box.

## Baseline Algorithm
Two-stage object detection method Faster RCNN based on ResNet-50 is developed for object detection tracks. For Track 1, add an angle information regression to realize rotated boxes regression.

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
| Faster RCNN | 48.42 |