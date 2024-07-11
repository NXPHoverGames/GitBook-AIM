# Adding obstacles into Gazebo simulation

## Sample Obstacles

Participants can download few sample obstacles that may be used in the final round from the given zip file:

{% file src=".gitbook/assets/AIM_S2/sample obstacles.zip" %}
sample obstacles
{% endfile %}

{% file src=".gitbook/assets/AIM_S2/sample_person1.zip" %}
sample person obstacle
{% endfile %}



Extract the contents of the above zip files at: _**\~/ros2ws/nxp\_gazebo/models**_

## Adding Static Obstacles

#### Location of obstacles

Participants can add a variety of different types of static/fixed obstacles into the simulation. A large number of sample obstacles are already provided in the software stack stored at **\~/ros2ws/osrf/models**

![Sample Representation of osrf/models sub folder](.gitbook/assets/AIM_S2/osrf.png)

Also, after downloading and extracting the contents of the above .zip folders, the participants will have obstacles present at _**\~/ros2ws/nxp\_gazebo/models**_

![Sample Representation of nxp\_gazebo/models sub folder ](.gitbook/assets/AIM_S2/gazeboM.png)

#### Adding obstacles into the simulation world

To add obstacles into the simulation environment, navigate to _**\~/ros2ws/src/sim\_gazebo\_bringup/config**_ in the software stack and open the **gen\_params.json **_****_ file.

To add obstacles navigate to the "embedded\_models" sub-tag in the "world\_params" tag. Now add any number of obstacles by following the example shown:

![Sample code snippet to add obstacles into Gazebo](.gitbook/assets/AIM_S2/jsonFile.png)

{% hint style="info" %}
Please make sure to save the file before running the simulation command and follow proper JSON syntax in the file
{% endhint %}

#### Explanation of code:

```
"embed_model_1": {
					"model": "start_point",
					"name": "start_point_0",
					"pose": "0.2 -0.45 0.09 0 0 0"
				}
```

* **"embed\_model\_{x}":** Represents a unique identifier tag for each obstacle/model to be spawned in the simulation world. This tag name should be unique for each model to be spawned into the simulation
* **"model":** It is the name of the model to be spawned into the simulation. This represents the name of the desired model that has to be spawned and is stored either in _**\~/ros2ws/nxp\_gazebo/models**_ or in **\~/ros2ws/osrf/models.**

{% hint style="info" %}
Please make sure the name of the model passed to the _"model:"_ parameter must be case sensitive as well as present in either of the mentioned folders&#x20;
{% endhint %}

* **"name":** It is a custom unique identifier given to each entity which allows Gazebo to keep track of each model spawned into the simulation.

{% hint style="info" %}
Use unique string values for the _"name"_ parameter for each obstacle to be added. As same value will not spawn the obstacles into simulation
{% endhint %}

* **"pose":** This parameter defines the position and orientation of models in simulation. It is represented by "x y z R P Y" where: **x is x-coordinate, y is y-coordinate, z is z-coordinate, R is roll, P is pitch and Y is yaw.**

## Adding Moving Obstacles

#### Creating Custom Plugin

To add moving obstacles into the simulation, the first thing to do is create a custom plugin for each separate obstacle that you wish to animate/ move in the simulation. This custom plugin will help the obstacle/model to move in a fixed path in simulation with fixed time stamps.

Tutorial for to create such plugins is available at: [http://gazebosim.org/tutorials?tut=animated\_box\&cat=build\_robot](http://gazebosim.org/tutorials?tut=animated\_box\&cat=build\_robot)

Tutorial to build and compile custom plugins is available at: [http://gazebosim.org/tutorials?tut=plugins\_hello\_world\&cat=write\_plugin](http://gazebosim.org/tutorials?tut=plugins\_hello\_world\&cat=write\_plugin)

#### Adding obstacle with  the plugin

To add moving obstacles into the simulation navigate to _**gen.world.jinja**_ located at _\~/ros2ws/nxp\_gazebo/worlds ****_ in the software stack. Navigate to **line 115.** Below this line use \<include> tags to spawn models into simulation and define their properties along with the plugin to be used. A sample is shown below:

![](.gitbook/assets/AIM_S2/moving.png)

{% hint style="warning" %}
Please make sure to provide the full path of the plugin to be used as many times gazebo have problems in locating custom plugin files
{% endhint %}
