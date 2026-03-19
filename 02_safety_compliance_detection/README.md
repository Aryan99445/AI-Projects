# Safety Compliance Detection System

A real-time PPE (Personal Protective Equipment) detection system trained on construction site safety data. Detects helmets, safety vests and face masks from images, video files and webcam input and generates compliance alerts based on what gear is detected.

<br>

## How It Works

A YOLOv8 model is fine-tuned on the Construction Site Safety dataset from Roboflow. The trained model then runs inference on the input source and checks which PPE items are present or missing. A color coded alert banner is drawn on the output — green for compliant, red for violations.

<br>

## Features

- Detects helmets, safety vests and face masks
- Supports three input modes: image, video and webcam
- Real-time compliance alerts with bounding boxes
- Trained on real construction site safety data
- Exports annotated images and videos

<br>

## Tech Stack

| Tool | Purpose |
|------|---------|
| YOLOv8 (Ultralytics) | Object detection model |
| OpenCV | Image and video processing |
| Roboflow | PPE dataset |
| Matplotlib | Displaying results |

<br>

## Dataset

**Construction Site Safety** dataset from Roboflow Universe.

Classes: `hardhat`, `mask`, `safety vest`, `no-hardhat`, `no-mask`, `no-vest`, `person`

<br>

## Setup

1. Enable GPU in Google Colab — Runtime → Change runtime type → T4 GPU
2. Get a free Roboflow API key at https://app.roboflow.com
3. Open the notebook and run all cells
4. Enter your Roboflow API key when prompted
5. Wait for training to complete (~20 minutes on T4 GPU)

<br>

## Output

- Annotated image or video with bounding boxes
- Color coded alert banner — green (compliant) or red (missing PPE)
- Downloadable trained model weights (`best.pt`)
