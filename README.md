# Floorplan Generation from Noisy Point Cloud

This repository releases the data and trained models presented in our paper: [Floorplan Generation from Noisy Point Cloud] (https://dl.acm.org/doi/abs/10.1145/3615888.3627810)

Our work extends [RoomFormer](https://github.com/ywyue/RoomFormer) to operate on noisier data of point clouds composed of real-world sensor samples. We transformed the [FloorNet](https://art-programmer.github.io/floornet.html) dataset into a COCO style dataset for easier integration with RoomFormer. The raw data was collected using Tango devices with depth estimation.

### Data

Our adaptation of the FloorNet dataset captures density images in two folders ``train/`` and ``val/``, and COCO style annotations:

```
data/floorNet_COCO
└── annotations/
    └── train.json
    └── val.json
└── train/
    └── scan_i.png
    ...
└── val/
    └── scan_j.png
    ...
```
### Models

We trained several models, with the best performing checkpoints included in this repository.

- Optimised for polygon only floorplans: [link](https://floornet-data.s3.eu-west-1.amazonaws.com/polygon.pth)

- Optimised for rich semantic floorplans: [link](https://floornet-data.s3.eu-west-1.amazonaws.com/rich_sem.pth)


Licensing. Our development is built on top of other code released with the MIT license, so we carry the same conditions. 

If you are planning to use our models and dataset, please consider citing our work:
```
@inproceedings{10.1145/3615888.3627810,
  author = {Talotta, Anselmo and Radu, Valentin and Sorgi, Lorenzo},
  title = {Floorplan Generation from Noisy Point Cloud},
  year = {2023},
  publisher = {ACM},
  url = {https://doi.org/10.1145/3615888.3627810},
  doi = {10.1145/3615888.3627810},
  pages = {8–15},
  numpages = {8},
  location = {Hamburg, Germany},
  series = {GeoIndustry '23}
}
```
 
