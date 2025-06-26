# transformer-resolution-scaling
##  MNIST Super-Resolution with Deep Learning

This project implements a Super-Resolution framework for enhancing MNIST digit images using deep learning. The main goal is to reconstruct high-resolution (HR) images from their low-resolution (LR) counterparts and evaluate the perceptual and structural fidelity of the generated outputs.

###  Key Features

- **Custom Dataset Class**: A PyTorch `Dataset` is created to downscale MNIST images and return LR-HR pairs for training the model.

- **Super-Resolution Network**: A convolutional neural network is designed for upscaling MNIST images from 14×14 back to the original 28×28 resolution.

- **Perceptual Loss (VGG-based)**: In addition to pixel-wise losses (like MSE), the model optionally uses a perceptual loss computed using intermediate features from a pre-trained VGG-19 network.

- **Evaluation Metrics**:
  - PSNR (Peak Signal-to-Noise Ratio)
  - SSIM (Structural Similarity Index)

- **Cross-Validation**: Implements Leave-One-Out Cross Validation (LOOCV) to evaluate model generalization.

- **Visualization**: Saves and plots low-resolution, super-resolved, and ground truth images for qualitative assessment.

###  Results

The model is evaluated both quantitatively (PSNR, SSIM) and visually. The super-resolved digits closely resemble the originals, showing that the model successfully learns the mapping from LR to HR digits.
