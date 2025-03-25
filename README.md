# AerialCSP Dataset

## Introduction

AerialCSP is a virtual dataset that simulates aerial imagery of Concentrated Solar Power plants. By generating
synthetic data that closely mimics real-world conditions, we aim to facilitate pretraining of models before deployment,
significantly reducing the need for extensive manual labeling.

## Dataset Overview

The process of creating the virtual dataset is outlined in the following figure:
![images](modules_of_paper.png)

The final AerialCSP dataset is created by compositing the rendered Blender images onto the inpainted backgrounds. To introduce variability, we apply random scaling and rotations to the synthetic SCE images before pasting them onto the backgrounds. These transformations are also applied to the corresponding segmentation masks to maintain annotation consistency. AerialCSP is designed to support two primary computer vision tasks:

* **Object Detection:** Each image is accompanied by a YOLO-formatted annotation file containing bounding box information. The annotation format follows `<class> <x\_center> <y\_center> <width> <height>`, where all coordinates are normalized (0 to 1), and class indices are zero-indexed.
* **Instance Segmentation:** Segmentation masks are stored in a format where each line corresponds to an object and follows `<class-index> <x$_1$> <y$_1$> <x$_2$> <y$_2$> ... <x$_n$> <y$_n$>`, where (x, y) coordinates define the polygonal mask of the object and are normalized within [0,1].

The AerialCSP dataset is publicly available at [ToDo: Insert dataset URL], facilitating research in aerial robotics and automated monitoring of CSP plants. To ensure fair comparisons, we provide a standardized dataset split into training, validation, and test sets, following a 75\%-15\%-10\% distribution. In total, AerialCSP contains 18 058 labeled images.

## Example Images

Here are a few example images from the dataset:

![Image 1](image1.jpg)
![Image 2](image2.jpg)
![Image 3](image3.jpg)

## Using the Dataset

To use the AerialCSP dataset, simply download the data from the link below and follow these steps:

1. [Step 1: Describe how to use the dataset]
2. [Step 2: Describe how to use the dataset]
3. [Step 3: Describe how to use the dataset]


## Benchmarks

Add benchmarks for bounding box detection and image segmentation using YOLOv11.

| Model           | Task                   | mAP50 (mean Average Precision) |
|-----------------|------------------------|--------------------------------|
| YOLOv11n        | Bounding Box Detection | 95.3                           |
| YOLOv11m        | Bounding Box Detection | 96.2                           |
| YOLOv11x        | Bounding Box Detection | 96.1                           |
|-----------------|------------------------|--------------------------------|
| YOLOv11n-seg    | Image Segmentation     | 70.7                           |
| YOLOv11m-seg    | Image Segmentation     | 73.2                           |
| YOLOv11x-seg    | Image Segmentation     | 73.3                           |


## Download the Dataset

You can download the AerialCSP dataset from [link to external storage].

[Link to download the dataset](https://example.com/download-link)