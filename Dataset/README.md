# Dataset

This folder will contain benchmark datasets such as medical images and SAR images used for simulation and evaluation.

Dataset
Dataset Overview

This project uses benchmark grayscale image datasets to evaluate existing and proposed quantum image representation techniques. The datasets are selected to ensure compatibility with quantum simulation constraints while still reflecting real-world image characteristics.

Selected Datasets
1. Medical Images

X-ray and MRI grayscale images

Contain regions with both low and high detail

Commonly used in quantum image processing literature

Why chosen:

High-detail regions make them suitable for testing adaptive and hybrid encoding

Widely accepted in IEEE and Springer research

2. SAR Images (Synthetic Aperture Radar)

Grayscale radar images

Include texture-rich and background regions

Why chosen:

Useful for evaluating robustness of quantum image representations

Frequently referenced in recent quantum image processing studies

Image Size and Preprocessing

Due to current quantum hardware and simulator limitations, images are resized to:

2×2 and 4×4 pixels

Preprocessing steps:

Grayscale conversion

Pixel value normalization

Resizing to small benchmark dimensions

This approach is standard practice in quantum image processing research and enables fair comparison across different quantum image representation techniques.

Usage in This Project

The same input images are used for all existing and proposed methods

Ensures fair comparison of qubit usage, circuit complexity, and accuracy

Supports simulation-based evaluation on quantum platforms

Summary

The selected datasets provide a balance between real-world relevance and quantum simulation feasibility, making them suitable for validating both existing methods and the proposed Adaptive Hybrid Quantum Image Representation (AHQIR).
