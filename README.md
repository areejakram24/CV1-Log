# CV1-Log[README.md](https://github.com/user-attachments/files/23388309/README.md)
# YOLOv11 Object Detection and Segmentation

A computer vision project utilizing pre-trained YOLO (You Only Look Once) models for object detection and segmentation on photos and video streams. This repository tracks the setup, configuration, and progress of using pretrained yolo models for solving real-world problems in Vision domain.

----------------------------------------------------

## Tasks

* **Task 1:** Set-up virtual environment and install ultralytics. Implement **Object Detection and Segmentation** using YOLOv11n and YOLOv11-seg for specific object types, e.g., cars, pedestrians, buses.
* **Task 2:** Implement **Object Detection and Segmentation** using YOLOv11n and YOLOv11-seg on multiple in a single program and evaluate performance metrics. 
* **Task 3:** Create **multiple images** from video clip and implement **Object Detection and Segmentation** on the frames and sitch them back into a clip.

------------------------------------------------------

## Getting Started

Follow these steps to set up the project environment and run the models.

### 1. Prerequisites

You need the following software installed:

**Python 3.13.3**

### 2. Environment Setup

It is highly recommended to use a Python virtual environment (`venv`).

```bash
# Create a new directory for the project
mkdir projai
cd projai

# Create the virtual environment
python3 -m venv projai

# Activate the virtual environment
source projai/bin/activate  # On Linux/macOS

#Install ultralytics and get Git
pip install ultralytics
git clone https://github.com/ultralytics/ultralytics.git
pip3 install torch torchvision

#Install ffmpeg 
brew instal ffmpeg

```

Docs:

https://docs.python.org/3/library/venv.html

https://docs.ultralytics.com/quickstart/

