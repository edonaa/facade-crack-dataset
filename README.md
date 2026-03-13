# Facade Crack Segmentation Dataset (FCD-108)

This repository provides the Facade Crack Segmentation Dataset (FCD-108), a small-scale dataset designed for research on thin crack detection and semantic segmentation in building façades.

The dataset was created for the study:

Krasniqi, E., & Shehu, V. (2026).
A Lightweight Distance-Aware Loss for Thin Crack Segmentation in Building Façades under Limited Data Conditions.
Journal of Future Artificial Intelligence and Technologies.

The dataset supports research in computer vision for structural inspection, damage detection, and emergency management applications.

## Dataset Description

The dataset consists of 108 building façade images with manually annotated crack segmentation masks.
Images capture thin hairline cracks and moderately thicker cracks commonly observed in exterior building surfaces.

All annotations are provided as pixel-level binary segmentation masks, where:

- 1 = crack pixel

- 0 = background

Due to the extremely thin geometry of façade cracks, crack pixels occupy only a small portion of the image area, resulting in severe class imbalance, which makes segmentation particularly challenging.
## Image Acquisition
The images were captured in Ferizaj, Kosovo, using a smartphone camera (Apple iPhone 17 Pro Max) under natural daylight conditions.

Two camera focal lengths were used depending on the distance from the façade:
- 24 mm standard camera
- 100 mm telephoto camera

The dataset includes variations in:

 - crack thickness
 - crack continuity
 - surface texture
 - local lighting and shadow conditions

These variations reflect real-world façade inspection conditions.
## Image Preprocessing

For training and evaluation purposes, all images were resized to:

- 512 × 512 pixels

Resizing ensures consistent input resolution for deep learning models such as U-Net.

### Dataset Structure
Dataset/v1/
- `train/` 
- `valid/`
  
#### Train Set

- 87 images - manually annotated crack masks

#### Validation Set

- 21 images - used for model evaluation

Masks follow the naming convention:

- image_name.jpg
- image_name_mask.png

### Annotation Process

All crack masks were manually annotated at pixel level using the Roboflow annotation tool.

Annotation guidelines included:

- labeling visible crack structures

- maintaining thin crack continuity

- excluding texture artifacts not associated with cracks

Due to the extremely thin structure of cracks, minor annotation uncertainty may exist for very faint crack segments.

## Intended Use

This dataset is intended for research in:

- crack detection
- semantic segmentation
- thin structure segmentation
- structural damage assessment
- post-disaster building inspection
- computer vision for emergency management
## Citation
If you use this dataset in your research, please cite the following paper:
@article{krasniqi2026distanceaware,
  title={A Lightweight Distance-Aware Loss for Thin Crack Segmentation in Building Façades under Limited Data Conditions},
  author={Krasniqi, Edona and Shehu, Visar},
  journal={Journal of Future Artificial Intelligence and Technologies},
  year={2026}
}

### Dataset Availability

The dataset is publicly available on Google Drive:

[Download link](https://drive.google.com/drive/folders/1JUeB9En3NkMRwucTwVmyUr0X80IndyqU?usp=drive_link)

### License
This dataset is released under the Creative Commons Attribution 4.0 International License (CC BY 4.0).
You are free to:
- use
- share
- adapt
for research and academic purposes with proper attribution.
License details:
https://creativecommons.org/licenses/by/4.0/

## Acknowledgments

This dataset was created as part of research on AI-based structural damage detection and emergency decision support systems.
