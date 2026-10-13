# Object Detection using Faster R-CNN

## Overview
This project implements object detection using a pretrained **Faster R-CNN with ResNet-50 FPN** model in PyTorch. It randomly selects an image from a specified folder, detects objects, and displays the detected objects with bounding boxes, class labels, and confidence scores.

The model is pretrained on the COCO dataset and can recognize multiple common object categories, such as people, vehicles, animals, furniture, and electronic devices.

## Features
- Pretrained Faster R-CNN object detection model.
- ResNet-50 backbone with Feature Pyramid Network (FPN).
- Automatic CPU or CUDA GPU selection.
- Random image selection from a specified folder.
- Confidence threshold filtering for detections.
- Bounding box and object label visualization.
- Confidence scores displayed for detected objects.

## Technologies Used
- Python
- PyTorch
- Torchvision
- Pillow (PIL)
- OpenCV
- Matplotlib

## Requirements
Install the required libraries using pip:

```bash
pip install torch torchvision pillow matplotlib opencv-python
```

**Note:** Install compatible versions of PyTorch and Torchvision for your Python version and hardware. For GPU acceleration, ensure that your PyTorch installation supports your CUDA environment.

## Project Structure

```text
Object-Detection-Project/
├── Object Detection/
│   ├── object_detection.py
│   └── CocoaImages/
│       └── sample.jpg
├── Research Paper/
├── README.md
├── .gitignore
└── LICENSE
```

The `CocoaImages` folder contains the input images. Update the folder path in the Python script according to your system.

## How to Run

1. Clone the repository:

   ```bash
   git clone <repository-url>
   ```

2. Navigate to the project directory:

   ```bash
   cd Object-Detection
   ```

3. Install the dependencies.

4. Update the `image_folder` variable in the Python script:

   ```python
   image_folder = r"path\to\your\image\folder"
   ```

5. Run the script:

   ```bash
   python object_detection.py
   ```

The program randomly selects an image, performs object detection, and displays the output with bounding boxes, class labels, and confidence scores.

## How It Works

1. **Model Loading:** Loads a pretrained Faster R-CNN model with a ResNet-50 backbone and FPN.
2. **Image Loading:** Reads an image from the specified directory and converts it into RGB format.
3. **Preprocessing:** Converts the image into a PyTorch tensor.
4. **Object Detection:** Runs inference to predict object locations, classes, and confidence scores.
5. **Threshold Filtering:** Displays only detections whose confidence scores exceed the selected threshold (default: `0.5`).
6. **Visualization:** Uses Matplotlib to draw bounding boxes and display the predicted class labels and confidence scores.

## Model Configuration

- **Model:** Faster R-CNN
- **Backbone:** ResNet-50 with Feature Pyramid Network
- **Pretraining Dataset:** COCO
- **Default Confidence Threshold:** 0.5
- **Inference Device:** CUDA GPU when available; otherwise, CPU

## Applications
- Image analysis and object recognition.
- Traffic and vehicle detection.
- Wildlife and animal identification.
- Automated visual inspection.
- General-purpose object detection experiments.

## Limitations
- The pretrained model recognizes the object categories included in its training dataset.
- Detection accuracy depends on image quality, lighting, object size, and visibility.
- Objects outside the model's trained categories may not be detected or correctly classified.
- The current implementation processes one randomly selected image per execution.

## Future Improvements
- Process all images in the input directory.
- Save annotated images automatically.
- Add a user interface for uploading images.
- Fine-tune the model on a custom dataset for specialized object detection tasks.
- Add configurable confidence thresholds and detection summaries.

## License
This project is intended for educational and experimental purposes. Check the applicable licenses for the pretrained model and its dependencies before redistributing them.

## Author
Om Jangam
