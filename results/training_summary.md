# Training Summary

## Dataset Split

- Dataset: Medical Segmentation Decathlon Task01 BrainTumour
- Configuration: 3D Full Resolution
- Fold: 0
- Training cases: 387
- Validation cases: 97

## Training Configuration

- Batch size: 2
- Patch size: 128 × 128 × 128
- Target spacing: 1 × 1 × 1 mm
- MRI modalities: 4
- Normalization: Z-score
- Network: PlainConvUNet
- GPU: NVIDIA Tesla T4

## Best Recorded Result

- Best validation EMA pseudo-Dice: **0.7679 (76.79%)**
- Best epoch: **35**

## Epoch 36

Class-wise pseudo-Dice:

- Class 1: 0.7688
- Class 2: 0.6599
- Class 3: 0.8535

Validation loss:

- **-0.6020**

## Reproduction Limitation

The trained model checkpoint was not retained after the experimental Colab session.

Therefore, independent test-set inference and final test metrics could not be reproduced.

The quantitative result reported here is limited to the validation metrics recorded during training.
