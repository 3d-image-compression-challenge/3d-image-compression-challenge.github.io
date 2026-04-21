---
layout: default
title: Dataset
permalink: /dataset/
---
## Dataset

The dataset comes from whole mouse brains imaged with the [ExaSPIM](https://alleninstitute.org/news/scientific-overview-exa-spim/) light sheet microscope at the Allen Institute for Neural Dynamics. A subset of neurons in each brain are fluorescently labeled, allowing researchers to trace their shapes and connections in 3D. 

(to do - include some sample images) 

Because whole-brain images are large (~20 TB each), we've broken the data into smaller **3D blocks**, for the challenge. Each block is a cutout from one of these whole-brain images and contains labeled neurons along with their surrounding tissue.

Each block is provided in **OME-Zarr format**, a standard for large-scale 3D image data. Alongside each block, we provide **segmentations** and **SWC files**, which describe the traced shapes and skeletons of neurons. These were generated using a lightweight [segmentation pipeline](https://github.com/AllenNeuralDynamics/segmentation-skeleton-metrics) developed for the challenge — a streamlined version of the production pipeline used at the Allen Institute that produces realistic segmentation performance. Together, these files serve as ground truth for evaluating how well compressed images preserve biological strucutures needed for downstream analysis. 

### Train/Test/Held-Out Blocks

The blocks are split into train, test, held-out groups for the competition. 

- **10 training blocks** — for developing and testing your compression algorithms.
- **5 test blocks** — used for evaluation during the development phase.
- **Held-out blocks** — used for final evaluation, released one week before the competition ends.

### Accessing the Data

The dataset is publicly available hosted on [S3](https://open.quiltdata.com/b/aind-benchmark-data/tree/3d-image-compression/). For instructions on downloading and working with the data, see the [README](https://open.quiltdata.com/b/aind-benchmark-data/tree/3d-image-compression/README.md) 
