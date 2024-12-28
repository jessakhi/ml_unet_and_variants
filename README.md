# U-Net Variants for Brain Tumor Segmentation

## Overview
This project focuses on implementing U-Net and its variants for brain tumor segmentation using the BraTS2020 dataset. The dataset consists of multimodal MRI scans and ground truth annotations for tumor regions. The objective is to leverage deep learning techniques to segment different tumor subregions effectively.

## Dataset
The dataset used is the [BraTS2020 Training Data](https://www.kaggle.com/datasets/awsaf49/brats2020-training-data), which contains:

- **T1**: Native structural imaging.
- **T1Gd**: Post-contrast imaging with Gadolinium enhancement.
- **T2**: Imaging for edema detection.
- **T2-FLAIR**: Imaging suppressing CSF signals to enhance lesion visibility.

### Tumor Annotations:
- **NCR/NET** (Label 1): Necrotic and non-enhancing tumor core.
- **ED** (Label 2): Peritumoral edema.
- **ET** (Label 4): Enhancing tumor core.

## Features
- **Preprocessing**: Loading and resizing MRI scans from NIfTI format.
- **Data Augmentation**: Using techniques like flipping, rotation, and intensity scaling.
- **Model Architectures**:
  - Basic U-Net
  - U-Net with residual blocks
  - Attention U-Net
- **Evaluation Metrics**: Dice coefficient and visual comparison of predicted and ground truth segmentations.

## Key Functions
- `dice_coeff`: Computes the Dice coefficient.
- `build_unet`: Constructs the U-Net architecture.
- `residual_block`: Adds residual connections to U-Net.
- `attention_block`: Integrates attention mechanisms.
- `plot_history`: Plots training/validation metrics over epochs.
- `predict_segmentation`: Generates predictions for a given MRI volume.
- `show_predicted_segmentations`: Visualizes predictions alongside ground truth.

## Installation
### Prerequisites
Ensure you have the following libraries installed:
- TensorFlow
- Keras
- NumPy
- Pandas
- Matplotlib
- Nibabel
- OpenCV
- scikit-image
- scikit-learn

Install dependencies using:
```bash
pip install tensorflow keras numpy pandas matplotlib nibabel opencv-python scikit-image scikit-learn
```

## Usage
1. **Dataset Preparation**:
   - Download the BraTS2020 dataset and unzip it.
   - Update paths in the notebook to point to the dataset.

2. **Training**:
   - Train the U-Net models using the provided training script.
   - Evaluate the models on validation and test sets.

3. **Visualization**:
   - Use `show_predicted_segmentations` to visualize segmentation results.

## Results
- The models achieve high Dice coefficients for segmenting tumor regions.
- Visualizations show clear delineation of NCR/NET, ED, and ET subregions.

## Files
- `Unet_de_base_et_ses_variants.ipynb`: Main notebook containing data preprocessing, model training, and evaluation.
- Pre-trained models and logs (if applicable).

## Contributing

H.MADDOUCH

## Acknowledgements

We thank the organizers of the BRAT2020 challenge for providing the dataset and resources that made this project possible.
## License
This project is licensed under the MIT License. See the `LICENSE` file for details.
---


---

Thank you for visiting our repository!
