---
layout: default
title: Dataset
permalink: /dataset/
---

## Dataset

<figure class="figure">
  <img src="{{ site.baseurl }}/media/exaspim-flythru.gif" alt="A whole mouse brain with neurons labelled" />  <figcaption>A whole mouse brain with neurons labelled</figcaption>
</figure>

<figure class="figure">
  <img src="{{ site.baseurl }}/media/exaspim-flythru-sagittal.mp4" alt="A whole mouse brain with neurons labelled" />  <figcaption>A whole mouse brain with neurons labelled</figcaption>
</figure>

The dataset comes from whole mouse brains imaged with the [ExA-SPIM](https://alleninstitute.org/news/scientific-overview-exa-spim/) light sheet microscope at the Allen Institute Neural Dynamics Accelerator. A subset of neurons in each brain are fluorescently labeled, allowing researchers to trace their shapes and connections in 3D. The data is largely sparse, but the labeled neuronal structures of interest can be very thin (single voxel) and have weak intensity boundaries — properties that make this a tractable, but challenging compression challenge. (Read more about how the data was generated and processed [here.](https://allenneuraldynamics.org/platforms/brain-wide-anatomy-at-cellular-resolution))

<figure class="figure">
  <img src="{{ site.baseurl }}/media/data-media.gif" alt="Visualization of a 3D image block from the dataset" />
  <figcaption>Slices of a 3D image block from the dataset.</figcaption>
</figure>

Because whole-brain images are large (~120 TB each), we've broken the data into smaller **3D blocks** for the challenge. Each block is a cutout from one of these whole-brain images and contains labeled neurons along with their surrounding tissue.

<figure class="figure">
  <img src="{{ site.baseurl }}/media/medulla_media.png" alt="Neurons in the medulla within a whole-brain image" />
  <figcaption>Neurons in the medulla within a whole-brain image, captured with ExA-SPIM.</figcaption>


Each block is provided in **OME-Zarr format**, a standard for large-scale 3D image data. Alongside each block, we provide **segmentations** and **SWC files**, which describe the traced shapes and skeletons of neurons. These were generated using the [segmentation pipeline](https://github.com/AllenNeuralDynamics/aind-exaspim-neuron-segmentation/tree/main). Together, these files serve as ground truth for evaluating how well compressed images preserve biological structures needed for downstream analysis.

<figure class="figure">
  <img src="{{ site.baseurl }}/media/annotations-compressed.mp4" alt="Annotations video" />  <figcaption>Process for annotating the skeleton of a single neuron in the ExA-SPIM volume </figcaption>
</figure>

### Train/Test/Held-Out Blocks

The blocks are split into train, test, held-out groups for the competition.

- **10 training blocks** — for developing and testing your compression algorithms.
- **5 test blocks** — used for evaluation during the development phase.
- **Held-out blocks** — used for final evaluation, released one week before the competition ends.

### Accessing the Data

The dataset is publicly hosted on [S3](https://open.quiltdata.com/b/aind-benchmark-data/tree/3d-image-compression/). For instructions on downloading and working with the data, see the [README](https://open.quiltdata.com/b/aind-benchmark-data/tree/3d-image-compression/README.md).



---
layout: default
title: Dataset
permalink: /dataset/
---

## Dataset

The dataset comes from whole mouse brains imaged with the [ExA-SPIM](https://alleninstitute.org/news/scientific-overview-exa-spim/) light sheet microscope at the Allen Institute Neural Dynamics Accelerator. A subset of neurons in each brain are fluorescently labeled, allowing researchers to trace their shapes and connections in 3D.

<figure class="figure">
  <img src="{{ site.baseurl }}/media/exaspim-flythru.gif" alt="Fly-through of a whole mouse brain imaged with ExA-SPIM" />
  <figcaption>A fly-through of a whole mouse brain imaged with ExA-SPIM. Bright structures are individual fluorescently labeled neurons spanning the entire brain.</figcaption>
</figure>

The data is largely sparse, but the labeled neuronal structures of interest can be very thin (as small as a single voxel) and have weak intensity boundaries, properties that make this a tractable but challenging compression problem. (Read more about how the data was generated and processed [here](https://allenneuraldynamics.org/platforms/brain-wide-anatomy-at-cellular-resolution).)

### Image Blocks

Because whole-brain images are large (~120 TB each), we've broken the data into smaller **3D blocks** for the challenge. Each block is a cutout from one of these whole-brain images and contains labeled neurons along with their surrounding tissue.

<figure class="figure">
  <img src="{{ site.baseurl }}/media/data-media.gif" alt="2D slices through a 3D image block, showing how labeled neurons appear across depth" />
  <figcaption>Sequential 2D slices through a 3D image block, showing how labeled neurons appear across depth.</figcaption>
</figure>

<figure class="figure">
  <img src="{{ site.baseurl }}/media/medulla_media.png" alt="Example 3D image block showing labeled neurons in the medulla region of the mouse brain" />
  <figcaption>Example 3D image block showing labeled neurons in the medulla, a region near the base of the brain.</figcaption>
</figure>

### Annotations

Each block is provided in **OME-Zarr format**, a standard for large-scale 3D image data. Alongside each block, we provide **segmentations** (3D masks identifying which voxels belong to each neuron) and **SWC files** (graph representations of neuron skeletons). These were generated using our [segmentation pipeline](https://github.com/AllenNeuralDynamics/aind-exaspim-neuron-segmentation/tree/main) and serve as ground truth for evaluating how well compressed images preserve the biological structures needed for downstream analysis.

<figure class="figure">
  <img src="{{ site.baseurl }}/media/annotations.mp4" alt="Process for annotating the skeleton of a single neuron in a 3D image block" />
  <figcaption>Annotating the skeleton of a single neuron in a 3D image block. </figcaption>
</figure>

### Train, Test, and Held-Out Blocks

The blocks are split into three groups for the competition:

- **10 training blocks** — for developing and testing compression methods.
- **5 test blocks** — used for evaluation during the development phase.
- **Held-out blocks** — used for final evaluation, released near the end of the competition.

### Accessing the Data

The dataset is publicly hosted on [S3](https://open.quiltdata.com/b/aind-benchmark-data/tree/3d-image-compression/). For instructions on downloading and working with the data, see the [README](https://open.quiltdata.com/b/aind-benchmark-data/tree/3d-image-compression/README.md).