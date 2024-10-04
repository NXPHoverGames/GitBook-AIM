### NXP AIM GRAND FINALE EVALUATION SETUP

  {% hint style="danger" %} Participanting teams that are will do the following changes will automatically be eliminated from the competition. {% endhint %}
  
- <span style="background-color: #FFC0CB; font-weight:bold"> For the evaluation of NXP AIM 2024 Grand Finale, following are the requirements from the participants -</span>
  - **REQUIREMENTS (TO BE PERFORMED ON THE NAVQPLUS)**
    - Ensure the ROS2 version is HUMBLE. (Command for checking: "echo $ROS_DISTRO".)
    - NavQPlus must have the following ROS2 environment variables configuration:
      - ROS_DOMAIN_ID=7
      - ROS_LOCALHOST_ONLY=0
      - (Note: Commands for these are added in "~/.bashrc" when setting up CogniPilot.)
    - You may refer "[github.com/NXPHoverGames/b3rb_robot/tree/nxp_aim_2024_pose_eval](https://github.com/NXPHoverGames/b3rb_robot/commit/ea44e8edda6790cf015348eb73db8cb2b5339f15)" for the following:
      - In the file "~/cognipilot/cranium/src/b3rb_robot/b3rb_bringup/launch/robot.launch.py", at line = 167:
        - Comment the following nodes from the LaunchDescription object returned in robot.launch.py:
          - nav2, corti, slam, localization.
      - In the file "~/cognipilot/cranium/src/b3rb_robot/b3rb_bringup/launch/laser.launch.py", at line = 50:
        - Set pub_rate as 4.0.
    - Comment the following lines in the "~/.bashrc" at NavQ+.
      - export RMW_IMPLEMENTATION=rmw_cyclonedds_cpp
      - export CYCLONEDDS_URI=/home/$USER/CycloneDDSConfig.xml
      - (Then, restart NavQPlus.)

  {% hint style="info" %} After above steps make sure to re-build using colcon build followed by source. {% endhint %}
    
  {% hint style="danger" %} Participants should not change cranium nodes other than the ones in ~/cognipilot/cranium/src/b3rb_ros_line_follower and ~/cognipilot/cranium/src/synapse_msgs. {% endhint %}
