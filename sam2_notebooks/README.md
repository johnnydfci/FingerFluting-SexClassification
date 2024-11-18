# SAM2 to crop tactile images

  - Steps for cropping tactile images:
  
  1. Provide either a single central point or five central points as the input prompt.
  2. Select the mask with the highest probability and process it as follows: Dilate the mask by 5 pixels; Perform connected component analysis to isolate the largest component.
  3. Identify the bounding box of the largest connected component.
  4. Crop the image based on the bounding box.
