# Track 4: Semantic Segmentation in Optical Satellite Images

Track 4 is for semantic segmentation in optical satellite images. A pair of images are provided for each geographic tile. One is the original optical satellite image, and the other is an image annotated with the ground truth which is the same size as the previous satellite image. In ground truth images, different categories are marked with different RGB values in pixel level.

## Baseline Algorithm
For semantic segmentation tracks, using PSPNet based on ResNet-50 as baseline solution. 

### Introduction
PSPNet baseline for semantic segmentation tracks in 2020 Gaofen Challenge is written by the deep learning framework of PyTorch.

- Linux
- Python 3.5+
- PyTorch 1.0+
- CUDA 10.0+
- NCCL 2+
- GCC 4.9+



### Data format

* Convert the data format to the same as Vaihingen and modify the ${CONFIG_FILE}.

    Assuming `C` as number of classes in the semantic segmentation dataset, then valid label ids are from `0` to `C-1`. And we tend to set the ignore label as 255 where loss calculation will be ignored and no penalty will be given on the related ground truth regions. If original ground truths ids are not in needed format, you may need to do label id mapping

* Prepare the `$DATASET$_colors.txt` and `$DATASET$_names.txt` accordingly. Get the training/testing ground truths and lists ready.


### Code
The code will be available soon.

### Result

|    Method   | Result (FWIoU) |
| ----------- | ----------- |
|    PSPNet   | 69.78 |