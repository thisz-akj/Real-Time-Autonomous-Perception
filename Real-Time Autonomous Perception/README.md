# Real-Time Autonomous Perception for robots

### YOLOv8 + DeepSORT + Custom Color Dataset

### This project implements a real-time object detection and tracking system using:

-YOLOv8 (Ultralytics) for fast, accurate object detection

-DeepSORT for multi-object identity tracking

-MARS appearance embeddings for robust ID assignment

-A custom dataset of colored objects annotated in CVAT

-This pipeline is designed for robotics, autonomous systems, and real-world perception tasks, where reliable, ID-consistent tracking is essential.

 ## Features

✔ Custom YOLOv8 detection model (trained on your dataset)

✔ DeepSORT tracker upgraded for TensorFlow 2.x

✔ MARS appearance model (mars-small128.pb) integration

✔ Supports video input, image input, and webcam

✔ Saves an annotated output video with unique track IDs

✔ Fully reproducible pipeline — dataset → training → tracking

## Repository Structure

<img width="581" height="194" alt="image" src="https://github.com/user-attachments/assets/db8ddd61-8d16-44ad-8616-a9416d9699c3" />

## Dataset Description

This project uses a self-created dataset of colored objects (Red, Blue, Yellow).
Images were captured in various environments to improve real-world robustness.

## Dataset Preparation Steps

-Collected ~80 images containing colored samples

-Annotated using CVAT with bounding boxes

-Exported annotations in CVAT XML format

-Converted XML → YOLOv8 TXT labels via custom Python script

-Split into train (80%) + val (20%) folders

-Generated dataset.yaml for YOLOv8

Dataset -> https://drive.google.com/drive/folders/1f98Opw2vio1RhRVv7_a1CLyEHTJnzZ2Y?usp=sharing

## System Architecture

<img width="402" height="481" alt="image" src="https://github.com/user-attachments/assets/c1e21bcd-4b93-4078-a61d-3a175fca79c6" />

## How to Use
1. Run the Notebook (Recommended)

### Open Detection.ipynb:

#### It includes:

Dataset preprocessing

YOLO training

YOLO inference

DeepSORT tracking

Output video generation

### Train YOLOv8 on Your Dataset

### Run YOLO Inference (Detection Only)

### Run Object Tracking (YOLO + DeepSORT)

### The output video will contain:

-Bounding boxes

-Class labels

-Persistent object IDs

-Tracking lines


