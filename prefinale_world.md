# Evaluation World For Pre-Finale Round

## Adding Static Obstacles

To add obstacles into the simulation environment, navigate to _**\~/ros2ws/src/sim\_gazebo\_bringup/config**_ in the software stack and open the _**gen\_params.json**_ file.

To add obstacles navigate to the "embedded\_models" sub-tag in the "world\_params" tag. Then copy the following code:

```"embed_model_0": {
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
				},
				"embed_model_45": {
					"model": "start_point",
					"name": "start_point_0001",
					"pose": "6.305489 1.876002 0 0 0 0"
				},
				 "embed_model_48": {
					"model": "barricade",
					"name": "barricade",
					"pose": "2.194609 -1.300408 0.018361 -0.093369 -0.009292 0"
				},
				 "embed_model_51": {
					"model": "car_blue",
					"name": "car62",
					"pose": "6.771580 0.623883 0 0 0 0"
				},
				
			          "embed_model_58": {
					"model": "car_blue",
					"name": "car63",
					"pose": "6.774790 1.007196 0 0 0 0"
				},
			          "embed_model_59": {
					"model": "car_blue",
					"name": "car64",
					"pose": "6.781790 0.823987 0 0 0 0"
				},
			          "embed_model_60": {
					"model": "postbox2",
					"name": "postbox_2",
					"pose": "6.707060 -4.025880 0 0 0 0"
				},
			          "embed_model_61": {
					"model": "postbox2",
					"name": "postbox_3",
					"pose": "6.873150 -4.212660 0 0 0 0"
				},
			          "embed_model_62": {
					"model": "postbox2",
					"name": "postbox_4",
					"pose": "7.157350 -4.368260 0 0 0 0"
				},
			          "embed_model_63": {
					"model": "oak_tree_mini",
					"name": "tree_4",
					"pose": "7.443300 -4.516780 0 0 0 0"
				},
			          "embed_model_64": {
					"model": "oak_tree_mini",
					"name": "tree_5",
					"pose": "7.727030 -4.570390 0 0 0 0"
				},
			          "embed_model_65": {
					"model": "oak_tree_mini",
					"name": "tree_6",
					"pose": "7.960390 -4.552590 0 0 0 0"
				},
			          "embed_model_69": {
					"model": "fire_hydrant2",
					"name": "fire_hydrant_5",
					"pose": "8.310840 -3.954310 0 0 0 0"
				},
			          "embed_model_70": {
					"model": "postbox2",
					"name": "postbox_5",
					"pose": "6.707060 -4.025880 0 0 0 0"
				},
			          "embed_model_71": {
					"model": "fire_hydrant2",
					"name": "fire_hydrant_6",
					"pose": "8.485060 -3.880990 0 0 0 0"
				},
			          "embed_model_72": {
					"model": "car",
					"name": "car1",
					"pose": "5.964630 -0.569309 0 0 0 0"
				},
			          "embed_model_73": {
					"model": "car",
					"name": "car2",
					"pose": "8.089680 3.431590 0 0 0 0"
				},
			          "embed_model_77": {
					"model": "car_red",
					"name": "car6",
					"pose": "2.798470 7.770910 0 0 0 0"
				},
			          "embed_model_78": {
					"model": "car_blue",
					"name": "car7",
					"pose": "3.219050 7.743590 0 0 0 -0.722550"
				},
			          "embed_model_79": {
					"model": "car",
					"name": "car11",
					"pose": "2.379117 7.836338 0 0 0 -0.722550"
				},
			          "embed_model_80": {
					"model": "car_blue",
					"name": "car12",
					"pose": "3.019249 7.028828 0 0 0 -0.722550"
				},
			          "embed_model_81": {
					"model": "car",
					"name": "car13",
					"pose": "2.240290 7.064150 0 0 0 -0.722550"
				},
			          "embed_model_90": {
					"model": "oak_tree_mini",
					"name": "tree_18",
					"pose": "9.798663 5.240543 0 0 0 0"
				},
			          "embed_model_91": {
					"model": "oak_tree_mini",
					"name": "tree_19",
					"pose": "9.713505 4.396950 0 0 0 0"
				},
			          "embed_model_92": {
					"model": "oak_tree_mini",
					"name": "tree_20",
					"pose": "9.656664 4.021600 0 0 0 0"
				},
			          "embed_model_93": {
					"model": "oak_tree_mini",
					"name": "tree_21",
					"pose": "9.749110 5.729170 0 0 0 0"
				},
			          "embed_model_94": {
					"model": "oak_tree_mini",
					"name": "tree_22",
					"pose": "9.573650 6.120090 0 0 0 0"
				},
			          "embed_model_95": {
					"model": "oak_tree_mini",
					"name": "tree_23",
					"pose": "9.475110 6.494870 0 0 0 0"
				}
				
			},

```

## Adding Moving Obstacles
First download the given .zip file and save it in _**\~/ros2ws/nxp\_gazebo/**_ directory.

{% file src=".gitbook/assets/custom_pluggins.zip" %}
plugins for moving obstacles
{% endfile %}

![code snippet](.gitbook/assets/dir_custom_plugin.png)

To add moving obstacles into the simulation navigate to _**gen.world.jinja**_ located at _**\~/ros2ws/nxp\_gazebo/worlds **_ in the software stack. Navigate to _**line 115.**_ 
Below this line instert following lines of code:
```
    <include>
      <uri>model://car_blue</uri>
      <name>moving_car</name>
      <pose>-1.562250 3.107690 0 0 0 0</pose>
      <plugin name="push_animate" filename="/home/manish/ros2ws/nxp_gazebo/custom_pluggins/car_animation/build/libanimated_car.so"/>
    </include>
    
    <include>
      <uri>model://person_1</uri>
      <name>moving_person_1</name>
      <pose>-2.071470 0.387716 0.018239 0 0 1.612632</pose>
      <plugin name="push_animate2" filename="/home/manish/ros2ws/nxp_gazebo/custom_pluggins/person_animation_x_dir/build/libanimated_person_xDir.so"/>
    </include>
    
    <include>
      <uri>model://person_1</uri>
      <pose>2.603500 0.543162 0.018239 0 0 0</pose>
      <name>moving_person_2</name>
      <plugin name="push_animate3" filename="/home/manish/ros2ws/nxp_gazebo/custom_pluggins/person_animation_y_dir/build/libanimated_person_yDir.so"/>
    </include>
```
{% hint style="warning" %}
Please make sure to provide the full path of the plugin to be used as many times gazebo have problems in locating custom plugin files. 
Also replace the /home/manish/ros2ws with the path in your own system.
{% endhint %}

![code snippet](.gitbook/assets/world_file.png)

## Make traffic light change colour during simulation
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


## Pre-finale World Visualised
The gazebo world will look like the image below:

![SAMPLE TRACK Img_1](<.gitbook/assets/prefinale_track_1.png>)

![SAMPLE TRACK Img_2](<.gitbook/assets/prefinale_track_2.png>)

![SAMPLE TRACK Img_3](<.gitbook/assets/prefinale_track_3.png>)

![SAMPLE TRACK Img_3](<.gitbook/assets/prefinale_track_4.png>)