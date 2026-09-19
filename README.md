# nnunet-brain-tumor-segmentation
Experimental reproduction of nnU-Net for 3D brain tumor segmentation using the Medical Segmentation Decathlon BrainTumour dataset.
# Experimental Reproduction of nnU-Net for Brain Tumor Segmentation

An experimental reproduction of the nnU-Net medical image segmentation pipeline using the Medical Segmentation Decathlon (MSD) Task01 BrainTumour dataset.

## 📌 Project Overview

This project explores the reproduction of the nnU-Net framework for 3D brain tumor segmentation from multi-modal MRI scans.

The implementation uses nnU-Net v2, which automatically configures important parts of the segmentation pipeline based on the characteristics of the dataset, including preprocessing, target spacing, patch size, network configuration, and training setup.

The experiment focuses on a single public dataset rather than reproducing the complete evaluation of the original nnU-Net paper.

## 🧠 Dataset

**Medical Segmentation Decathlon — Task01 BrainTumour**

The dataset contains four MRI modalities:

- FLAIR
- T1-weighted
- T1-weighted with gadolinium enhancement (T1gd)
- T2-weighted

The experiment used the training portion of the dataset with an automatically generated Fold 0 split:

- Training cases: 387
- Validation cases: 97

## ⚙️ Experimental Configuration

| Parameter | Configuration |
|---|---|
| Framework | nnU-Net v2 |
| Configuration | 3D Full Resolution |
| Fold | 0 |
| Batch Size | 2 |
| Patch Size | 128 × 128 × 128 |
| Target Spacing | 1 × 1 × 1 mm |
| Modalities | 4 MRI channels |
| Normalization | Z-score normalization |
| Network | PlainConvUNet |
| GPU | NVIDIA Tesla T4 |
| Training | Experimental limited-duration run |

The automatically generated network used six stages with feature sizes of:

`32, 64, 128, 256, 320, 320`

## 📊 Results

The best recorded validation result during the experimental training run was:

**Best validation EMA pseudo-Dice: 0.7679 (76.79%)**

This was recorded at:

**Epoch 35**

At Epoch 36, the recorded class-wise pseudo-Dice values were:

- 0.7688
- 0.6599
- 0.8535

The validation loss at Epoch 36 was:

`-0.6020`

## 🔬 Interpretation

The experiment demonstrated that nnU-Net could automatically configure and train a 3D full-resolution segmentation pipeline for the BrainTumour dataset.

The recorded validation performance indicates meaningful tumor-region segmentation during the experimental training run.

However, the trained model checkpoint was not retained after the Colab session. Therefore, independent test-set inference and final test metrics could not be reproduced.

The reported quantitative result is consequently limited to the validation metrics recorded during training.

## 📚 Reference

Isensee, F., Jaeger, P. F., Kohl, S. A. A., Petersen, J., & Maier-Hein, K. H. (2021).

**nnU-Net: a self-configuring method for deep learning-based biomedical image segmentation.**

Nature Methods, 18, 203–211.

DOI: 10.1038/s41592-020-01008-z

## 🛠️ Technologies

- Python
- PyTorch
- nnU-Net v2
- NVIDIA CUDA
- Google Colab
- Medical Segmentation Decathlon
- 3D Medical Image Segmentation
- MRI

## ⚠️ Reproduction Note

This repository documents an experimental reproduction of the nnU-Net pipeline on the MSD BrainTumour dataset.

It should not be interpreted as an exact reproduction of all experiments reported in the original nnU-Net paper.
