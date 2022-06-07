---
description: Track for Qualification Round
---

# QUALIFICATION ROUND TRACK

# Download Track

Download the following zip file containing the qualification round track and extract it in _**\~/ros2ws/src/ **_ .

Attach files

To add qualification round track into the simulation environment, navigate to _**\~/ros2ws/src/sim\_gazebo\_bringup/config**_ in the software stack and open the _**gen\_params.json**_ file.

To add obstacles navigate to the "embedded\_models" sub-tag in the "world\_params" tag. Then copy the following code:

```
"embedded_models": {
				"embed_model_0": {
					"model": "nxp_raceway_2",
					"name": "nxp_raceway_overpass_0",
					"pose": "-2 -0.35 -0.04 0 0 0"
				}
		
			},
```
