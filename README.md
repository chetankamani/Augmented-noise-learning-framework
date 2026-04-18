Augmented Noise Learning (ANL) for Medical Image Denoising

This repository presents an implementation of an Augmented Noise Learning (ANL) framework for medical image denoising, combining the strengths of dictionary learning (K-SVD) and a Deep Residual Network (DRN). The proposed approach is designed to effectively handle complex noise patterns commonly found in CT images, especially Poisson noise.

🔍 Overview

Traditional denoising techniques like K-SVD rely on sparse representations and fail to capture complex noise distributions. On the other hand, deep learning models such as DRN can learn data-driven noise patterns but may miss fine structural details.

This work integrates both approaches:

K-SVD captures local sparse structures
DRN learns global residual noise patterns
Final output is obtained by fusion of residuals from both methods
⚙️ Key Features
Patch-based image processing with overlapping patches
DCT-based dictionary initialization
Sparse coding using Orthogonal Matching Pursuit (OMP)
Deep Residual Network for noise estimation
Residual fusion strategy for improved denoising
Supports grayscale CT images (PNG format)
Evaluation using PSNR and SSIM
🧠 Methodology
Input image is divided into overlapping patches
Each patch is processed using:
K-SVD for sparse reconstruction → Residual R
1
	​

DRN for learned noise estimation → Residual R
2
	​


R = (R1 + R2) / 2	​

	​

Denoised patches are reconstructed to form the final image
📊 Evaluation Metrics
Peak Signal-to-Noise Ratio (PSNR)
Structural Similarity Index (SSIM)
🛠️ Technologies Used
Python (NumPy, OpenCV, Matplotlib)
PyTorch (Deep Learning)
scikit-image (metrics and preprocessing)
📁 Use Case
Low-dose CT (LDCT) denoising
Medical image enhancement
Hybrid model research (DL + Deep Learning)
