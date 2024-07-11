# Running NXP Gazebo

## Booting up Gazebo

Once you've installed the NXP Gazebo stack, you can move on to running the example code provided in aim\_line\_follow to self-drive the car around a simple track. At the end of the "Installation of NXP Gazebo" guide, we ran a command in our terminal that booted up the stack. As a reminder, here's the command:

```
$ ros2 launch sim_gazebo_bringup sim_gazebo.launch.py
```

When you run this command, you should see that the Gazebo simulation is booted up, and a QT viewer window showing the simulated pixy camera output (from simulation environment) is opened. Here's what it looks like:

![](<.gitbook/assets/AIM_S2/Screenshot from 2021-04-06 17-30-44.png>)

After about a 5 second delay, the car will start running the `aim_line_follow` ROS node automatically. It is your job as AIM participants to enhance the `aim_line_follow` node!

