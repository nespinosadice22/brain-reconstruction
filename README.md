# Understanding Autism from fMRI Brain Scans using Stacked Autoencoders 

This repository contains code and experiments exploring **stacked autoencoders** on the **ABIDE neuroimaging dataset**, focusing on **T1 MPRAGE structural MRI**.  
The goal is to learn normative reconstructions from **control participants** and analyze differences when reconstructing images from individuals with **ASD**.

## Project Overview 
- **Data source**: ABIDE Preprocessed Connectomes Project (MPRAGE structural MRI).  
- **Preprocessing**:  
  - Extracted **axial slices** from NIfTI volumes, resizing to 256x256 with normalization.  
  - Constructed site-aware datasets with both **Control** and **ASD** cohorts.  
- **Models**:  
  - Stacked **autoencoders** built in TensorFlow/Keras.  
  - Dense layers with `ReLU` activations, BatchNorm and L2 regularization to stabilize training, compact latent space to enforce structure.  
  - Decoder mirrors encoder & outputs 3-channel reconstructions.  
- **Evaluation**:  
  - Compare reconstruction MSE between **Control** and **ASD** groups.  
  - Visualize average reconstructions and **difference maps**.  
  - Produce side-by-side panels of originals, reconstructions and residuals.  
- **Baseline classification**:  
  - Use **LinearSVC** and **CNNS** to run classification tasks.


Within /notebooks, 
- data_preprocessing.ipynb: Fetches/organizes ABIDE data
- autoencoders/
- 
