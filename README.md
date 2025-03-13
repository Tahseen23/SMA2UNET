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
L_total =  (L_{wIoU} + L_{wBCE})
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

## Results
![Screenshot 2025-03-13 163839](https://github.com/user-attachments/assets/04c49920-d2ea-475f-8724-e3469b859150)
![Screenshot 2025-03-13 163855](https://github.com/user-attachments/assets/a5a73552-dedc-42bb-8429-056b92ff0339)

## Dataset
kaggle-https://www.kaggle.com/datasets/balraj98/duts-saliency-detection-dataset

## Future Work
- Improving the training pipeline.
- Fine-tuning hyperparameters.
- Testing on different datasets.

## License
This project is licensed under the MIT License.

