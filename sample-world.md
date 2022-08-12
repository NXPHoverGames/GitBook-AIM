# Sample World For Pre-Finale Round

## Sample World
{% hint style="danger" %}
The sample world was updatd on 12th August,2022. Please use the updated obstacle positions given below.
{% endhint %}

To add obstacles into the simulation environment, navigate to _**\~/ros2ws/src/sim\_gazebo\_bringup/config**_ in the software stack and open the _**gen\_params.json**_ file.

To add obstacles navigate to the "embedded\_models" sub-tag in the "world\_params" tag. Then copy the following code:

```"embedded_models": {
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
				},
				"embed_model_3": {
					"model": "turn_right_sign",
					"name": "turn_left_1",
					"pose": "6.961647 6.999404 0.141243 0 0 0.224956"
				},
				"embed_model_4": {
					"model": "turn_right_sign",
					"name": "turn_left_2",
					"pose": "7.157476 7.866743 0.139078 0 0 -0.480452"
				},
				"embed_model_8": {
					"model": "turn_left_sign",
					"name": "turn_left_3",
					"pose": "-0.001217 2.517102 0.141243 0 0 1.561054"
				},
				"embed_model_9": {
					"model": "turn_left_sign",
					"name": "turn_left_4",
					"pose": "-0.450366 3.231226 0.141243 0 0 0.563165"
				},
				"embed_model_5": {
					"model": "turn_left_sign",
					"name": "turn_right_0",
					"pose": "6.101090 7.838730 0.141243 0 0 -1.401961"
				},				
				"embed_model_6": {
					"model": "turn_left_sign",
					"name": "turn_right_1",
					"pose": "6.039118 7.043794 0.141243 0 0 -1.401962"
				},
				"embed_model_7": {
					"model": "turn_left_sign",
					"name": "turn_right_2",
					"pose": "6.850454 6.458070 0.317739 0 0 -2.318629"
				},
				"embed_model_10": {
					"model": "stop_traffic_sign",
					"name": "stop_traffic_sign",
					"pose": "1.394454 1.362193 0.153013 0 0 1.582700"
				},
				"embed_model_11": {
					"model": "finish_line",
					"name": "finish_line",
					"pose": "1.264966 1.625857 0.014189 0 0 1.546246"
				},
				"embed_model_12": {
					"model": "turn_right_sign",
					"name": "turn_right_01",
					"pose": "6.036990 -1.957740 0.141243 0 0 -3.010565"
				},
				"embed_model_13": {
					"model": "turn_right_sign",
					"name": "turn_right_02",
					"pose": "5.892650 -1.129460 0.141243 0 0 -3.010571"
				},
				"embed_model_14": {
					"model": "turn_right_sign",
					"name": "turn_right_03",
					"pose": "7.008253 -1.155979 0.141243 0 0 -0.034782"
				},
				"embed_model_15": {
					"model": "turn_right_sign",
					"name": "turn_right_04",
					"pose": "6.967960 -1.997830 0.141243 0 0 -0.034782"
				},
				"embed_model_16": {
					"model": "car",
					"name": "car_1",
					"pose": "1.520010 -2.371180 0 0 0 0"
				},
				"embed_model_17": {
					"model": "car_blue",
					"name": "car_2",
					"pose": "3.778930 -0.209861 0 0 0 0"
				},
				"embed_model_18": {
					"model": "dumpster2",
					"name": "dumpster_1",
					"pose": "6.209020 3.039650 0 0 0 0"
				},
				"embed_model_19": {
					"model": "dumpster2",
					"name": "dumpster_2",
					"pose": "6.787890 3.078500 0 0 0 0"
				},
				"embed_model_20": {
					"model": "Construction_Cone_mini",
					"name": "Construction_Cone_1",
					"pose": "5.196230 7.230290 0 0 0 0"
				},
				"embed_model_21": {
					"model": "Construction_Cone_mini",
					"name": "Construction_Cone_2",
					"pose": "4.985940 7.626090 0 0 0 0"
				},
				"embed_model_22": {
					"model": "Construction_Cone_mini",
					"name": "Construction_Cone_3",
					"pose": "4.866470 7.247080 0 0 0 0"
				},
				"embed_model_23": {
					"model": "Construction_Cone_mini",
					"name": "Construction_Cone_4",
					"pose": "4.835070 7.643900 0 0 0 0"
				},
				"embed_model_24": {
					"model": "Construction_Cone_mini",
					"name": "Construction_Cone_5",
					"pose": "4.604640 7.258980 0 0 0 0"
				},
				"embed_model_25": {
					"model": "Construction_Cone_mini",
					"name": "Construction_Cone_6",
					"pose": "4.439520 7.363690 0 0 0 0"
				},
				"embed_model_26": {
					"model": "Construction_Cone_mini",
					"name": "Construction_Cone_7",
					"pose": "4.256437 7.416032 0 0 0 0"
				},
				"embed_model_27": {
					"model": "Construction_Cone_mini",
					"name": "Construction_Cone_8",
					"pose": "4.100130 7.720550 0 0 0 0"
				},
				"embed_model_28": {
					"model": "Construction_Cone_mini",
					"name": "Construction_Cone_9",
					"pose": "3.975580 7.679610 0 0 0 0"
				},
				"embed_model_29": {
					"model": "Construction_Cone_mini",
					"name": "Construction_Cone_10",
					"pose": "3.976610 7.328560 0 0 0 0"
				},
				"embed_model_30": {
					"model": "Construction_Cone_mini",
					"name": "Construction_Cone_11",
					"pose": "3.767880 7.589030 0 0 0 0"
				},
				"embed_model_31": {
					"model": "Construction_Cone_mini",
					"name": "Construction_Cone_12",
					"pose": "3.637660 7.525750 0 0 0 0"
				},
				"embed_model_32": {
					"model": "barricade",
					"name": "barricade_1",
					"pose": "0.326338 5.906060 0.030935 0 0 0"
				},
				"embed_model_33": {
					"model": "barricade",
					"name": "barricade_2",
					"pose": "-0.245990 5.526630 0.030935 0 0 0"
				},
				"embed_model_34": {
					"model": "barricade",
					"name": "barricade_3",
					"pose": "0.297154 4.981470 0.030935 0 0 0"
				},
				"embed_model_35": {
					"model": "barricade",
					"name": "barricade_4",
					"pose": "-0.268218 4.486810 0.030935 0 0 0"
				},
				"embed_model_36": {
					"model": "barricade",
					"name": "barricade_5",
					"pose": "1.716760 8.794882 0.479858 0 0 0"
				},
				"embed_model_37": {
					"model": "person_2",
					"name": "person_1",
					"pose": "6.255060 0.113153 0 0 0 0"
				},
				"embed_model_38": {
					"model": "person_1",
					"name": "person_2",
					"pose": "3.677107 4.207261 0.468489 0 0 0"
				},
				"embed_model_39": {
					"model": "postbox2",
					"name": "postbox_1",
					"pose": "6.805440 -3.120050 0 0 0 0"
				},
				"embed_model_40": {
					"model": "oak_tree_mini",
					"name": "tree_1",
					"pose": "9.417270 -3.485010 0 0 0 0"
				},
				"embed_model_41": {
					"model": "oak_tree_mini",
					"name": "tree_2",
					"pose": "9.611970 4.774720 0 0 0 0"
				},
				"embed_model_42": {
					"model": "oak_tree_mini",
					"name": "tree_3",
					"pose": "6.616697 9.718095 0.441569 0 0 0"
				},
				"embed_model_43": {
					"model": "traffic_light_red",
					"name": "traffic_light",
					"pose": "1.322568 7.290203 0.680126 0 0 1.528681"
				},
				"embed_model_44": {
					"model": "fire_hydrant2",
					"name": "fire_hydrant_1",
					"pose": "8.499910 6.678930 0 0 0 0"
				}
			},
```

