## English Description

[中文文档](README_CN.md) | English

### Dataset Overview

This is a computer vision dataset for rebar detection and counting. The dataset contains images of rebars from construction sites along with corresponding annotation information, which can be used to train object detection models for automatic rebar identification and counting.

### Dataset Details

- **Number of Images**: 250 images
- **Number of Annotations**: 250 YOLO format files + 2 V50OC format files
- **Number of Classes**: 1 class (rebar)
- **Image Format**: JPG
- **Annotation Formats**:
  - YOLO format (.txt): Normalized bounding box coordinates
  - PASCAL VOC format (.xml): Absolute pixel coordinates for bounding boxes

### Annotation Format Description

#### YOLO Format (labels/*.txt)

Each line contains annotation information for one object:

class_id center_x center_y width height

- `class_id`: Class ID (0 for rebar)
- `center_x, center_y`: Normalized coordinates of bounding box center (0-1)
- `width, height`: Normalized width and height of bounding box (0-1)

#### PASCAL VOC Format (Annotations/*.xml)

XML format contains detailed annotation information:

- Image dimension information
- Bounding box coordinates for each object (absolute pixel values)
- Object class names
- Other attributes (pose, truncated, difficult, etc.)

### Usage Recommendations

1. **Object Detection**: Use YOLO, SSD, Faster R-CNN and other models for rebar detection
2. **Instance Segmentation**: Can be extended for precise rebar segmentation tasks
3. **Counting Applications**: Combine detection results for automatic rebar counting
4. **Data Augmentation**: Recommend using rotation, scaling, color transformation and other augmentation techniques
