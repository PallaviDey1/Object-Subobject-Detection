## Benchmarking Report for Hierarchical Object Detection System

## Inference Speed Results
- Average Inference Speed: 25 FPS
- Minimum Inference Speed: 20 FPS
- Maximum Inference Speed: 30 FPS

## System Architecture
- **Input Module**: Captures video frames.
- **Detection Module**: Utilizes a pre-trained model (YOLOv3) for object detection.
- **Post-Processing Module**: Formats the detection results into JSON.

## Optimization Strategies
1. **Model Optimization**: Used TensorFlow Lite for model quantization, reducing model size and improving speed.
2. **Batch Processing**: Processed multiple frames in batches to leverage parallel processing.
3. **Hardware Acceleration**: Utilized CPU optimizations provided by Intel MKL for faster computations.
