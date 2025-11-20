# Realtime Autonomous Perceptron- Object Detection & Multi-Object Tracking Using YOLOv8 + DeepSORT

(Professional, resume-ready project description)

Built a real-time perception pipeline combining YOLOv8 for object detection and an updated DeepSORT tracker for multi-object identity tracking. Designed the full workflow end-to-end—from dataset creation to real-time inference—while modernizing legacy DeepSORT code for TensorFlow 2.x compatibility.

Key Contributions

Custom Dataset Creation & Annotation:
Collected 80+ images across varied lighting/backgrounds, annotated using CVAT, and built a complete preprocessing pipeline (XML → YOLO format) with automated train/val splits and dataset YAML generation.

Model Training & Optimization:
Trained a custom YOLOv8 model using Ultralytics, achieving robust color-object detection with high mAP scores. Implemented early-stopping, evaluation curves, and confusion-matrix analysis to validate performance.

DeepSORT Modernization (TensorFlow 2.x):
Refactored multiple outdated modules (linear assignment, session-based execution, SciPy API changes) to ensure compatibility with TF 2.x. Fixed:

sklearn.utils.linear_assignment_ removal

SciPy’s updated linear_sum_assignment return format

Deprecated tf.Session() issues by enabling TF1-compat mode
Result: a fully functional, updated DeepSORT pipeline.

Appearance Embedding Integration:
Integrated the MARS appearance encoder for generating robust feature embeddings, enabling identity-preserving tracking during occlusion, motion, and re-entry events.

Real-Time Video Tracking Pipeline:
Engineered an end-to-end inference system that:

Runs YOLOv8 frame-by-frame

Filters detections by confidence

Converts YOLO boxes into DeepSORT format

Updates tracks using Kalman filtering + cosine-distance matching

Assigns stable, unique IDs with per-track visualizations

Optimized I/O & Visualization:
Implemented color-coded bounding boxes, ID overlays, and class-count summaries. Output is written as a fully processed annotated video via OpenCV.

Technical Stack

YOLOv8, DeepSORT, TensorFlow 2.x, OpenCV, NumPy, SciPy, CVAT, Google Colab, Python

Outcome

Delivered a real-time, identity-consistent perception system capable of detecting and tracking objects robustly even under occlusion or cluttered scenes—mirroring the perception behavior required in robotics, autonomous navigation, and real-world CV applications.
