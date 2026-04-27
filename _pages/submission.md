---
layout: default
title: Submission
permalink: /submission/
---

## Submission

Submissions are made through the [Codabench competition page](add link when ready...). To prepare a valid submission, apply your compression algorithm to the test dataset and generate the required outputs using our provided pipeline. 

### Instructions

1. **Compress the Test Dataset**  
   Run your compression algorithm on the test dataset. Save both the compressed (any format) and decompressed (.tiff) versions of each block.

2. **Generate Segmentations and Skeletons**  
   Use the provided segmentation pipeline in our [GitHub repository](https://github.com/AllenNeuralDynamics/image-compression-challenge/tree/main), see [generate_submission.py](https://github.com/AllenNeuralDynamics/image-compression-challenge/blob/main/src/image_compression_challenge/generate_submission.py) to:
   - Generate segmentations from the decompressed images.
   - Generate SWC files (neuron skeletons) from the segmentations.

3. **Package Your Submission**  
   Combine your outputs into a single ZIP archive with the compressed images, decompressed images, segmentations, and SWCs. 

4. **Submit on Codabench**  
Upload your ZIP file to the Codabench platform for scoring.

### Evaluation

Submissions are scored on:
- **Compression ratio** — how much the file size is reduced.
- **Image quality** — measured by Structural Similarity Index (SSIM ≥ 0.9).
- **Segmentation accuracy** — how well the compressed data preserves neuron structures for downstream analysis.

For detailed submissions instruction and information on the segmentation pipeline, visit our [GitHub repository](https://github.com/AllenNeuralDynamics/image-compression-challenge).