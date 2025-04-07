# Sex Classification Using Finger Fluting Images  
### *Virtual and Tactile Image Modalities*

This repository presents the implementation of a technical study exploring the feasibility of deep learning-based sex classification using finger fluting images. The study focuses on two distinct modalities: **virtual** and **tactile** images.

---

## Dataset

The dataset consists of finger fluting images collected from two sources:

- **Virtual Images**: 92 participants (63 female, 29 male)  
- **Tactile Images**: 79 participants (56 female, 23 male)

To maximize the utility of available data, the dataset was split into **training** and **test** sets with an 80:20 ratio at the participant level.  
The dataset is publicly available at:  
[Google Drive - Finger Fluting Dataset](https://drive.google.com/drive/folders/1_CBRTB26yzQKEwfBJ-0cWzvpmC_H0SZi?usp=drive_link)

### Data Ethics and Consent

This dataset was collected under approved ethics protocol (Griffith University Ref. No. 2023/667). All participants provided informed consent for their data to be used in this and future related research.The dataset is shared exclusively for academic and non-commercial use, in compliance with Griffith University's [Privacy Plan](https://www.griffith.edu.au/about-griffith/corporate-governance/plans-publications/griffith-university-privacy-plan).

---

## Implementation

### Step 1: Data Preparation

Scripts for dataset preparation and organization are included in this repository. The data was structured into training and test sets as follows:

- **Virtual Images**: Used in raw form.  
- **Tactile Images (Cropped)**: Preprocessed and cropped using the SAM2 model to ensure consistency.  
  For detailed preprocessing steps, refer to [Implementation_steps.md](sam2_notebooks/README.md).

---

### Step 2: Model Training and Accuracy Evaluation

Deep learning models were fine-tuned on the prepared datasets to perform binary sex classification. The training pipeline follows the approach described in this [Kaggle notebook](https://www.kaggle.com/code/frozenwolf/coronahack-finetuning-resnet18-pytorch).

Two model architectures were explored:

#### 2.1 ResNet-18

- [Virtual Images (Jupyter Notebook)](Github_finetuning_resnet18_virtual_img.ipynb)  
- [Tactile Images (Jupyter Notebook)](Github_finetuning_resnet18_tactile.ipynb)

#### 2.2 EfficientNet-V2-S

- [Virtual Images (Jupyter Notebook)](Github_finetuning_efficient_net_v2s_virtual_img.ipynb)  
- [Tactile Images (Jupyter Notebook)](Github_finetuning_efficient_net_v2s_tactile.ipynb)

---

## Contact

For questions, suggestions, or collaboration inquiries, feel free to reach out.
