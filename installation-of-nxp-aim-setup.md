---
description: Guide to install setup for NXP AIM CUP CHALLENGE.
---
To run Gazebo you will need an Ubuntu Linux (22.04) environment. You can run the Ubuntu as a native OS or as a virtual machine. Recommended specs for running the Gazebo simulation environment are as follows:

| Component       | Amount                                   |
| --------------- | ---------------------------------------- |
| Processor       | Any modern quad-core processor or better |
| RAM             | 8GB of RAM or better                     |
| Hard Disk Space | \~20GB of space (SSD recommended)        |

# Installation of Ubuntu 22.04

## Notice

{% hint style="warning" %}
It is advised to have a steady internet collection and system to be plugged onto power as installation and setting up the setup will take a long time to finish. We also advise you to perform this installation on a clean Ubuntu 22.04 installation.
{% endhint %}

## Steps for Ubuntu 22.04 setup
Steps to setup ubuntu are described in the attached PPT below. Both methods for dual boot and are mentioned below:

![](<.gitbook/assets/AIM_S2/NXP AIM installation guide.pptx>)

## Setting up SSH keys

{% hint style="info" %}
To use NXP Gazebo, you will need to have a GitHub account. The installation scripts require a GitHub account with an SSH key.
{% endhint %}

### Creating an SSH key

To create an SSH key, run the following in a terminal:

```
$ ssh-keygen
```

Follow the prompt. We suggest just pressing enter until you reach the end. It will be easier if you just use the default path for the id\_rsa file and if you go without a passphrase (though you're welcome to use one!). You should get the output below. Note that the RSA key is not shown here for security reasons:

![](<.gitbook/assets/AIM_S2/image (10).png>)

Next, you'll want to install `xclip`. This program will allow you to copy the contents of the id\_rsa.pub file to your clipboard so you can paste it into GitHub. To install `xclip`, run the following command:

```
$ sudo apt install xclip git
```

Once you've installed xclip, you need to copy the id\_rsa.pub file to your clipboard. To do so, run the following command:

```
$ xclip -sel clip < ~/.ssh/id_rsa.pub
```

### Adding your SSH key to GitHub

Now, log into your GitHub account and paste your SSH key. The SSH key field is located in your account settings under "SSH and GPG keys". Add a new SSH key by pressing "New SSH key" and pasting your SSH key in the box. Make sure to give it a name!

![](<.gitbook/assets/AIM_S2/image (1).png>)

Once you've done this, you're ready to begin the installation.

## Installing Software Stack
```
$ cd ~/ros2ws
$ colcon build --packages-select sim_gazebo_bringup --symlink-install
$ echo "source /home/$USER/ros2ws/install/setup.bash" >> ~/.bashrc
$ source ~/.bashrc
```

![](<.gitbook/assets/AIM_S2/Screenshot from 2021-04-07 00-26-31.png>)

Now that we have the bringup package set up, we can start installing all of the NXP Gazebo packages. Run the following command:

```
$ ros2 launch sim_gazebo_bringup sim_gazebo.launch.py
```

{% hint style="warning" %}
After running the above command you will be asked to run few commands a shown in the image. Copy them and run them before moving to next step of installation​
{% endhint %}

![](<.gitbook/assets/AIM_S2/Screenshot from 2021-04-07 00-33-42.png>)

You've now installed NXP Gazebo! You can now move on to the next sections to continue.
