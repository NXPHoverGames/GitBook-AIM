---
description: >-
  These updates has to be made by the participants in order to prepare for the
  final round of NXP AIM challenge
---

# Necessary Updates for Final Round

### Adding contact sensor to the car main body

The participants must add the following lines of code to enable contact sensor on the car body to determine car collision with obstacles.

To do so open _**`nxp_cupcar.sdf.jinja`**_ located at _\~/ros2ws/nxp\_gazebo/models/nxp\_cupcar_ in the software stack. Add the following lines of codes inside _link_ tag with _name=**"\{{model\_name\}}\_frame\_link"**_ below the collision sub-tag:&#x20;

```
<!--contact sensor test-->
      <sensor name="car_contact" type="contact">
        <contact>
          <collision>{{ model_name }}_frame_collision</collision>
        </contact>
        <update_rate>5</update_rate>
        <alwaysOn>true</alwaysOn>
      </sensor>
```

After the addition of this code the file must look like this:

![](.gitbook/assets/AIM_S2/add\_contact.png)

To see the output captured by the contact sensor, open a new terminal while the simulation is running and execute the following command:

```
$ gz topic -e /gazebo/canvas/sitl_nxp_cupcar_0/sitl_nxp_cupcar_0_frame_link/car_contact/contacts
```

![](.gitbook/assets/AIM_S2/terminal.png)

### Adding a new node to observe input image captured Pixy Camera (Optional)

Those who wish to visualize the input data, in this case, the image; captured by the Pixy Camera attached to the car, will have to follow the below steps.

Open _**`nxp_track_vision.py`**_ located at _\~/ros2ws/src/nxp\_cup\_vision/nxp\_cup\_vision_ in the software stack. First add the following line of code in **`__init__()`**  method function in _**NXPTrackVision**_ class definition under the _**#Publishers:**_

```
self.debugDetectionImagePub2 = self.create_publisher(sensor_msgs.msg.Image,
            '/{:s}'.format("Camera_Input"), 0)
```

![](.gitbook/assets/AIM_S2/publishers.png)

Now add another block of code in **`pixyImageCallback()`**method function under **`if self.debug:`** condition:

```
msg2=self.bridge.cv2_to_imgmsg(scene, "bgr8")
msg2.header.stamp = data.header.stamp
self.debugDetectionImagePub2.publish(msg2)
```

![](<.gitbook/assets/AIM_S2/Screenshot from 2021-06-08 12-30-08.png>)

The input image then can be visualized in the QT viewer when the simulation is running as seen in the images below:

![](.gitbook/assets/AIM_S2/input1.png)

![](.gitbook/assets/AIM_S2/Input2.png)
