# Experimental Training Results

The training results documented in this repository come from an experimental nnU-Net v2 training run on the Medical Segmentation Decathlon Task01 BrainTumour dataset.

The best recorded validation EMA pseudo-Dice was **0.7679 (76.79%) at Epoch 35**.

The experiment was performed using the 3D full-resolution configuration on an NVIDIA Tesla T4.

Because the trained checkpoint was not retained after the Colab session, test-set inference and final test metrics are not included.

See [`training_summary.md`](training_summary.md) for the recorded configuration and results.
