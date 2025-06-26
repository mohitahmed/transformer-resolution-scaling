# transformer-resolution-scaling
##  Transformer-based MNIST Super-Resolution

This project implements a Transformer-based Super-Resolution framework for enhancing MNIST digit images using deep learning. The main goal is to reconstruct high-resolution (HR) images from their low-resolution (LR) counterparts and evaluate the perceptual and structural fidelity of the generated outputs.

###  Key Features

- **Patch-based Tokenization**: Low-resolution MNIST images are divided into non-overlapping patches and embedded into a sequence suitable for transformer processing.

- **Transformer Encoder Blocks**: A series of self-attention-based encoder blocks model long-range dependencies across image patches, capturing global structure and context.

- **CNN Decoder with PixelShuffle**: The transformer outputs are reshaped into a spatial grid and decoded using convolutional layers and pixel shuffle blocks to reconstruct the high-resolution image.

- **Perceptual Loss (VGG-based)**: In addition to pixel-wise losses (like MSE), the model optionally uses a perceptual loss computed using intermediate features from a pre-trained VGG-19 network.

- **Evaluation Metrics**:
  - PSNR (Peak Signal-to-Noise Ratio)
  - SSIM (Structural Similarity Index)

- **Cross-Validation**: Implements Leave-One-Out Cross Validation (LOOCV) to evaluate model generalization.

- **Visualization**: Saves and plots low-resolution, super-resolved, and ground truth images for qualitative assessment.

###  Results

The model is evaluated both quantitatively (PSNR, SSIM) and visually. The super-resolved digits closely resemble the originals, demonstrating that the Transformer-CNN hybrid architecture effectively learns to reconstruct detailed images from low-resolution inputs.
