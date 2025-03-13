# SAM2-UNet

SAM2-UNet is a deep learning model based on the U-Net architecture designed for semantic segmentation tasks. The model combines advanced techniques such as convolutional layers, residual feature blocks, and adaptive scaling to improve performance in pixel-level predictions.

## Architecture

The model architecture is composed of:
- **Encoders:** Four encoder blocks, each with convolutional layers, normalization, and downsampling.
- **RFB (Residual Feature Blocks):** Extracts high-level features from each encoder block.
- **Decoders:** Three decoder blocks, each containing two `Conv-BN-ReLU` layers followed by upsampling operations. The outputs from each decoder pass through a `1x1 Conv` segmentation head.
- **Loss Function:** A combination of weighted Intersection-over-Union (IoU) Loss and Binary Cross-Entropy (BCE) Loss.

## Loss Function

The total loss for the model is calculated as:

\[
L_{total} = \sum_{i=1}^{3} (L_{wIoU} + L_{wBCE})
\]

Where:
- \( L_{wIoU} \) is the weighted IoU loss.
- \( L_{wBCE} \) is the weighted Binary Cross-Entropy loss.

## Requirements

- Python 3.8+
- TensorFlow 2.x
- NumPy
- Matplotlib
- OpenCV (for image preprocessing)



## Training Objective

The model is trained using a combination of Weighted IoU and BCE loss with deep supervision applied to all segmentation outputs.

## Future Work
- Improving the training pipeline.
- Fine-tuning hyperparameters.
- Testing on different datasets.

## License
This project is licensed under the MIT License.

