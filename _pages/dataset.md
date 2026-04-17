## Dataset

The dataset for this challenge consists of **10 training blocks** and **5 test blocks**, which are 3D cutouts from high-resolution whole-brain microscopy images. These blocks were collected using the ExaSPIM light sheet microscope and are provided in **OME-Zarr format**. Accompanying each image block are SWC files that represent the skeletons of the segmented neurons, which are used to evaluate segmentation accuracy. 

### Key Details
- **Training Blocks**: Used to develop and test your compression algorithms.
- **Test Blocks**: Used for evaluation during the development phase of the competition. 
- **Held-out Blocks**: Used for final evaluation of the competition. 

The provided [packaging code](https://github.com/AllenNeuralDynamics/image-compression-challenge/) will generate SWC files from the decompressed data for evaluation.

### Access the Dataset
The dataset is hosted on [S3](https://open.quiltdata.com/b/aind-benchmark-data/tree/3d-image-compression/). 
