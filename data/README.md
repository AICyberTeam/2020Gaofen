# DATA 
To satisfy the needs of practical applications and the highresolution earth observation system construction requirements for major national scientific and technological projects, images in Gaofen Challenge are collected from Gaofen-2 satellite and Gaofen-3 satellite. Specifically, we use the Gaofen-2 optical satellite data with 0.8-4m resolution for the Airplane Detection, Bridge Detection, Water-body Segmentation and so on. And the Gaofen-3 SAR data with 1-5m resolution is used for Ship Detection, Semantic Segmentation in Polarimetric SAR and so on. To obtain high-quality data, we invited hundreds of experts taking more than three months to prepare the dataset. Finally, a large-scale and challenging dataset with various categories, multiple sensors and tremendous object instances have been published for Gaofen Challenge.

## Data Description:
The Gaofen-2 optical satellite data with 0.8-4m resolution is used for the Airplane Detection, Bridge Detection, Water-body Segmentation and so on. And the Gaofen-3 SAR data with 1-5m resolution is used for Ship Detection, Semantic Segmentation in Polarimetric SAR and so on.

|    Track    | DESCRIPTION |
| ----------- | ----------- |
|   Track-1   | Data for Track 1 (Airplane Detection and Recognition in Optical Images) were provided by Gaofen-2 satellite. The scenes include the main civil airports in the world, such as Sydney Airport, Beijing Capital International Airport, Shanghai Pudong International Airport, Hongkong Airport, Tokyo International Airport, and so on. It contains 3000 remote sensing images with spatial resolution of 0.8m. Each image is of the size 1000x1000 pixels and contains 10 categories of airplanes (i.e. Boeing 737, Boeing 747, Boeing 777, Boeing 787, Airbus A220, Airbus A321, Airbus A330, Airbus A350, COMAC ARJ21, and other) exhibiting a wide variety of orientations and scales. |
|   Track-2   | Data for Track 2 (Ship Detection in SAR Images) were collected from Gaofen-3 satellite. It contains 1000 SAR images with spatial resolution ranging from 1m-5m. Each image is of the size 1000x1000 pixels and contains ships exhibiting a wide variety of orientations and scales. The scenes include the main civil ports in the world, such as Victoria Harbour, Port of Sanya, Incheon Port, and so on. |
|   Track-3   | Data for Track 3 (Automatic Bridge Detection in Optical Satellite Images) were provided by Gaofen-2 satellite with the resolution ranging from 1m-4m. Each image contains at least one bridge, covering railway bridges, highway bridges, road-rail bridges, pedestrian bridges, water-carrying bridges, and so on. There are 3000 images with different sizes ranging from 667x667 to 1001x1001 pixels in bridge dataset. |
|   Track-4   | Data for Track 4 (Semantic Segmentation in Optical Satellite Images) were provided by Gaofen-2 satellite with 0.8m resolution. Each image was finely annotated with nine categories of ground objects at the pixel level, including road, building, shrub & tree, lawn, land, waterbody, vehicle, impervious ground, and other. There are 1800 images with the size ranging from 512 to 5000 pixels. |
|   Track-5   | Data for Track 5 (Automatic Water-Body Segmentation in Optical Satellite Images) were provided by Gaofen-2 satellite with the resolution ranging from 1m-4m, covering rivers and lakes in large-scope. There are 2500 images with the size ranging from 492 to 2000 pixels in water-body dataset. |
|   Track-6   | Data for Track 6 (Semantic Segmentation in Fully Polarimetric SAR Images) were provided by Gaofen-3 satellite with 1-3m resolution, containing 4 polarization modes (i.e. HH, VV, HV, and VH). Six categories including water-body, building, industrial area, lawn, land, and others were annotated at the pixel level for each image. There are 1200 images with the size ranging from 512 to 1500 pixels. |


## Image sizes:

| Track   | train set number | preliminary test set number | final test set number | Resolution (pixel) | Size (GB) |
| ------- | -----------------| --------------------------- | ----------------------| ------------------ | --------- |
| Track-1 | 1000 | 1000 | 1000 | 1000x1000 | 5 |
| Track-2 | 300 | 400 | 300 |1000x1000 | 2 |
| Track-3 | 2000 | 1000 | 1500 |512-12000 | 5.3 |
| Track-4 | 500 | 300 | 1000 | 512-5000   | 3.24 |
| Track-5 | 1000 | 500 | 1000 |492-2000   | 1.2 |
| Track-6 | 500 | 300 | 400 | 512-1500   | 2 |
