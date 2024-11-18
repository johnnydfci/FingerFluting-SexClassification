# SAM2 for Cropping Tactile Images

This repository leverages the **SAM2 model** for efficiently cropping tactile images.  
The SAM2 model is adapted from the original repository: [facebookresearch/sam2](https://github.com/facebookresearch/sam2).

---

## Requirements

- **Python**: >=3.10  
- **Torch**: >=2.3.1  
- **Torchvision**: >=0.18.1  

---

## Implementation

### Step 1: Clone and Install SAM2

```bash
git clone https://github.com/facebookresearch/sam2.git && cd sam2
pip install -e . #  optional, purely using python script via command line
pip install -e ".[notebooks]" # recommended,use the SAM2 predictor and run notebooks

```


### Step 2:  run the jupytnotebook to crop and save the images. 

- [image_predictor_finger_fluting_1point.ipynb](image_predictor_finger_fluting_1point.ipynb)  (use 1 central point for input prompt)

- [image_predictor_finger_fluting_group_5_points.ipynb ](image_predictor_finger_fluting_group_5_points.ipynb)(use 5 central points for input prompt)

An original example can been seen in the google colab: https://colab.research.google.com/github/facebookresearch/sam2/blob/main/notebooks/image_predictor_example.ipynb
   
