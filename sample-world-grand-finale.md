# Sample World For Grand Finale Round

## Updated Obstacles

Participants must download new and updated obstacles that will be used in the grand finale rounds from the given zip file:

{% file src=".gitbook/assets/obstacles_updated.zip" %}
sample obstacles
{% endfile %}


Extract the contents of the above zip files at: _**\~/ros2ws/nxp\_gazebo/models**_.



## Sample World

To add obstacles into the simulation environment, navigate to _**\~/ros2ws/src/sim\_gazebo\_bringup/config**_ in the software stack and open the _**gen\_params.json**_ file.

To add obstacles navigate to the "embedded\_models" sub-tag in the "world\_params" tag. Then copy the following code:

```"embedded_models": {
				"embed_model_0": {
					"model": "Grand_Finale_Track",
					"name": "Raceway_1_track",
					"pose": "0 0 0.04000 0 0 0"
				},
				"embed_model_1": {
					"model": "turn_right_sign",
					"name": "traffic_sign_1",
					"pose": "9.402500 -1.977447 0.148539 0 0 0"
				},
				"embed_model_2": {
					"model": "turn_right_sign",
					"name": "traffic_sign_2",
					"pose": "9.456667 -1.139340 0.148539 0 0 -0.071725"
				},
				"embed_model_3": {
					"model": "turn_right_sign",
					"name": "traffic_sign_3",
					"pose": "9.883320 7.044300 0.148539 0 0 0.303384"
				},
				"embed_model_4": {
					"model": "turn_right_sign",
					"name": "traffic_sign_4",
					"pose": "9.803770 7.857500 0.148539 0 0 -0.258759"
				},
				"embed_model_5": {
					"model": "turn_left_sign",
					"name": "traffic_sign_5",
					"pose": "0.001388 2.479030 0.136295 0 0 1.533982"
				},
				"embed_model_6": {
					"model": "turn_left_sign",
					"name": "traffic_sign_6",
					"pose": "-0.512472 3.303309 0.136295 0 0 0.658347"
				},
				"embed_model_7": {
					"model": "turn_left_sign",
					"name": "traffic_sign_7",
					"pose": "8.487010 7.067690 0.136295 0 0 -1.652750"
				},
				"embed_model_8": {
					"model": "turn_left_sign",
					"name": "traffic_sign_8",
					"pose": "9.562090 7.052380 0.136295 0 0 -1.652750"
				},
				"embed_model_9": {
					"model": "turn_left_sign",
					"name": "traffic_sign_9",
					"pose": "8.457190 7.796263 0.136295 0 0 -1.652750"
				},
				"embed_model_10": {
					"model": "turn_right_sign",
					"name": "traffic_sign_10",
					"pose": "8.281400 -1.139660 0.148539 0 0 -3.097239"
				},
				"embed_model_11": {
					"model": "turn_right_sign",
					"name": "traffic_sign_11",
					"pose": "8.303630 -1.948590 0.148539 0 0 -3.097239"
				},
				"embed_model_12": {
					"model": "stop_traffic_sign",
					"name": "traffic_sign_12",
					"pose": "1.844553 1.162403 0.148539 0 0 1.613485"
				},
				"embed_model_13": {
					"model": "start_sign",
					"name": "traffic_sign_13",
					"pose": "0.440220 -0.329911 0.148895 0 0 2.236049"
				},
				"embed_model_14": {
					"model": "finish_line",
					"name": "finish_line",
					"pose": "1.783834 1.444477 0.013138 0 0 1.572164"
				},
				"embed_model_15": {
					"model": "start_point",
					"name": "start_point_1",
					"pose": "-0.612618 -0.013972 0.045986 0 0 0"
				},
				"embed_model_16": {
					"model": "start_point",
					"name": "start_point_2",
					"pose": "0.612618 -0.013972 0.045986 0 0 0"
				},
				"embed_model_17": {
					"model": "traffic_light_red",
					"name": "traffic_light",
					"pose": "1.715409 7.437574 0.682362 0 0 1.625140"
				},
				"embed_model_18": {
					"model": "Construction_Cone_mini",
					"name": "cone_1",
					"pose": "7.567870 7.210160 0.005632 0 0 0"
				},
				"embed_model_19": {
					"model": "Construction_Cone_mini",
					"name": "cone_2",
					"pose": "7.448000 7.340340 0.005632 0 0 0"
				},
				"embed_model_20": {
					"model": "Construction_Cone_mini",
					"name": "cone_3",
					"pose": "7.202740 7.441100 0.005632 0 0 0"
				},
				"embed_model_21": {
					"model": "Construction_Cone_mini",
					"name": "cone_4",
					"pose": "6.894920 7.351870 0.005632 0 0 0"
				},
				"embed_model_22": {
					"model": "Construction_Cone_mini",
					"name": "cone_5",
					"pose": "6.858850 7.699800 0.005632 0 0 0"
				},
				"embed_model_23": {
					"model": "Construction_Cone_mini",
					"name": "cone_6",
					"pose": "6.592080 7.539160 0.005632 0 0 0"
				},
				"embed_model_24": {
					"model": "Construction_Cone_mini",
					"name": "cone_7",
					"pose": "6.387780 7.187800 0.005632 0 0 0"
				},
				"embed_model_25": {
					"model": "Construction_Cone_mini",
					"name": "cone_8",
					"pose": "6.377240 7.488970 0.005632 0 0 0"
				},
				"embed_model_26": {
					"model": "Construction_Cone_mini",
					"name": "cone_9",
					"pose": "6.119870 7.649290 0.005632 0 0 0"
				},
				"embed_model_27": {
					"model": "Construction_Cone_mini",
					"name": "cone_10",
					"pose": "6.000159 7.294543 0.005632 0 0 0"
				},
				"embed_model_28": {
					"model": "Construction_Cone_mini",
					"name": "cone_11",
					"pose": "5.796370 7.574460 0.005632 0 0 0"
				},
				"embed_model_29": {
					"model": "Construction_Cone_mini",
					"name": "cone_12",
					"pose": "7.574460 7.277210 0.005632 0 0 0"
				},
				"embed_model_30": {
					"model": "Construction_Cone_mini",
					"name": "cone_13",
					"pose": "5.609410 7.609925 0.005632 0 0 0"
				},
				"embed_model_31": {
					"model": "Construction_Cone_mini",
					"name": "cone_14",
					"pose": "5.345370 7.431643 0.005632 0 0 0"
				},
				"embed_model_32": {
					"model": "barricade",
					"name": "barricade_1",
					"pose": "1.552310 8.849634 0.487573 0 0 0"
				},
				"embed_model_33": {
					"model": "barricade",
					"name": "barricade_2",
					"pose": "12.893254 5.917786 0.042556 0 0 -0.025547"
				},
				"embed_model_34": {
					"model": "barricade",
					"name": "barricade_3",
					"pose": "12.488200 5.465990 0.042556 0 0 -0.218661"
				},
				"embed_model_35": {
					"model": "barricade",
					"name": "barricade_4",
					"pose": "13.132400 5.127830 0.042556 0 0 -0.218661"
				},
				"embed_model_36": {
					"model": "barricade",
					"name": "barricade_5",
					"pose": "12.484065 4.944537 0.042556 0 0 -0.218661"
				},
				"embed_model_37": {
					"model": "barricade",
					"name": "barricade_6",
					"pose": "12.949740 4.383964 0.042556 0 0 -0.334116"
				},
				"embed_model_38": {
					"model": "barricade",
					"name": "barricade_7",
					"pose": "12.516300 3.706770 0.042556 0 0 -1.263369"
				},
				"embed_model_39": {
					"model": "barricade",
					"name": "barricade_8",
					"pose": "11.806300 3.750260 0.042556 0 0 -1.263369"
				},
				"embed_model_40": {
					"model": "barricade",
					"name": "barricade_9",
					"pose": "8.610840 3.068810 0.042556 0 0 -0.048239"
				},
				"embed_model_41": {
					"model": "beer",
					"name": "can",
					"pose": "8.387030 3.097294 -0.000002 0 0 0.004894"
				},
				"embed_model_42": {
					"model": "dumpster2",
					"name": "dumpster_1",
					"pose": "8.871810 3.061850 0 0 0 0"
				},
				"embed_model_43": {
					"model": "dumpster2",
					"name": "dumpster_2",
					"pose": "9.054320 3.059220 0 0 0 0"
				},
				"embed_model_44": {
					"model": "dumpster2",
					"name": "dumpster_3",
					"pose": "7.120070 4.796838 0.433025 0 0 0"
				},
				"embed_model_45": {
					"model": "car",
					"name": "car_1",
					"pose": "4.272600 -0.428299 0 0 0 0"
				},
				"embed_model_46": {
					"model": "car_red",
					"name": "car_2",
					"pose": "0.695777 -2.381700 0 0 0 0"
				},"embed_model_47": {
					"model": "car_blue",
					"name": "car_3",
					"pose": "10.286200 -4.549350 0 0 0 0"
				},"embed_model_48": {
					"model": "car_red",
					"name": "car_4",
					"pose": "12.041410 7.038221 0 0 0 -0.455982"
				},"embed_model_49": {
					"model": "car_blue",
					"name": "car_5",
					"pose": "11.597200 7.240060 0 0 0 0"
				},"embed_model_50": {
					"model": "car",
					"name": "car_6",
					"pose": "3.469760 7.886740 0 0 0 -1.052809"
				},"embed_model_51": {
					"model": "car_blue",
					"name": "car_7",
					"pose": "4.226350 7.801730 0 0 0 2.009600"
				},"embed_model_52": {
					"model": "car_red",
					"name": "car_8",
					"pose": "3.806930 7.780270 0 0 0 -1.052814"
				},"embed_model_53": {
					"model": "car_blue",
					"name": "car_9",
					"pose": "3.254790 7.816110 0 0 0 -1.064601"
				},"embed_model_54": {
					"model": "car_blue",
					"name": "car_10",
					"pose": "3.759180 7.045848 0 0 0 0"
				},"embed_model_55": {
					"model": "car_red",
					"name": "car_11",
					"pose": "4.223640 6.954260 0 0 0 1.172812"
				},
				"embed_model_56": {
					"model": "car_red",
					"name": "car_12",
					"pose": "3.330235 6.953325 0 0 0 1.319436"
				},
				"embed_model_57": {
					"model": "person_1",
					"name": "person_1",
					"pose": "12.970000 -3.012290 0 0 0 1.319436"
				},
				"embed_model_58": {
					"model": "person_1",
					"name": "person_2",
					"pose": "5.342956 4.135203 0.449260 0 0 0"
				},
				"embed_model_59": {
					"model": "person_2",
					"name": "person_3",
					"pose": "4.649300 10.489862 0.424585 0 0 0"
				},
				"embed_model_60": {
					"model": "person_2",
					"name": "person_3",
					"pose": "1.128260 1.773810 0 0 0 0"
				},
				"embed_model_61": {
					"model": "person_2",
					"name": "person_4",
					"pose": "8.473800 -3.183250 0 0 0 0"
				},
				"embed_model_62": {
					"model": "coke_can",
					"name": "can_2",
					"pose": "2.218836 4.614859 0.456268 0 0 0"
				},
				"embed_model_63": {
					"model": "fire_hydrant2",
					"name": "fire_hydrant_1",
					"pose": "0.651545 2.982810 0 0 0 0"
				},
				"embed_model_64": {
					"model": "fire_hydrant2",
					"name": "fire_hydrant_2",
					"pose": "2.857220 -0.326151 0 0 0 0"
				},
				"embed_model_65": {
					"model": "postbox2",
					"name": "postbox",
					"pose": "11.322000 -1.340280 0 0 0 0"
				},
				"embed_model_66": {
					"model": "oak_tree_mini",
					"name": "tree_1",
					"pose": "11.424100 -4.529290 0 0 0 0"
				},
				"embed_model_67": {
					"model": "oak_tree_mini",
					"name": "tree_2",
					"pose": "11.581800 -4.538950 0 0 0 0"
				},
				"embed_model_68": {
					"model": "oak_tree_mini",
					"name": "tree_3",
					"pose": "12.034900 -4.353690 0 0 0 0"
				},
				"embed_model_69": {
					"model": "oak_tree_mini",
					"name": "tree_4",
					"pose": "11.424100 -4.431000 0 0 0 0"
				},
				"embed_model_70": {
					"model": "oak_tree_mini",
					"name": "tree_5",
					"pose": "12.230900 -4.245590 0 0 0 0"
				},
				"embed_model_71": {
					"model": "oak_tree_mini",
					"name": "tree_6",
					"pose": "12.326000 -4.135820 0 0 0 0"
				},
				"embed_model_72": {
					"model": "oak_tree_mini",
					"name": "tree_7",
					"pose": "12.504000 -3.970900 0 0 0 0"
				},
				"embed_model_73": {
					"model": "oak_tree_mini",
					"name": "tree_8",
					"pose": "12.646600 -3.745520 0 0 0 0"
				},
				"embed_model_74": {
					"model": "oak_tree_mini",
					"name": "tree_9",
					"pose": "12.108400 -3.330360 0 0 0 0"
				},
				"embed_model_75": {
					"model": "oak_tree_mini",
					"name": "tree_10",
					"pose": "11.909600 -3.485480 0 0 0 0"
				},
				"embed_model_76": {
					"model": "oak_tree_mini",
					"name": "tree_11",
					"pose": "12.326000 -3.330360 0 0 0 0"
				},
				"embed_model_77": {
					"model": "oak_tree_mini",
					"name": "tree_12",
					"pose": "12.028000 -3.536200 0 0 0 0"
				},
				"embed_model_78": {
					"model": "oak_tree_mini",
					"name": "tree_13",
					"pose": "11.794300 -3.670010 0 0 0 0"
				},
				"embed_model_79": {
					"model": "oak_tree_mini",
					"name": "tree_14",
					"pose": "11.508400 -3.821190 0 0 0 0"
				},
				"embed_model_80": {
					"model": "oak_tree_mini",
					"name": "tree_15",
					"pose": "11.727300 -2.093740 0 0 0 0"
				},
				"embed_model_81": {
					"model": "oak_tree_mini",
					"name": "tree_16",
					"pose": "11.636100 -1.341640 0 0 0 0"
				},
				"embed_model_82": {
					"model": "oak_tree_mini",
					"name": "tree_16",
					"pose": "6.169830 -1.006910 0 0 0 0"
				},
				"embed_model_83": {
					"model": "oak_tree_mini",
					"name": "tree_17",
					"pose": "1.298290 -2.406160 0 0 0 0"
				},
				"embed_model_84": {
					"model": "ambulance_mini",
					"name": "ambulance",
					"pose": "11.465000 -2.144160 0 0 0 0"
				}	
				
			},
```

The gazebo world will look like the image below:

![SAMPLE TRACK Img_1](<.gitbook/assets/gf_sample_1.png>)

![SAMPLE TRACK Img_1](<.gitbook/assets/gf_sample_2.png>)

![SAMPLE TRACK Img_1](<.gitbook/assets/gf_sample_3.png>)


{% hint style="warning" %}
This is just a _**sample world for the grand Finale Round**_. 
{% endhint %}


{% hint style="info" %}
In Grand Finale round, there will be both moving and static obstacles. More obstacles will be added in these rounds. Positions  and direction of traffic signs (& lights) will be changed.{% endhint %}

### Make traffic light change colour during simulation
{% hint style="info" %}
The sample world was updatd on 12th August,2022. Please use the updated traffic light positions given below
{% endhint %}
In  _**spawn\_light.py**_  file, replace the content of the file with following lines of code:
```import os
from time import sleep

spawn_green="gz model --spawn-file=/home/manish/ros2ws/nxp_gazebo/models/traffic_light_green/model.sdf --model-name=lightGreen -x 1.883040 -y 7.477359 -z 0.785598 -R 3.132084 -P -0.000383 -Y 1.615736"
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
