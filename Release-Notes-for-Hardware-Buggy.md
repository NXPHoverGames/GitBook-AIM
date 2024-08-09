# Release Notes for Hardware Buggy
This tutorial describes the differences in hardware buggy compared to the simulation.

## b3rb_ros_line_follower

### LIDAR
The order of reporting of the obstacles by the hardware LIDAR STL-27L is different compared to the one in simulation. This is reflected in the "ranges" variable in the "lidar_callback" function. Hence, the code for retrieving the LIDAR data corresponding to the front hemisphere is different now.
- ![alt text](.gitbook/assets/AIM_2024/lidar_callback.png)

## b3rb_ros_edge_vectors

### CAMERA
The quality of the live feed and the simulation vs physical track properties can be different for the Simulation Camera and the Hardware Camera, i.e. the images captured by OV5645 may contain noise or glitches unlike simulation camera that gives perfect images.
- Participants may need to apply image processing techniques to refine their captured image to be able to detect the edge vectors cleanly. As an example we have applied dilation while preprocessing the image for edge vectors in the function "process_image_for_edge_vectors".
- ![alt text](.gitbook/assets/AIM_2024/edge_vectors.png)

## b3rb_ros_object_recog

### YOLOv5
It provides framework for running YOLOv5 TFLITE on NXP IMX8MPLUS NPU.
- This file provides reference for running Machine Learning models on NXP hardware.
- This model recognizes objects and draws a rectangle around them to identify their position.
- For the list of objects recognized by the YOLOv5 model, refer resource/coco.yaml.
- By default, we have provided an untrained model that only recognizes the objects in coco.yaml.
  - Participants may be required to further train the default model to recognize more objects.
- Please feel free to modify this file or utilize a different model for object recognition.

## PHYSICAL CHARACTERISTICS
- Camera mounting angle significantly affects edge vector creation and object recognition. Participants could experiment with different angles to improve the overall performance.
- Buggy speed and steer should be set within the range [-1, +1] as mentioned in the docstring of the function "rover_move_manual_mode" in the node "b3rb_ros_line_follower".
  - It is advised that initial testing should be done with low speed such as 0.25, then gradually speed should be increased to improve time taken to complete lap.
