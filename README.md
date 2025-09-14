# Evaluating the Effects of L1 and L2 Regularisation Placement in GAN Architectures

This repository contains the research project, configuration manual, and Jupyter Notebook implementation for evaluating how different placements of L1 and L2 regularisation affect the training stability and performance of GANs.  

The project systematically investigates regularisation applied to:
- **Generator output**
- **Discriminator input**
- **Generator weights**
- **Discriminator weights (early/late layers)**  

We implemented and tested both DCGAN and CGAN architectures on the CIFAR-10 dataset and evaluated performance using:
- **Fréchet Inception Distance (FID)**
- **Inception Score (IS)**
- **Training loss curves**
- **Visual inspection of generated samples**

## Repository Structure
.
├── Research_Report.pdf          # Final submitted research report
├── Configuration_Manual.pdf     # Configuration and setup guide
├── GAN_Regularization_Experiments.ipynb  # Jupyter notebook for experiments

## How to Use

1. Open the notebook:
   - You can run it locally (ensure PyTorch is installed with CUDA support if you have a GPU)  
   - Or run it on **Google Colab** (recommended for GPU access)

2. Run cells sequentially:
   - Configure experiment settings at the top of the notebook  
   - Execute training for DCGAN/CGAN variants  
   - Evaluate using FID/IS and inspect saved image samples

3. Outputs:
   - Generated images are saved every 10 epochs  
   - FID/IS scores, loss curves, and checkpoints are stored in the specified output directory

## Notes
- Training uses **CIFAR-10** (50,000 training images, normalised to [-1, 1]).  
- For CGAN, class labels are **one-hot encoded** and concatenated with noise/input images for conditional generation.  
- Regularisation strength is fixed at λL1 = 0.0001 and λL2 = 0.001 for all experiments to maintain fair comparison across placements.

## Citation
If you use this work or build upon it, please cite the report or reference this repository.
