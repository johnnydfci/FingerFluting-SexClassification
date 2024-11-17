# Sex Classification Using Finger Fluting Images  
### *Virtual and Tactile Image Modalities*

This repository contains the implementation for a technical study on the feasibility of deep learning-based sex classification using finger fluting images, focusing on **virtual** and **tactile** image modalities.


## Dataset

The dataset used in this study includes:
- **Virtual Images**: 92 participants (63 female, 29 male)
- **Tactile Images**: 79 participants (56 female, 23 male)

The dataset was split into **training** and **tuning sets** in an 8:2 ratio at the individual level to maximize utility. Due to the limited dataset size, no independent test set was utilized.

---

## Implementation

### Step 1: Data Preparation
Scripts for dataset preparation and organization are provided. The dataset was divided into training and tuning subsets as follows:
- **Virtual Images**: Raw images
- **Tactile Images (cropped)**: Tactile images were cropped using the [**SAM2 model**](https://colab.research.google.com/github/facebookresearch/sam2/blob/main/notebooks/image_predictor_example.ipynb.  ).
  - Steps for cropping tactile images:
  
  1. Provide either a single central point or five central points as the input prompt.
  2. Select the mask with the highest probability and process it as follows: Dilate the mask by 5 pixels; Perform connected component analysis to isolate the largest component.
  3. Identify the bounding box of the largest connected component.
  4. Crop the image based on the bounding box.


---

### Step 2: Model Training
Deep learning models were trained on the prepared datasets to classify sex based on the fine-tuning pipeline described in this [Kaggle notebook](https://www.kaggle.com/code/frozenwolf/coronahack-finetuning-resnet18-pytorch). The following architectures were employed:

#### 2.1 ResNet-18   [implementation in jupyter notebook](Github_finetuning_resnet18_lr0.0001_virtual_img.ipynb)
Reference:[ PyTorch ResNet-18](https://pytorch.org/vision/main/models/generated/torchvision.models.resnet18.html)

#### 2.2 EfficientNet-V2-S [implementation in jupyter notebook](Github_finetuning_efficientnetv2s_lr0.0001_virtual_img.ipynb)

Reference:[PyTorch EfficientNet-V2-S](https://pytorch.org/vision/main/models/generated/torchvision.models.efficientnet_v2_s.html)

