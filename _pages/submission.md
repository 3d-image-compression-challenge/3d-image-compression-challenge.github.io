---
layout: default
title: Submission
permalink: /submission/
---

## Submission

Submissions are made through the [Codabench competition page](#). To prepare a valid submission, apply your compression method to the image blocks in the test dataset and generate the required outputs using our provided pipeline.

### Instructions

1. **Compress the test dataset**  
   Apply your compression method to each image block in the test dataset. Save both the compressed (any format) and decompressed (`.tiff`) versions of each block.

2. **Generate segmentations and skeletons**  
   Run [`generate_submission.py`](https://github.com/AllenNeuralDynamics/image-compression-challenge/blob/main/src/image_compression_challenge/generate_submission.py) from the [image-compression-challenge](https://github.com/AllenNeuralDynamics/image-compression-challenge) repository to produce:
   - Segmentations from the compressed images.
   - Neuron skeletons (SWC files) from the segmentations.

3. **Prepare your write-up and code**  
   Write a 1–2 page document describing your compression method, including the underlying approach, key design choices, and any external resources used (e.g., pretrained models, datasets). Provide the code used to run your method end-to-end, along with a README and Dockerfile to reproduce the results. 

4. **Package your submission**  
   Combine all outputs into a single ZIP archive containing the compressed images, decompressed images, segmentations, SWC files, write-up, code, README, and Dockerfile.

5. **Submit on Codabench**  
   Upload your ZIP file to the [Codabench platform](#) for scoring.

### Evaluation

Submissions are scored on:

- **Compression ratio** — how much the file size is reduced.
- **Image quality** — measured by Structural Similarity Index (SSIM ≥ 0.9).
- **Segmentation accuracy** — how well the compressed data preserves neuron structures for downstream analysis.

For full details on the scoring code and submission requirements, see our [GitHub repository](https://github.com/AllenNeuralDynamics/image-compression-challenge).