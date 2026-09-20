# CrispTEM

A Python-based deep learning workflow for automated feature segmentation and quantitative analysis of transmission electron microscopy (TEM) images.

## Authors

* Rajat Nama
* Deepak Kumar

## Overview

CrispTEM uses a U-Net convolutional neural network (CNN) to automatically segment nanoscale features in TEM images. The workflow was developed and demonstrated for nanopore detection in zirconium (Zr) corrosion oxides.

The workflow integrates:

* Image preparation and preprocessing
* Data augmentation
* U-Net model training
* Model validation
* Batch inference
* Quantitative feature analysis

The model generates pixel-wise probability maps that can be converted into binary segmentation masks using a user-defined probability threshold. These masks can then be used to quantify detected features, including feature number, area, size, morphology, and porosity.

## Installation

Clone the repository:

```bash
git clone https://github.com/rajatnama/CrispTEM.git
cd CrispTEM
```

Install the required Python packages:

```bash
pip install -r requirements.txt
```

## Workflow

1. Prepare grayscale TEM images and corresponding pixel-level annotation masks.
2. Run data augmentation on paired images and masks.
3. Train the U-Net segmentation model.
4. Evaluate the model using held-out validation images.
5. Run inference on previously unseen TEM images.
6. Generate probability maps and binary segmentation masks.
7. Perform quantitative analysis of the segmented features.

## Input Data

CrispTEM uses:

* Grayscale TEM images
* Corresponding binary segmentation masks

The feature of interest should be represented as the foreground class in the annotation mask.

## Output

The workflow generates:

* Predicted probability maps
* Binary segmentation masks
* Feature counts
* Feature area measurements
* Porosity measurements
* Visual overlays of predicted features

## Model

CrispTEM uses a U-Net encoder-decoder convolutional neural network with skip connections for pixel-level image segmentation.

The network is trained using user-generated pixel-level masks and can be retrained for different datasets and imaging conditions.

## Applications

CrispTEM was developed and demonstrated for nanopore segmentation in Zr corrosion oxides. The workflow can also be retrained for other nanoscale TEM features and materials where conventional contrast-based image segmentation is insufficient or manual analysis is time-consuming.

## License

MIT License
