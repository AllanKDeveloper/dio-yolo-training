# YOLOv4 Object Detection with COCO Dataset

This repository demonstrates how to use YOLOv4 (You Only Look Once v4) for real-time object detection using the COCO dataset. The model predicts objects in images by identifying bounding boxes and class labels. YOLOv4 is fast, accurate, and highly suitable for deployment in various computer vision applications.

## Prerequisites

- Darknet framework for YOLOv4 (https://github.com/AlexeyAB/darknet)
- COCO dataset (for training)
- YOLOv4 configuration (`yolov4.cfg`) and pretrained weights (`yolov4.weights`)

## Getting Started

1. **Clone the repository** (if necessary)
   ```bash
   git clone https://github.com/your-username/yolov4-coco-detection.git
   cd yolov4-coco-detection
   ```

2. **Set up Darknet** (if not set up already)
   Follow the instructions to install Darknet and configure it for YOLOv4 detection.

3. **Download the YOLOv4 weights**
   You can download the pretrained YOLOv4 weights from the official YOLO website:
   ```bash
   wget https://pjreddie.com/media/files/yolov4.weights
   ```

4. **Testing the Model**
   You can test the model on your own images using the following command. This runs YOLOv4 object detection on the test image and shows predictions.

   ```bash
   ./darknet detector test cfg/coco.data cfg/yolov4.cfg yolov4.weights /content/darknet/data/test2.jpg
   ```

   This command loads the YOLOv4 configuration file (`yolov4.cfg`), the COCO dataset info (`coco.data`), and the trained weights (`yolov4.weights`), then makes predictions on the input image (`test2.jpg`). The output will be saved as `predictions.jpg`.

5. **Visualizing the Results**
   After running the command, you can visualize the prediction results by loading and showing the saved image:

   ```python
   imShow('predictions.jpg')
   ```

   This will display the image with the predicted bounding boxes and class labels.

## Code Example

```bash
# Run YOLOv4 object detection on an image using COCO dataset and YOLOv4 weights
./darknet detector test cfg/coco.data cfg/yolov4.cfg yolov4.weights /content/darknet/data/test2.jpg

# Display the predicted image with bounding boxes
imShow('predictions.jpg')
```

## Outputs

- **Predictions**: The output image (`predictions.jpg`) will display detected objects with bounding boxes and class labels.
- **Performance**: YOLOv4 provides fast predictions with high accuracy, suitable for real-time applications.
  
![sample](https://github.com/user-attachments/assets/653a89cb-ddc8-49e2-a41f-0b21156931bf)

