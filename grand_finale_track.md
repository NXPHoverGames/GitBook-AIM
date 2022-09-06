---
description: Track for GRAND FINALE ROUND.
---

# GRAND FINALE ROUND TRACK

## Download Qualification Track

Download the following zip file containing the qualification round track and extract it in _**\~ros2ws/nxp_gazebo/models/**_ .

{% file src=".gitbook/assets/Raceway_1_final_qf.zip" %}
Qualification Round Track Model
{% endfile %}

{% hint style="warning" %}
You might get pop-up dialogue for replacing start_point model folder. Replace it with the new model available in .zip package
{% endhint %}

Your directory will look like this after downloading the new track: 

![](<.gitbook/assets/model_dir.png>)


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
 
![](<.gitbook/assets/code_add.png>)


 After launching gazebo via command line, you will see the following world in simulation:

![](<.gitbook/assets/track_final_qr.png>)
