# New Tracks

## New traffic sign models

These are updated traffic signs, traffic light, zebra line and finish line. Participants are required to replace the previous model folders with new folders in given zip file.

{% file src=".gitbook/assets/new_signs.zip" %}
New signs
{% endfile %}

## New Human Obstacles

{% file src=".gitbook/assets/person_2.zip" %}
Human Obstacle 1
{% endfile %}

{% file src=".gitbook/assets/person_1.zip" %}
Human Obstacle 2
{% endfile %}

## Sample Track

To add obstacles into the simulation environment, navigate to _**\~/ros2ws/src/sim\_gazebo\_bringup/config**_ in the software stack and open the **gen\_params.json **_****_ file.

To add obstacles navigate to the "embedded\_models" sub-tag in the "world\_params" tag. Then copy the following code:

```
"embedded_models": {
				"embed_model_0": {
					"model": "nxp_raceway_2",
					"name": "nxp_raceway_overpass_0",
					"pose": "-2 -0.35 -0.04 0 0 0"
				},
				"embed_model_1": {
					"model": "start_point",
					"name": "start_point_0",
					"pose": "0.2 -0.412042 0.09 0 0 0"
				},
				"embed_model_2": {
					"model": "start_point",
					"name": "start_point_1",
					"pose": "0.2 0.624883 0.09 0 0 0"
				},
				"embed_model_3": {
					"model": "go_straight_sign",
					"name": "sign_1",
					"pose": "5.393145 4.020703 0.115537 0 0 0"
				},
				"embed_model_4": {
					"model": "go_straight_sign",
					"name": "sign_2",
					"pose": "5.326705 3.146068 0.115537 0 0 -1.639132"
				},
				"embed_model_5": {
					"model": "stop_traffic_sign",
					"name": "stop",
					"pose": "-0.171723 0.467679 0.123072 0 0 -2.549039"
				},
				"embed_model_6": {
					"model": "oak_tree_mini",
					"name": "tree",
					"pose": "7.190042 3.645584 0 0 0 0"
				},
				
				"embed_model_7": {
					"model": "barricade",
					"name": "barricade_1",
					"pose": "3.519024 0.370385 0.031807 0 0 1.539841"
				},
				"embed_model_8": {
					"model": "barricade",
					"name": "barricade_2",
					"pose": "-0.658839 1.234693 0.031807 0 0 1.539841"
				},
				"embed_model_9": {
					"model": "barricade",
					"name": "barricade_3",
					"pose": "4.026354 -0.119128 0.031807 0 0 1.539841"
				},
				"embed_model_10": {
					"model": "finish_line",
					"name": "finish",
					"pose": "-0.397272 0.101526 0.005 0 0 0"
				},
				"embed_model_11": {
					"model": "fire_hydrant2",
					"name": "hydrant",
					"pose": "6.400470 0.997986 -0.010970 0 0 0"
				},
				
				"embed_model_12": {
					"model": "traffic_light_red",
					"name": "traffic_light",
					"pose": "0.607803 2.528717 0.224218 0 0 1.612265"
				},
				"embed_model_13": {
					"model": "start_sign",
					"name": "start",
					"pose": "0.581745 0.585257 0.150951 0 0 -2.196015"
				},
				"embed_model_14": {
					"model": "zebra_line",
					"name": "crossing",
					"pose": "0.791940 2.817986 0.005 0 0 1.583922"
				},
				"embed_model_15": {
					"model": "Construction_Cone_mini",
					"name": "cone_1",
					"pose": "6.516230 4.990960 0 0 0 0"
				},
				"embed_model_16": {
					"model": "Construction_Cone_mini",
					"name": "cone_2",
					"pose": "6.162980 4.990960 0 0 0 0"
				},
				"embed_model_17": {
					"model": "Construction_Cone_mini",
					"name": "cone_3",
					"pose": "5.761880 4.990960 0 0 0 0"
				},
				"embed_model_18": {
					"model": "Construction_Cone_mini",
					"name": "cone_4",
					"pose": "2.809120 6.380610 0 0 0 0"
				},
				"embed_model_19": {
					"model": "Construction_Cone_mini",
					"name": "cone_5",
					"pose": "2.380310 5.919590 0 0 0 0"
				},
				"embed_model_20": {
					"model": "Construction_Cone_mini",
					"name": "cone_6",
					"pose": "1.922995 6.422790 0 0 0 0"
				},
				"embed_model_21": {
					"model": "Construction_Cone_mini",
					"name": "cone_7",
					"pose": "1.423960 6.035790 0 0 0 0"
				},
				"embed_model_22": {
					"model": "car_blue",
					"name": "car",
					"pose": "4.023540 3.360870 0 0 0 0"
				},
				"embed_model_23": {
					"model": "ambulance_mini",
					"name": "ambulance",
					"pose": "0.233090 6.622330 0 0 0 0"
				},
				"embed_model_24": {
					"model": "person_1",
					"name": "human_1",
					"pose": "4.558640 2.158550 0 0 0 0"
				},
				"embed_model_25": {
					"model": "person_1",
					"name": "human_2",
					"pose": "-0.661461 4.982290 0 0 0 0"
				}
			
			},
```

![code snippet](.gitbook/assets/code1.png)

The gazebo world will look like the image below:

![SAMPLE TRACK](<.gitbook/assets/sample track.png>)

{% hint style="warning" %}
This is just a sample track. In grand finale, there will be both moving and static obstacles.
{% endhint %}

### Make traffic light change colour during simulation

{% file src=".gitbook/assets/spawn_light.zip" %}
Color change python program
{% endfile %}

Download the above zip file and extract the file: _**spawn\_light.py**_ in the root folder/dir

While simulation is running, open a new terminal and run the following command:

```
$ python3 spawn_light.py
```

{% hint style="info" %}
Run the above command only when gazebo has started and initialized succesfully
{% endhint %}

This script will enable changing of red light to green light (and vice versa) in simulation after 10 seconds interval.

{% hint style="danger" %}
This script is only compatible for sample track given above. If you want to use the script for other locations of red light in the gazebo, world then edit the -x -y -z -R -P -Y values accordingly
{% endhint %}
