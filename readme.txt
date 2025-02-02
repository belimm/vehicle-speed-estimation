
Vehicular Speed Estimation

-----------||-----------||-----------||-----------||-----------||-----------||-----------||-----------||-----------

Overview

This project estimates vehicular speed using a YOLO-based object detection model and OpenCV. It utilizes the ultralytics package for YOLO and supervision for object tracking and analysis.

-----------||-----------||-----------||-----------||-----------||-----------||-----------||-----------||-----------

Installation

To set up the environment, install the required dependencies:

pip install supervision ultralytics opencv-python numpy matplotlib


-----------||-----------||-----------||-----------||-----------||-----------||-----------||-----------||-----------


How the Code Works

1-Library Imports: The script imports OpenCV for image processing, ultralytics.YOLO for vehicle detection, and supervision for tracking.

2-Model Loading: A pre-trained YOLO model is loaded to detect vehicles in video frames.

3-Object Detection: The YOLO model processes each frame, identifying vehicles and their bounding boxes.

4-Tracking & Speed Estimation:

    4.1-The script assigns unique IDs to detected vehicles.

    4.2-Vehicle positions are tracked across frames.

    4.3-Speed is estimated based on the movement of bounding boxes.

5-Visualization: Detected vehicles and their speeds are displayed on the video frames.

-----------||-----------||-----------||-----------||-----------||-----------||-----------||-----------||-----------


Running the Code

To run the notebook:

Ensure dependencies are installed.

Open the Jupyter Notebook:

jupyter notebook Vehicular_Speed_Estimation.ipynb

Execute the cells sequentially to process a video input.


-----------||-----------||-----------||-----------||-----------||-----------||-----------||-----------||-----------

Input Data

The script expects a video file as input.

Modify the input path in the OpenCV cv.VideoCapture function to use a custom video file.


-----------||-----------||-----------||-----------||-----------||-----------||-----------||-----------||-----------

Output

The processed video will display detected vehicles with speed annotations.

The model outputs speed estimations based on object movement.

-----------||-----------||-----------||-----------||-----------||-----------||-----------||-----------||-----------


Customization

To use a different YOLO model, modify the YOLO initialization:

model = YOLO('path_to_custom_model.pt')

Adjust detection thresholds and tracking parameters to improve accuracy.


-----------||-----------||-----------||-----------||-----------||-----------||-----------||-----------||-----------

Notes

The accuracy of speed estimation depends on frame rate and calibration.

Ensure the video is captured from a stable perspective for better results.

