# Adding Obstacles in Simulation World

## Get all models to be used in Regional Finale
Below zip file contains all the gazebo models to be used in Regional Finale:

{% file src=".gitbook/assets/AIM_2024/obstacles.zip" %}
Gazebo obstacles
{% endfile %}

Download and extract the obstacles in the following folder: __**~/cognipilot/cranium/src/dream_world/models**_

After extraction your folder should look like this:

![](.gitbook/assets/AIM_2024/model_dir.png)

## Adding Obstacles in Simulation World

To add obstacles to appear at start of simulation, you need to add model information to be included in the world file. To do this navigate to folder:  _**~/cognipilot/cranium/src/dream_world/worlds**_
And open the _**Raceway_1.sdf**_ file to include the information of various obstacles to be included in the simulation world at the start.

![](.gitbook/assets/AIM_2024/world_dir.png)

After the last _</scene>_ tag at the end of world file, we will add the information related to the models/obstacles to be spawned at the start. Refer to below image for more information:

{% hint style="info" %}Only models that are present in __**~/cognipilot/cranium/src/dream_world/models**_ directory can be included into the simulation by this method. {% endhint %}

![](.gitbook/assets/AIM_2024/world_file.png)