![code snippet](.gitbook/assets/gen_params_sample_track.png)

The gazebo world will look like the image below:

![SAMPLE TRACK Img_1](<.gitbook/assets/sample_track1.png>)

![SAMPLE TRACK Img_2](<.gitbook/assets/sample_tack-2.png>)

![SAMPLE TRACK Img_3](<.gitbook/assets/sample_track_3.png>)

![SAMPLE TRACK Img_4](<.gitbook/assets/sample_track_4.png>)

{% hint style="warning" %}
This is just a _**sample world for the Pre-Finale Round**_. 
{% endhint %}


{% hint style="info" %}
In Pre-finale and Grand Finale round, there will be both moving and static obstacles. More obstacles will be added in these rounds. Positions  and direction of traffic signs (& lights) will be changed.{% endhint %}

### Make traffic light change colour during simulation
{% hint style="info" %}
The sample world was updatd on 12th August,2022. Please use the updated traffic light positions given below
{% endhint %}
In  _**spawn\_light.py**_  file, replace the content of the file with following lines of code:
```import os
from time import sleep

spawn_green="gz model --spawn-file=/home/manish/ros2ws/nxp_gazebo/models/traffic_light_green/model.sdf --model-name=lightGreen -x 1.496568 -y 7.320472 -z 0.778152 -R -3.121948 -P -0.006105 -Y 1.503726"
del_green="gz model -m lightGreen -d"

while(True):	
	sleep(10)
	os.system(spawn_green)
	sleep(10)
	os.system(del_green)	

```

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
