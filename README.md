# Spectral Super Resolution using Residual CNN and Efficient Channel Attention

## Overview

This repository presents a deep learning framework for hyperspectral image reconstruction from multispectral imagery. The proposed model employs a Residual Convolutional Neural Network (ResCNN) integrated with an Efficient Channel Attention (ECA) mechanism to recover high-dimensional spectral information from low-dimensional multispectral inputs.

The framework is designed for remote sensing applications, including:

* Hyperspectral image reconstruction
* Spectral super-resolution
* Land use and land cover analysis
* Environmental monitoring
* Precision agriculture
* Earth observation studies

---

## Key Features

* Residual CNN architecture with skip connections
* Efficient Channel Attention (ECA) module for spectral feature enhancement
* MSI-to-HSI reconstruction
* GeoTIFF input and output support
* Patch-based training and prediction
* Parameter sensitivity analysis
* RMSE and PSNR performance evaluation
* TensorFlow/Keras implementation

---

## Network Architecture

### Input

* Multispectral Image (MSI)

### Feature Extraction

* 1×1 Convolution Layer
* 64 Feature Maps

### Residual Blocks (×3)

Each block contains:

* 3×3 Convolution
* 1×1 Convolution
* Feature Concatenation
* 1×1 Convolution
* Efficient Channel Attention (ECA)
* Residual Skip Connection

### Reconstruction Layer

* 1×1 Convolution
* ECA Refinement
* Hyperspectral Output

---

## Dataset

The framework supports hyperspectral datasets such as:

* Hyperion
* HYDICE
* Pavia University
* Custom MSI-HSI datasets

Input format:

* MATLAB (.mat)
* GeoTIFF (.tif)

---

## Requirements

Python 3.9+

Libraries:

```bash
tensorflow
numpy
scipy
rasterio
matplotlib
pandas
scikit-learn
```

Install dependencies:

```bash
pip install tensorflow numpy scipy rasterio matplotlib pandas scikit-learn
```

---

## Training

Run the training script to train the ResCNN-ECA model:

```bash
python train.py
```

Training parameters:

| Parameter      | Value |
| -------------- | ----- |
| Epochs         | 50    |
| Batch Size     | 32    |
| Learning Rate  | 0.01  |
| Patch Size     | 8     |
| Training Ratio | 70%   |

---

## Prediction

Load the trained model and perform MSI-to-HSI reconstruction:

```bash
python predict.py
```

Outputs:

* Predicted hyperspectral cube
* GeoTIFF export
* Spectral visualization

---

## Evaluation Metrics

The model performance is evaluated using:

* Root Mean Square Error (RMSE)
* Peak Signal-to-Noise Ratio (PSNR)

Formulas:

RMSE:

RMSE = sqrt(mean((y_true - y_pred)^2))

PSNR:

PSNR = 20 × log10(MAX / RMSE)

---

## Parameter Sensitivity Analysis

The framework evaluates:

### Patch Size Sensitivity

* 4 × 4
* 8 × 8
* 16 × 16
* 32 × 32

### Training Ratio Sensitivity

* 50%
* 60%
* 70%
* 80%

Performance is analyzed using RMSE and PSNR.

---

## Results

The proposed ResCNN-ECA model demonstrates:

* Improved spectral reconstruction accuracy
* Lower reconstruction error
* Enhanced spectral feature preservation
* Better PSNR compared to baseline configurations
---

## Applications

* Remote Sensing
* Precision Agriculture
* Environmental Monitoring
* Land Cover Mapping
* Mineral Exploration
* Climate Studies

---

## Author

Dinesh Kumar Manchala

Department of Information Technology

Siddhartha Academy of Higher Education

India

---

## License

This project is released under the MIT License.
