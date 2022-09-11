---
description: Track for GRAND FINALE ROUND.
---

# GRAND FINALE ROUND TRACK

## Download Grand Fianle Track

{% hint style="danger" %} 
The grand finale track was updatd on 11th September,2022 (12:00 AM IST). Please download the new track available below. 
{% endhint %}

Download the following zip file containing the qualification round track and extract it in _**\~ros2ws/nxp_gazebo/models/**_ .

{% file src=".gitbook/assets/Grand_Finale_Track_updated.zip" %}
Grand Finale Track Model
{% endfile %}

Your directory will look like this after downloading the new track: 

![](<.gitbook/assets/adding_gf_track.png>)


## Spawn Track in Gazebo

To add qualification round track into the simulation environment, navigate to _**\~/ros2ws/src/sim\_gazebo\_bringup/config**_ in the software stack and open the _**gen\_params.json**_ file.

To add new track navigate to the "embedded\_models" sub-tag in the "world\_params" tag. Then copy the following code:

```
"embedded_models": {
				"embed_model_0": {
					"model": "Grand_Finale_Track",
					"name": "Raceway_1_track",
					"pose": "0 0 0.04000 0 0 0"
				}
			},
```
 
![](<.gitbook/assets/code_gf_track.png>)


 After launching gazebo via command line, you will see the following world in simulation:

![](<.gitbook/assets/gf_1.png>)
![](<.gitbook/assets/gf_2.png>)


## Update Delay (Compulsory)

For Grand Finale Round, teams are required to add delay of 15 seconds before the car starts moving.
To do this navigate to _**aim\_line\_follow.py**_ located at: _**`~/ros2ws/src/aim_line_follow/aim_line_follow`**_. Set the value of _**start_delay**_.

```
self.start_delay = 15.0
```

![](<.gitbook/assets/change_aim_follow.png>)
