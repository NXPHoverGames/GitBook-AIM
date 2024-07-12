---
description: Guide to run simulation setup for NXP AIM CHALLENGE.
---
# Running the Simulation:

To run the simulation, run the following commands in a new Terminal Window


```
$ ros2 launch b3rb_gz_bringup sil.launch.py world:=Raceway_1
```

Running this will launch the gazebo simulation as follows:

![](<.gitbook/assets/AIM_S2/gazebo_up_1.png>)

On a different terminal run the following code:

```
$ source ~/cognipilot/cranium/install/setup.bash
$ ros2 run b3rb_ros_line_follower vectors
```

On a different terminal run the following code:

```
$ source ~/cognipilot/cranium/install/setup.bash
$ ros2 run b3rb_ros_line_follower runner
```

On a different terminal run the following code:

```
$ source ~/cognipilot/cranium/install/setup.bash
$ ros2 run b3rb_ros_line_follower detect
```

__**Running the above 3 commands should make the buggy move autonomously now in simulation.*_

{% hint style="danger" %}If on execution of any __ros2 run b3rb_ros_line_follower_ gives error like below, it means that sourcing of setup.bash was unsuccesful
{% endhint %}

![](<.gitbook/assets/AIM_S2/line_follower_fail.png>)
