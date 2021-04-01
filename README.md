# 2020 Gaofen Challenge data, baselines, and metrics
For more information visit 2020 Gaofen Challenge on Automated High-Resolution Earth Observation Image Interpretation: [Tracks 1-2](http://en.sw.chreos.org/), [Tracks 3-6](http://sw.chreos.org/).


## Cloning this repository
This repository contains large model files used by baseline algorithms. The model files do not need to be downloaded, but are provided as a convenience. Please use [git lfs](https://git-lfs.github.com/) when cloning to have access to these models. If you did not install and initialize git lfs before cloning, you can simply run `git lfs fetch` after locally initializing git lfs.

## Challenge Tracks
### Track 1: Airplane Detection and Recognition in Optical Images
[Track 1](track1) is for the detection and recognition of airplanes in optical remote sensing images. For each image in the dataset, there is an XML file with the same name for describing annotation information. Each airplane instance in images is annotated by the corresponding category information and location with an oriented bounding box.

### Track 2: Ship Detection in SAR Images
[Track 2](track2) is for the detection of ships in SAR images, whose purpose is to locate the ship in SAR images. In each image, the coordinates of ships are described in a predefined format. The horizontal bounding boxes of ships are provided in XML files.

### Track 3: Automatic Bridge Detection in Optical Satellite Images
In [Track 3](track3) the goal is to locate the bridge in the largescale optical satellite images. The coordinates of the bridge are horizontal bounding box.

### Track 4: Semantic Segmentation in Optical Satellite Images
[Track 4](track4) is for semantic segmentation in optical satellite images. A pair of images are provided for each geographic tile. One is the original optical satellite image, and the other is an image annotated with the ground truth which is the same size as the previous satellite image. In ground truth images, different categories are marked with different RGB values in pixel level.

### Track 5: Automatic Water-Body Segmentation in Optical Satellite Images
In [Track 5](track5) the purpose is to locate the water-body in the optical satellite images with pixel level. The original optical satellite images and ground truth images were provided for water-body segmentation.

### Track 6: Semantic Segmentation in Fully Polarimetric SAR Images
[Track 6](track6) is a semantic segmentation track for SAR
images. Its goal is to classify the features in SAR satellite images with pixel level.

## Performance
For the track of object detection (Track 1-3), mean Average Precision (mAP) with the Intersection over Union (IoU) threshold of 0.5 is used to evaluate the results. For a given ground truth and the predicted result, TP, FP, FN are selected according to an IoU threshold of 0.5. Then the precision and recall are calculated. According to Pascal VOC 2012, the AP of each class is calculated based on precision and recall, and then the mAP can be obtained. For the track of semantic segmentation (Track 4-
6), Frequency Weighted Intersection over Union (FWIoU) is
used as an accuracy evaluation indicator.

## Data
Data from Chinese Gaofen satellites were provided for all
six tracks of the 2020 Gaofen Challenge. The data used in the challenge includes multi-scale, multi-view, multi-resolution optical remote sensing images and SAR images, with ground truth geometric and semantic labels. The optical remote sensing images and SAR images were all collected from Gaofen-2 and Gaofen-3 satellites with the resolution ranging from 1-4 meters and 1-5 meters, respectively. The data containing more than 10,000 images were annotated by more than 100 experts over 3 months.

## Baseline algorithms
Classic object detection and semantic segmentation networks
are used as baseline solutions of each track separately.
Two-stage object detection method Faster RCNN based on
ResNet-50 is developed for object detection tracks. For Track 1, add an angle information regression to realize rotated boxes regression. For semantic segmentation tracks, using PSPNet based on ResNet-50 as baseline solution. These baselines are available in the Track 1-6 folders referenced above.

## Submission requirements
Submissions must match the formats and data types described on the challenge website. Please check your files before submitting. There is no requirement to use a particular language for producing submissions.

## Acknowledgements
We are very grateful for the support of the IEEE Geoscience and Remote Sensing Society, especially to Professor Paolo Gamba, Professor Jun Li, and the Image Analysis and Data Fusion Technical Committee for their valuable comments. And many thanks to the International Society for Photogrammetry and Remote Sensing, especially to Professor Charles Toth and Professor Stefan Hinz for their great support. It is also supported by the National Natural Science Foundation of China 61725105 and the National Major Project on China High-resolution Earth Observation System GFZX0404120201.

## Reference
For more information on the data of Track 4:
X. Sun, A. Shi, H. Huang, H. Mayer. BAS4Net: Boundary-Aware Semi-Supervised Semantic Segmentation Network for Very High-Resolution Remote Sensing Images. IEEE Journal of Selected Topics in Applied Earth Observations and Remote Sensing, 2020. DOI: 10.1109/JSTARS.2020.3021098.

