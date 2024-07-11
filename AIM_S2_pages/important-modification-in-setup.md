# Important Modification in Setup

The participants are required to do the following code changes mentioned below.

{% hint style="info" %}
These changes will help to improve your algorithm working and now there will be less variation in simulation outputs
{% endhint %}

### Change one:&#x20;

The first change is to be done in _**gen\_params.json**_ located at: _**`~/ros2ws/src/sim_gazebo_bringup/config`**_

You need to delete the following lines of code as shown in the image below:

![](<.gitbook/assets/AIM_S2/before para.png>)

After deletion your file must look like this:

![](<.gitbook/assets/AIM_S2/Screenshot from 2021-04-30 12-50-15.png>)



## Change two:

For the second change navigate to _**aim\_line\_follow.py**_ located at: _**`~/ros2ws/src/aim_line_follow/aim_line_follow`**_

You need to delete the following lines of code that are selected below image:

![](.gitbook/assets/AIM_S2/aim.png)

After deletion, write the lines 24- 32 as shown in the image below:

![](.gitbook/assets/AIM_S2/after\_aim.png)

{% hint style="danger" %}
Please note that the values of self.linear\__velocity , self.angular\_velocity and self.single\_linear\__steer\_scale must be of **float() type** \[example: 1.0, 1.2, 0.9, -1.0, -0.8 etc]
{% endhint %}
