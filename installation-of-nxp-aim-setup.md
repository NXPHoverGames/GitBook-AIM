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

### Notice

{% hint style="warning" %}
It is advised to have a steady internet collection and system to be plugged onto power as installation and setting up the setup will take a long time to finish. We also advise you to perform this installation on a clean Ubuntu 22.04 installation.
{% endhint %}

### Steps for Ubuntu 22.04 setup
Steps to setup ubuntu are described in the attached PPT below. Both methods for dual boot and only ubuntu BIOS are mentioned below:

{% file src=".gitbook/assets/AIM_2024/AIM_installation_guide.pptx" %}
Ubuntu 22.04 installation
{% endfile %}

{% hint style="danger" %} The slides are made in reference for ubuntu ver 20.04, but same steps apply for latest versions as well. {% endhint %}

# Setting up SSH keys

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

![](<.gitbook/assets/AIM_2024/ssh_key_gen.PNG>)

Once you've done this, you're ready to begin the installation.

# Installing the Setup

Install the following package which contains a python installation script to be used in next steps.

{% file src=".gitbook/assets/AIM_2024/AIM_S3_Installation.zip" %}
AIM 2024 installation setup
{% endfile %}

### Python version check
You can check your python version by using the following command:

```
$ python3 --version
```

The output should be something like this:

![](<.gitbook/assets/AIM_2024/pic1.PNG>)

If python version is 3.11 or greater than 3.11, make sure to run the following command:
```
$ sudo rm /usr/lib/python3.11/EXTERNALLY-MANAGED
```
(Note: Replace the python3.11 with you installed version. For example, if your installed version is 3.12.06, the you should
write python3.12)

## Running the Installation Script

To run the installation script follow the steps below:
1. Install streamlit
```
$ sudo pip install streamlit
```
2. Navigate to the folder where you have downloaded the installation script
3. Run the following command
```
$ streamlit run AIM_S3_Install_Script.py
```

On running this command, if it asks for your email, you can skip that by just pressing enter.
After that the following should be opened on your default browser:

![](<.gitbook/assets/AIM_2024/pic2.PNG>)

{% hint style="info" %} If the above page does not open on its own, you can go to your default web browser and paste this: {% endhint %}
```
$ localhost:8051
```
4. Enter your device usename and password
![](<.gitbook/assets/AIM_2024/password.PNG>)

{% hint style="warning" %} Make sure to check that username and password have been entered before executing any SET {% endhint %}

### Step-1
Execute SET 1 commands by pressing the **Sart Installation (SET 1)** button
Wait for the script to run. After the script has been run, the following can be seen:

![](<.gitbook/assets/AIM_2024/step1.PNG>)

The progress and the outcome can also be verified from the terminal on which you ran the ‘streamlit run …’ command.
The output will be something like:

![](<.gitbook/assets/AIM_2024/step1.png>)

** After runing SET 1, please restart your device. **

{% hint style="warning" %} If SET 1 fails, you can manually follow SET 1 steps from this link:
https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debians.html {% endhint %}

### Step-2

Now, after restart, again go the directory where you downloaded the installation script and run the __‘streamlit run …’__
command again.
Now the **Start Installation (SET 2)** button should be enabled

![](<.gitbook/assets/AIM_2024/step1.PNG>)

Once again enter your username and password and press the **Start Installation (SET 2)** button.
Now wait for some time till the commands ran successfully message pops up

![](<.gitbook/assets/AIM_2024/step3.PNG>)

Now wait for a pop-up terminal window to open…
**Enter 1, to choose the airy release**

![](<.gitbook/assets/AIM_2024/step3_airy.PNG>)

**Again Enter 1, to choose native installer**

![](<.gitbook/assets/AIM_2024/step3_native.PNG>)

**Enter your device password**

![](<.gitbook/assets/AIM_2024/step3_password.PNG>)

**Enter y, when asked to clone repositories with git using already setup github ssh keys**

![](<.gitbook/assets/AIM_2024/step3_y.PNG>)

**Enter yes, when asked if you are sure you want to continue connecting**

![](<.gitbook/assets/AIM_2024/step3_y2.PNG>)

This will take some time to download and install. After successfully running, the terminal will automatically close and you will be notified with following on main terminal:

![](<.gitbook/assets/AIM_2024/step2.png>)

Now run the following command in a seperate terminal:

```
$ source ~/.bashrc
```

{% hint style="info" %} After successful Installation there should be a folder named cognipilot in the home directory and the ~/cognipilot/ directory should look like this: {% endhint %}

![](<.gitbook/assets/AIM_2024/step3_folder.PNG>)

**Now please restart your device.**

### Step-3

Now the **Start Installation (SET 3)** button should be enabled

![](<.gitbook/assets/AIM_2024/step3.PNG>)

Once again enter your username and password and press the **Start Installation (SET 3)** button.
Now wait for some time till the commands ran successfully message pops up. __**This may take some time (upto 10 mins) depending on your device configurations.**__

![](<.gitbook/assets/AIM_2024/step3_1.png>)

![](<.gitbook/assets/AIM_2024/step3_2.png>)

{% hint style="info" %} After running SET 3, the directory structure inside the ~/cognipilot/ folder should look like the following: {% endhint %}

![](<.gitbook/assets/AIM_2024/step3_last_dic.PNG>)

{% hint style="warning" %}If SET 3 fails multiple times, or if the directory structure does not resemble the picture above, restart your device and run the following command on terminal after restart: {% endhint %}

![](<.gitbook/assets/AIM_2024/step3_last_dic.PNG>)

```
$ build_workdpace
```

**Now please restart your device.**

### Step-4

Now the **Start Installation (SET 4)** button should be enabled.

![](<.gitbook/assets/AIM_2024/step4.PNG>)

Once again enter your username and password and press the **Start Installation (SET 4)** button.
Now wait for some time till the commands ran successfully message pops up:

![](<.gitbook/assets/AIM_2024/step4.png>)

**Now please restart your device.**

### Step-5

1. Download the file from the following link:

https://396338415-files.gitbook.io/~/files/v0/b/gitbook-xprod.
appspot.com/o/spaces%2FU93yDWZcgjXGgsC1Duqv%2Fuploads%2FlOvM24532lSgdGTQmH49%2Fupdate_repo
alt=media&token=dce08eda-26f1-440e-8ca7-cf8ac297b1d4

2. Rename the file as: __**update_repos_native.sh**__
3. Save the file in the following directory: __**~/cognipilot/**__
4. Run the following commands in a new terminal

![](<.gitbook/assets/AIM_2024/step5_1.png>)

```
$ cd ~/cognipilot
$ chmod +x update_repos_native.sh
$ ./update_repos_native.sh
```

Close this terminal and now run SET 5 of installation script, which should be enabled now:

![](<.gitbook/assets/AIM_2024/step5.PNG>)

Once again enter your username and password and press the **Start Installation (SET 5)** button.
Now wait for some time till the commands ran successfully message pops up.This may take some time (upto 10 mins) depending on your device configurations.

![](<.gitbook/assets/AIM_2024/step5_2.png>)

**Now please restart your device.**

### Step-6

Now the **Start Installation (SET 6)** button should be enabled.

![](<.gitbook/assets/AIM_2024/step6.PNG>)

Once again enter your username and password and press the Start Installation (SET 6) button.
Now wait for some time till the commands ran successfully message pops up:

![](<.gitbook/assets/AIM_2024/stepdone.PNG>)

![](<.gitbook/assets/AIM_2024/step6_1.png>)

__**Congratulations, you are done with the Install and Setup!**__
