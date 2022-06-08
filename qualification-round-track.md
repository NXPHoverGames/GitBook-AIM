---
description: Track for Qualification Round.
---

# QUALIFICATION ROUND TRACK

## Download Qualification Track

Download the following zip file containing the qualification round track and extract it in _**\~ros2ws/nxp_gazebo/models/ **_ .

{% file src=".gitbook/assets/qualification_round_track_model.zip" %}
Qualification Round Track Model
{% endfile %}

{% hint style="warning" %}
You might get pop-up dialogue for replacing start_point model folder. Replace it with the new model available in .zip package
{% endhint %}

Your directory will look like this after downloading the new track: 
![](<.gitbook/assets/qulaification round track.png>)

To add qualification round track into the simulation environment, navigate to _**\~/ros2ws/src/sim\_gazebo\_bringup/config**_ in the software stack and open the _**gen\_params.json**_ file.

To add new track navigate to the "embedded\_models" sub-tag in the "world\_params" tag. Then copy the following code:

```
"embedded_models": {
				"embed_model_0": {
					"model": "nxp_raceway_2",
					"name": "nxp_raceway_overpass_0",
					"pose": "-2 -0.35 -0.04 0 0 0"
				}
		
			},
```
[image]

 After launching gazebo via command line, you will see the following world in simulation:
 
 [image]
