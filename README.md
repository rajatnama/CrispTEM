# CrispTEM

A Python-based deep learning workflow for automated feature segmentation and quantitative analysis of transmission electron microscopy (TEM) images.

## Authors

- Rajat Nama
- Deepak Kumar

## Overview

CrispTEM uses a U-Net convolutional neural network to automatically segment nanoscale features in TEM images. The workflow was developed and demonstrated for nanopore detection in zirconium (Zr) corrosion oxides.

The workflow includes:
- Image preparation and preprocessing
- Data augmentation
- U-Net model training
- Model validation
- Batch inference
- Quantitative feature analysis

The output includes pixel-wise probability maps, binary segmentation masks, and quantitative measurements of detected features.

## Features

- U-Net-based image segmentation
- User-generated pixel-level annotations
- TEM-specific data augmentation
- Batch processing of TEM images
- Adjustable probability threshold for segmentation
- Automated feature counting and porosity measurement
- Support for retraining on new datasets and imaging conditions

## Installation

Clone the repository:

```bash
git clone https://github.com/rajatnama/CrispTEM.git
cd CrispTEM
