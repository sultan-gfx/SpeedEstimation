# Car Speed Estimation Project Report

## Task Definition
The goal of this project was to develop a system capable of estimating the speed of vehicles in a video. The system uses object detection and tracking techniques, leveraging a pre-trained YOLO model, and integrates a speed estimation module to provide quantitative evaluations of vehicle motion in real-world scenarios.

## Review of Existing Solutions
Object detection and tracking have been extensively studied in computer vision. YOLO (You Only Look Once) is one of the most prominent frameworks for real-time object detection due to its speed and accuracy. Recent advancements, such as YOLOv8, enhance the performance and efficiency of object detection tasks. Existing speed estimation systems often rely on traditional image processing techniques or integrate AI models to improve accuracy. However, many of these approaches require specialized setups, such as calibrated cameras or ground truth data, which limits their generalizability.

## Solution Description
To achieve the task, the following steps were implemented:

1. **Environment Setup**:
   - Used Google Colab for development and computation.
   - Connected Google Drive to Colab for file storage.
   - Installed the `ultralytics` library to access YOLOv8 functionalities.

2. **Model and Dataset**:
   - Loaded the pre-trained YOLOv8n model trained on the COCO dataset.
   - Used a sample video containing moving vehicles as input ("Cars.mp4").

3. **Implementation**:
   - Imported required libraries: OpenCV for video processing, Ultralytics for YOLO integration, and a custom speed estimation module.
   - Defined a line of reference in the video for speed calculations.
   - Processed the video frame-by-frame, using YOLO to track objects and estimate their speeds.
   - Annotated the video frames with detected objects and their estimated speeds.

4. **Output**:
   - Generated an output video (`speed_estimation.avi`) with speed annotations.
   - Saved the YOLOv8n model file for reuse.

## Experiments and Evaluation Results
The system was tested using a video containing multiple moving vehicles. The evaluation was qualitative, as no ground truth speed data was available. Observations include:

- The system accurately detected vehicles in most frames.
- Speed estimations appeared consistent, aligning with visual expectations of vehicle movement.
- The output video provided clear visualizations of the detections and speed annotations.

### Challenges
- Frame drops occurred in some cases due to computational limitations in Google Colab.
- Variations in vehicle sizes and occlusions occasionally affected detection accuracy.

### Improvements
Future iterations could include:
- Quantitative evaluation using a dataset with labeled speed data.
- Enhancements to handle occlusions and improve detection consistency.

### Git Repository
https://github.com/sultan-gfx/SpeedEstimation

## Conclusion
This project successfully implemented a car speed estimation system using YOLOv8 and Google Colab. While the results were promising, further refinements and quantitative evaluations could enhance the system's accuracy and robustness. The output video and the developed scripts demonstrate the project's feasibility and provide a foundation for future work.
