# Understanding the B3RB ROS LINE FOLLOWER

This folder is present at location __~/cognipilot/cranium/src_. This is the only folder that participants will need to modify and submit for regional finale.
This project contains three python scripts for a line follower application.

## b3rb_ros_edge_vectors
- <span style="background-color: #FFC0CB; font-weight:bold">b3rb_ros_edge_vectors</span>: It creates vectors on the edges of the road in front of the rover.
  - The image captured from the front camera is used for detecting edges of the road.
  - Cases based on number of vectors created:
    - 0: When neither left or right edge of the road is detected.
    - 1: When only 1 out of left or right edge of the road is detected.
    - 2: When both left and right edge of the road are detected.
      - Both the vectors's mid-point can't lie in either the left or right half.
      - One vector must lie in the left half and the other must lie in the right half.
  - The vectors are published to the topic "/edge_vectors".
    - Message type: "~/cognipilot/cranium/src/synapse_msgs/msg/EdgeVectors.msg".
  - We assume the part of road that is very close to the rover is relevant for decision making.
    - Hence, only the bottom 30% of the image is analyzed for edges of the road.
      - This threshold could be modified by changing the value of lower_image_height.
    - Hence, the y-coordinates of the vectors ∈ [30% of image height, image height].
  - Please feel free to modify this file if you feel that would improve the vector creation.
 
## b3rb_ros_line_follower
- <span style="background-color: #FFC0CB; font-weight:bold"> b3rb_ros_line_follower</span>: Contains framework for running the rover using edge vectors.
  - Write your code in the "edge_vectors_callback" function for line follower application.
    - This callback is called whenever a new set of vectors are published on "/edge_vectors".
  - Utilize "rover_move_manual_mode" for moving the rover. Refer its docstring for explanation.
  - Write your code in the "lidar_callback" function for obstacle avoidance and ramp detection.
    - This callback is called whenever a new set of data is published on "/scan".
  - Please note that this file contains a generic implementation of line follower functionality.
    - You are allowed to modify or implement a different method to improve performance.
   
## b3rb_ros_object_recog
- <span style="background-color: #FFC0CB; font-weight:bold"> b3rb_ros_object_recog</span>: Contains framework for recognizing objects on the track.
  - Write your code in the "camera_image_callback" function.

# Communication between ROS-2 nodes

The below diagram depicts how various essential ROS-2 nodes are communicating with each other:

![](<.gitbook/assets/AIM_2024/ros_graph.PNG>)
![image](https://github.com/user-attachments/assets/455c6213-0444-47f5-ab6c-cf3c397ff922)

In above graph:
  - The ovals are the nodes.
  - The rectangles are the topics.
  - The outer rectangles are namespaces of the topics.
  - The arrows represent publishers and subscriptions of nodes.
