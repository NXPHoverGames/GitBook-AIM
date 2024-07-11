---
description: Track for Qualification Round.
---

# Pre-Finale Round Track

{% hint style="danger" %}
The qualification track was updatd on 12th August,2022 (3:30 PM IST). Please download the new track available below. 
{% endhint %}

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
					"model": "Raceway2",
					"name": "Raceway_1_track",
					"pose": "0 0 0.04000 0 0 0"
				},
				"embed_model_1": {
					"model": "start_point",
					"name": "start_point_1",
					"pose": "0.533241 0 0.067473 0 0 0"
				},
				"embed_model_2": {
					"model": "start_point",
					"name": "start_point_2",
					"pose": "-0.533241 0 0.067473 0 0 0"
				}			
			},
```
 
Next, you have to re-adjust the car position in Gazebo simulation. For this, navigate to the "spawn\_pose" for "model\_params\_0" sub-tag in the "models" tag. Then  copy the following code:

```
"spawn_pose": [0,0,0.1,0,0,-1.5],
```

After doing the above changes, the _**gen\_params.json**_ file would appear like this:
 
![](<.gitbook/assets/change_in_config_file.png>)


 After launching gazebo via command line, you will see the following world in simulation:

![](<.gitbook/assets/prefinale_track_2.png>)
![](<.gitbook/assets/prefinale_track_1.png>)
