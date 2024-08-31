# Moving the buggy with manual mode

## Installing Manual Joystick Mode on Foxglove

**Step 1:** Make sure you have installed foxglove on your linux/windows system

**Step 2:** Go to the following link:
	https://github.com/CogniPilot/foxglove-cognipilot-joy/releases?q=airy&expanded=true

**Step 3:** Scroll down and download this particular file: _**cognipilot.cognipilot-joystick-0.0.1.zip**_

**Step 4:** Unzip the downloaded zip file and put it in correct path for operating systems 	foxglove-studio. For Linux Systems Only: (Run the below commands on a terminal)

{% hint style="info" %}
Make sure that you are in the same directory that you downloaded the zip 	while executing the above commands
{% endhint %}

```
mkdir -p ~/.foxglove-studio/extensions 
mv cognipilot.cognipilot-joystick-*.zip ~/.foxglove-studio/extensions 
cd ~/.foxglove-studio/extensions 
unzip cognipilot.cognipilot-joystick-*.zip
```

**Step 5:** Download the layout of foxglove from this link:
	https://github.com/CogniPilot/electrode/blob/airy/foxglove_layouts/b3rb.json (Press the download icon on the top right side of the page to download the file)

**Step 6:** Open the foxglove studio application on your device

**Step 7:** Connect to your buggy via the open a connection option

**Step 8:** Once the connection is established, on the top right corner, there will be an 	option for layout, choose a custom layout and select the downloaded json file.

## Update CANHUBK344 Firmware 
Update CANHUBK344 firmware with safety disbabled.

**Step 1:** Go to following file on setup: **_~/cognipilot/ws/cerebri/app/b3rb/prj.conf_**

**Step 2:**  Update **_CONFIG_CEREBRI_SENSE_POWER_** on line 24 by replacing y with n:
```
CONFIG_CEREBRI_SENSE_POWER=n
```

**Step 3:**  Update **_CONFIG_CEREBRI_SENSE_SAFETY_** on line 25 by replacing y with n:
```
CONFIG_CEREBRI_SENSE_SAFETY=n
```

**Step 4:**  Rebuild the code for CANHUBK344 and deploy it on board using J-link debugger

## Get  NXP AIM Buggy in Manual Mode

**Step 1:** Conenct buggy and host laptop to same wifi network

**Step 2:** Open the foxglove studio application on your device and connection option

**Step 3:**  Click on Manual button on foxglove GUI

**Step 4:**  Click on ARM button on foxglove GUI

**Step 5:**  Click on the joystick to move buggy on manual mode

