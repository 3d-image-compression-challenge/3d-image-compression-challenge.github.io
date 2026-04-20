---
layout: default
title: Overview
permalink: /overview/
---

# Compression Challenge on 3D Microscopy Images

## Welcome to the Challenge
The Compression Challenge on 3D Microscopy Images invites researchers, engineers, and enthusiasts to develop cutting-edge image compression methods for massive 3D microscopy datasets. Hosted by the Allen Institute for Neural Dynamics, this competition focuses on reducing the size of high-resolution whole-brain microscopy images while preserving critical biological features. 

## Why This Challenge?
Modern light sheet microscopy, such as the ExaSPIM, generates terabytes of data per brain, capturing images of large tissues, such as whole mouse brains, at single cell resolution. Efficient compression of these datasets is essential for enabling large-scale neuroscience studies, reducing storage costs, and improving data accessibility.

## Task
Participants will design algorithms to compress 3D microscopy images, achieving higher compression ratios than current standard methods. The challenge focuses on preserving image quality and the biological details needed to ensure the compressed data can be used for downstream processing, including identifying and tracing the shapes of neurons in 3D. 

## Key Details

**Dataset:** Provided in OME-Zarr format, the dataset includes 10 training blocks and 5 test blocks of whole-brain microscopy data.

**Evaluation:**Submissions are scored on compression efficiency, Structural Similarity Index (SSIM ≥ 0.9), and segmentation accuracy.


**Phases:**  
**Phase 1:** Initial test set for model development.
**Phase 2:** Final test set for leaderboard ranking. 

**Prizes:** Awards for top compression performance, segmentation accuracy, and best submission in Zarr format. 


## Get Started 

**Platform:** The competition runs on Codabench, where you’ll find the full evaluation pipeline and submission guidelines. 

**Resources:** Access the dataset and baseline code on GitHub. 

## Join Us
This challenge is open to anyone with expertise in neuroscience, data science, machine learning, or image processing. Your contributions will advance neuroscience by making large-scale brain imaging data more accessible and analyzable.