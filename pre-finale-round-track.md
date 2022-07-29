---
description: Track for Qualification Round.
---

# Pre-Finale ROUND TRACK

## Download Qualification Track

{% hint style="danger" %}
The pre-finale round evaluation will be taking place on the below track with obstacles included
{% endhint %}


Download the following zip file containing the qualification round track and extract it in _**\~ros2ws/nxp_gazebo/models/**_ .

{% file src=".gitbook/assets/Raceway2.zip" %}
Pre-Finale Round Track Model
{% endfile %}

## Spawn Track in Gazebo

To add qualification round track into the simulation environment, navigate to _**\~/ros2ws/src/sim\_gazebo\_bringup/config**_ in the software stack and open the _**gen\_params.json**_ file.

To add new track navigate to the "embedded\_models" sub-tag in the "world\_params" tag. Then copy the following code:

```
"embedded_models": {
				"embed_model_0": {
					"model": "Raceway_1",
					"name": "Raceway_1_track",
					"pose": "-3.698240 -1.411953 0.03000 0 0 0"
				},
				"embed_model_1": {
					"model": "start_point",
					"name": "start_point_1",
					"pose": "0.1 0.551953 0.03000 0 0 0"
				},
				"embed_model_2": {
					"model": "start_point",
					"name": "start_point_2",
					"pose": "0.1 -0.651953 0.03000 0 0 0"
				}			
			},
```
 
![](<.gitbook/assets/change_in_config_file.png>)


 After launching gazebo via command line, you will see the following world in simulation:

![](<.gitbook/assets/pre_track_2.png>)
![](<.gitbook/assets/track_pre_1.png>)
