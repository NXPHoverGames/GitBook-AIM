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
