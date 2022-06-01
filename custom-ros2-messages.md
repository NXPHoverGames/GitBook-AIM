# Custom ROS2 Messages

{% hint style="danger" %}
The guidelines regarding custom messages should be followed strictly!&#x20;
{% endhint %}

Teams will be required to create their own custom ROS2 messages to send necessary new data to aim\_line\_follow.py file to improve their self-driving algorithm and include all new changes. There is a fixed dedicated format for these messages that all teams must follow strictly:

Name of message package: **nxp\_aim\_interfaces**

Message file name: **NxpAim.msg**

Structure of variables in .msg file:

```
{datatype}  {TeamName}_{variableName}
```

eg: int64 teamDemo\_infoData1

{% hint style="info" %}
PARTICIPANTS MUST DO NECESSARY CHANGES IN package.xml OF ALL NECESSARY \~/ros2ws/src/ SUB\_FOLDERS
{% endhint %}

Tutorial and guide to make custom messages in ROS 2 Foxy: [http://docs.ros.org.ros.informatik.uni-freiburg.de/en/foxy/Tutorials/Custom-ROS2-Interfaces.html](http://docs.ros.org.ros.informatik.uni-freiburg.de/en/foxy/Tutorials/Custom-ROS2-Interfaces.html)
