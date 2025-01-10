# Object-Subobject-Detection
This repository provides structured pseudocode for building an object detection system, including object-subobject relationships for enhanced detection capabilities.

## Requirements
- Python 3.x
- TensorFlow or PyTorch
- OpenCV

## Run the system:
python main.py --input <path_to_video> --output <path_to_output_json>

## System Architecture
- **Input Module**: Captures video frames.
- **Detection Module**: Utilizes a pre-trained model (YOLOv3) for object detection.
- **Post-Processing Module**: Formats the detection results into JSON.

## Optimization Strategies
1. **Model Optimization**: 
   - Used TensorFlow Lite for model quantization, reducing model size and improving speed.
2. **Batch Processing**: 
   - Processed multiple frames in batches to leverage parallel processing.
3. **Hardware Acceleration**: 
   - Utilized CPU optimizations provided by Intel MKL for faster computations.
   - 
![Uploading YOLO.jpg…]()
