---
description: >-
  This page explains the overview and features of the self driving code provided
  in aim_line_follow.py
---

# Overview of Example Code

Inside of `aim_line_follow.py`, there is a function that receives vector information from the simulated Pixy camera and returns speed and steer values. The vector information is received through nxp\_cup\_interfaces that contains the PixyVector message and is nearly identical to the vector information sent by the Pixy over I2C.&#x20;

The source code uses a simple algorithm to extract speed and steer values from the supplied vector data to drive the car. We expect contestants to improve upon this algorithm and show us how fast their simulated NXP Cup car can go!&#x20;

## Key Components

### Important Variables and Functions

There are several important variables and functions that are used in the code. A key description of them is given below:

|    Variable/Function   |                                                                        Purpose                                                                        |
| :--------------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------: |
|       PixyVector       |  It is imported from "nxp\_cup_interfaces.msg" library. It contains information of pixy vectors obtained from Pixy Camera from nxp\_track\_vision.py_ |
|    _\_\_init_\_\_()    |                               Initialization function for LineFollow class. The code in this function may not be edited                               |
|    self.start\_time    |                                                  A custom timer corresponding to the simulation timer                                                 |
|   self.restart\_time   |                                                It is used when no vectors are found to start the timer                                                |
|  self.linear\_velocity |                            The class variable that will store the linear velocity by which the car will move in simulation                            |
| self.angular\_velocity |                              The Class variable will store the angular velocity by which the car will steer in simulation                             |
|   self.speed\_vector   |              Class variable to convert self.linear\_velocity into Vector3() object, which is suitable for message transferring to Gazebo              |
|   self.steer\_vector   |              Class variable to convert self.angular\_velocity into Vector3() object, which is suitable for message transferring to Gazebo             |
|      self.cmd\_vel     |             Variable that stores speed and steer information together and pass this information via messages for the nxp-cup car to move              |
|   get\_num\_vectors()  |                  Class method to calculate the number/s of Pixy Vectors obtained. The output of this function will be 0,1 or 2 only.                  |
|  listener\_callback()  |                Class method where all the necessary algorithms are applied to calculate linear velocity and steer for the nxp-cup car.                |
|      frame\_width      |                                          Frame width of QT viewer showing the output of simulated Pixy Camera                                         |
|      frame\_height     |                                         Frame height of QT viewer showing the output of simulated Pixy Camera                                         |
|      current\_time     | Get current time using datetime() library. This along with self.start\_time is used to calculate the time difference at ant given point of simulation |

### Data Structure of PixyVector

This data structure contains the head and tail points of two vectors from the simulated pixy camera.

The two vectors are defined by **msg.m0\_** __ and _ **msg.m1**_**\_.**&#x20;

```
# Vector 0 head and tail points
msg.m0_x0    # Tail of vector @ x cordinate
msg.m0_y0    # Tail of vector @ y cordinate
msg.m0_x1    # Head of vector @ x cordinate
msg.m0_y1    # Head of vector @ y cordinate

# Vector 1 head and tail points
msg.m1_x0    # Tail of vector @ x cordinate
msg.m1_y0    # Tail of vector @ y cordinate
msg.m1_x1    # Head of vector @ x cordinate
msg.m1_y1    # Head of vector @ y cordinate
```

## If-Else Block

The if-else block statements within `listener_callback()` performs different instructions depending on how many vectors are found.&#x20;

### Case: 0 vectors found

If no vectors are found (case 0), then a timer will start and tell the vehicle to stop after a certain amount of time

### Case: 1 vector found

If one vector is found, the algorithm finds the gradient of the vector and stores that in `steer`, and the `speed`

### Case: 2 vectors found

If two vectors are found, then the example algorithm will find the offset in the x direction of the average of the two head points of each vector. This will give us a steering value that will steer the cup car in the correct direction. This value is stored in `steer`. The speed value will be calculated and is stored in `speed`.
