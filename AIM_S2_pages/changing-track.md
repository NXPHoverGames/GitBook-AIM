# Changing Track

## Track 2

The new track to be used for the final round is available for download:

{% file src=".gitbook/assets/AIM_S2/nxp_raceway_2.zip" %}
nxp\_raceway\_2
{% endfile %}

Extract the contents of the above zip file at: _**\~/ros2ws/nxp\_gazebo/models**_

### Changing track for simulations:

To change track navigate to _**\~/ros2ws/src/sim\_gazebo\_bringup/config**_ in the software stack and open the **gen\_params.json **_****_ file.

To change the track navigate to the "embedded\_models" sub-tag in the "world\_params" tag and edit the contents of "embed\_model\_0"

![](.gitbook/assets/AIM_S2/changeTrack.png)

To use the new raceway track in simulation, use the following values:

```
"embed_model_0": {
					"model": "nxp_raceway_2",
					"name": "nxp_raceway_0",
					"pose": "-2 -0.35 -0.04 0 0 0"
				}
```

To use the previous overpass track in simulation:

```
"embed_model_0": {
					"model": "nxp_raceway_overpass",
					"name": "nxp_raceway_overpass_0",
					"pose": "0 0 -0.009 0 0 0"
				}
```



{% hint style="danger" %}
Only use the pose values mentioned above. These values are fixed and final evaluation will take place with the same values as well.
{% endhint %}
