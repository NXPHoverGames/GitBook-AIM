---
description: >-
  A line follower project for NXP MR-B3RB (Mobile Robotics Buggy 3 Rev B) for
  participants of AIM 2024.
---

# Code Overview for AIM 2024 software stack

## HARDWARE

This software can run on the B3RB and Gazebo Simulator.

2. [Gazebo Simulator](https://gazebosim.org/home): Development and testing environment used for B3RB.
   * It's used to simulate the B3RB with it's various sensors and capabilities.
   * It's used to simulate the track with it's various challenges and obstacles.

## SOFTWARE

This project is based on the autopilot project - [CogniPilot](https://cognipilot.org/) (AIRY Release for B3RB).

* Refer the [CogniPilot AIRY Dev Guide](https://airy.cognipilot.org/) for information about it's various components.
* [Cranium](https://airy.cognipilot.org/cranium/about/): A ROS workspace that performs higher level computation for CogniPilot.
  * On the hardware B3RB, it runs on [NavQPlus](https://nxp.gitbook.io/navqplus/) board (Mission Computer).
  * On the Gazebo Simulator, it runs on the Ubuntu Linux machine.
* This project includes a ROS2 Python package that integrates into the Cranium workspace.
  * This project (b3rb\_ros\_line\_follower) should be moved to \~/cognipilot/cranium/src.
  * This is the only folder that participants would modify and submit for the regional finale.

## Understanding the B3RB ROS LINE FOLLOWER

{% hint style="info" %}
\_\*\*\~/congnipilot/cranium/src/b3rb\_ros\_line\_follower\*\*\_ is the only folder that the participants have to modify an submit for the Regional Finale
{% endhint %}

![Location where the b3rb\_ros\_line\_follower ROS package needs to be copied into (\~/congnipilot/cranium/src/).](.gitbook/assets/AIM\_2024/update\_code.png)

This project contains three python scripts which provide a framework for a line follower application.

* b3rb\_ros\_edge\_vectors: It creates vectors on the edges of the road in front of the rover.
  * The image captured from the front camera is used for detecting edges of the road.
  * Cases based on number of vectors created:
    * 0: When neither left or right edge of the road is detected.
    * 1: When only 1 out of left or right edge of the road is detected.
    * 2: When both left and right edge of the road are detected.
      * Both the vectors's mid-point can't lie in either the left or right half.
      * One vector must lie in the left half and the other must lie in the right half.
  * The vectors are published to the topic "/edge\_vectors".
    * Message type: "\~/cognipilot/cranium/src/synapse\_msgs/msg/EdgeVectors.msg".
  * We assume the part of road that is very close to the rover is relevant for decision making.
    * Hence, only the bottom 40% of the image is analyzed for edges of the road.
      * This threshold could be modified by changing the value of lower\_image\_height.
    * Hence, the y-coordinates of the vectors ∈ \[40% of image height, image height].
  * Please feel free to modify this file if you feel that would improve the vector creation.
* b3rb\_ros\_line\_follower: Contains framework for running the rover using edge vectors.
  * Write your code in the "edge\_vectors\_callback" function for line follower application.
    * This callback is called whenever a new set of vectors are published on "/edge\_vectors".
  * Utilize "rover\_move\_manual\_mode" for moving the rover. Refer its docstring for explanation.
  * Write your code in the "lidar\_callback" function for obstacle avoidance and ramp detection.
    * This callback is called whenever a new set of data is published on "/scan".
  * Please note that this file contains a generic implementation of line follower functionality.
    * You are allowed to modify or implement a different method to improve performance.
* b3rb\_ros\_object\_recog: Contains framework for recognizing objects on the track.
  * Write your code in the "camera\_image\_callback" function.

## Communication between ROS-2 nodes

The below diagram depicts how various essential ROS-2 nodes are communicating with each other:

![](.gitbook/assets/AIM\_2024/ros\_graph.PNG)

![ros-graph](https://github.com/user-attachments/assets/9fb06484-875d-4903-b2cc-4582587698bc)

In above graph:

* The ovals are the nodes.
* The rectangles are the topics.
* The outer rectangles are namespaces of the topics.
* The arrows represent publishers and subscriptions of nodes.
