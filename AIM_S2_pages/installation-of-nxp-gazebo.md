---
description: Guide to install setup for NXP AIM CUP CHALLENGE.
---

# Installation of NXP Gazebo

## Notice

{% hint style="warning" %}
It is advised to have a steady internet collection and system to be plugged onto power as installation and setting up the setup will take a long time to finish. We also advise you to perform this installation on a clean Ubuntu 20.04 installation. If you have previously installed ROS1 Noetic, there may be issues with installation and we advise uninstalling it for the sake of compatibility with NXP Gazebo.
{% endhint %}

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

## Installing ROS2

To run NXP Gazebo, you must have ROS2 installed. This is an easy process - just run the following script:

{% file src=".gitbook/assets/AIM_S2/foxy_install_aim (1).sh" %}
foxy\_install\_aim.sh
{% endfile %}

Now, we will need to run the `foxy_install_aim.sh` file to set up our software. To start, run the following commands:

```
$ cd ~/Downloads
$ chmod a+x foxy_install_aim.sh
$ ./foxy_install_aim.sh
```

{% hint style="warning" %}
Note: This command will take a long time to finish since it is installing ROS2. It will show that it successfully installed by printing `DONE` once the script finishes.
{% endhint %}

And then source your `.bashrc` by running the following command:

```
$ source ~/.bashrc
```

## Installing NXP Gazebo <a href="#installing-nxp-gazebo" id="installing-nxp-gazebo"></a>

### Cloning and running sim\_gazebo\_bringup

Installing NXP Gazebo has become much easier over time. With this new install process, you'll be up and running with NXP Gazebo in record time!

First, we need to create a ROS2 workspace directory to store the installation files. Go to your home folder and create a new folder called "ros2ws", and a folder inside of that called "src":

```
$ cd ~
$ mkdir -p ros2ws/src && cd ros2ws/src
```

Once you are in the directory `~/ros2ws/src`, it's time to clone the bringup repo. The bringup repo contains code that sets up the workspace for you automatically. To clone it, run the following command:

```
$ git clone git@github.com:rudislabs/sim_gazebo_bringup.git -b aim
```

When git prompts you to continue connecting with your RSA fingerprint, type yes:

![](<.gitbook/assets/AIM_S2/image (7).png>)

Next, we are going to run `sim_gazebo_bringup`. To do this, run the following commands:

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
