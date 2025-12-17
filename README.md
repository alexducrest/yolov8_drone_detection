# YOLOv8 Drone Recognition

A computer vision project for detecting and recognizing drones in images using YOLOv8. This project is in its early stages and focuses on dataset exploration, analysis, and preparation for training a YOLOv8 object detection model.

## Overview

This project aims to develop an image detection algorithm capable of identifying drones in various scenarios. The dataset includes multiple object classes:
- **Drone** (primary focus)
- **Helicopter**
- **Airplane**
- **Bird**

## Dataset

The project uses a YOLOv8-formatted dataset with the following structure:
```
drone-detection/
├── drone-detection-new.v5-new-train.yolov8/
│   ├── train/
│   │   ├── images/
│   │   └── labels/
│   ├── valid/
│   │   ├── images/
│   │   └── labels/
│   ├── test/
│   │   ├── images/
│   │   └── labels/
│   └── data.yaml
```

### Dataset Statistics

Based on the analysis in the notebook:
- **Total files**: ~48,005
- **Image files**: ~35,994
- **Label files**: ~12,004

**Images per category (across all splits)**:
- Drone: 4,728 images
- Airplane: 2,535 images
- Helicopter: 2,523 images

## Features

The `image_detection.ipynb` notebook includes:

1. **Dataset Exploration**
   - File counting and categorization
   - Analysis of dataset splits (train/valid/test)
   - Category distribution analysis

2. **Dataset Analysis**
   - YOLOv8 format validation
   - Class ID mapping verification
   - Image-label pairing verification

3. **Video Frame Processing**
   - Extraction and organization of video frames
   - Frame counting per video sequence

4. **Dataset Filtering**
   - Creation of drone-only dataset subsets
   - Parallel processing for efficient data extraction

5. **Visualization Tools**
   - Interactive image browser
   - Grid display of sample images

## Requirements

To run this notebook, you'll need:

```python
# Core dependencies
- Python 3.x
- PyYAML
- Pillow (PIL)
- matplotlib
- ipywidgets
- tqdm
- Jupyter Notebook or JupyterLab
```

## Usage

1. **Setup**: Ensure your dataset is available at the specified path (default: `/kaggle/input/drone-detection`)

2. **Run the Notebook**: Execute cells sequentially in `image_detection.ipynb`

3. **Customize Paths**: Update the `root_dir` variable in the notebook cells to match your dataset location

## Project Status

This is the beginning of the image detection algorithm project. Current focus:
- Dataset exploration and analysis
- Dataset statistics and validation
- Data preprocessing and filtering
- Model training (upcoming)
- Inference and evaluation (upcoming)

## Future Work

- [ ] Train YOLOv8 model on the prepared dataset
- [ ] Implement model evaluation metrics
- [ ] Create inference pipeline for real-time detection
- [ ] Optimize model performance
- [ ] Add data augmentation strategies
- [ ] Implement model deployment solution

## Notes

- The notebook is designed to work with Kaggle datasets but can be adapted for local use
- Path configurations may need adjustment based on your environment
- The dataset uses YOLOv8 format with normalized bounding box coordinates

