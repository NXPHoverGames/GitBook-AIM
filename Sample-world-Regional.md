# Sample Simulation World for Regional Finale

## Sample world (without obstacles)
This is a practice simulation world,  which particpants can use to develope there own algorithms for self driving around the track.

{% hint style="warning" %}
Teams have to submit a video on this world to be eligible for region finale.
{% endhint %}

To access the world in simulation, there are two different approaches:

### Option-1

Download the following file and copy paste it content in _**models_config.json**_ file present in  _**~/cognipilot/cranium/AIM_2024_launcher**_ directory. After that run the launcher script by executing following commands:

 ```
$ cd ~/cognipilot/cranium/AIM_2024_launcher
$ python launch_sim.py start
```

{% file src=".gitbook/assets/AIM_2024/models_config_only_tack.json" %}
Sample world without obstacles json file
{% endfile %}

### Option-2

Download the following file and copy paste it content in _**Raceway_1.sdf**_ file present in  _**~/cognipilot/cranium/src/dream_world/worlds**_  directory. 

{% file src=".gitbook/assets/AIM_2024/Raceway_1_only_track.sdf" %}
Sample world without obstacles sdf file
{% endfile %}

After that you need to follow the steps mentioned on Running of AIM 2024 software stack and Updating Code Base for AIM 2024  gitbook pages

### Output

After following the above steps, the Simulation world should look like this:

![](<.gitbook/assets/AIM_2024/only_track_1.png>)

![](<.gitbook/assets/AIM_2024/only_track_2.png>)


## Sample world (with obstacles)
This is a practice simulation world,  which particpants can use to develope there own algorithms for self driving around the track and avoid obstacles.

{% hint style="warning" %}
This is just a sample world. In regional finale, there will be more obstacles and simulation world will be unkown.
{% endhint %}

To access the world in simulation, there are two different approaches:

### Option-1

Download the following file and copy paste it content in _**models_config.json**_ file present in  _**~/cognipilot/cranium/AIM_2024_launcher**_ directory. After that run the launcher script by executing following commands:

 ```
$ cd ~/cognipilot/cranium/AIM_2024_launcher
$ python launch_sim.py start
```

{% file src=".gitbook/assets/AIM_2024/models_config_sample_world.json" %}
Sample world json file
{% endfile %}

### Option-2

Download the following file and copy paste it content in _**Raceway_1.sdf**_ file present in  _**~/cognipilot/cranium/src/dream_world/worlds**_  directory. 

{% file src=".gitbook/assets/AIM_2024/Raceway_1_sample_world.sdf" %}
Sample world sdf file
{% endfile %}

After that you need to follow the steps mentioned on Running of AIM 2024 software stack and Updating Code Base for AIM 2024  gitbook pages

### Output

After following the above steps, the Simulation world should look like this:

![](<.gitbook/assets/AIM_2024/sample_world_0.png>)

![](<.gitbook/assets/AIM_2024/sample_world_1.png>)

![](<.gitbook/assets/AIM_2024/sample_world_2.png>)



## Advance Sample World (only for reference)


{% hint style="warning" %}
All teams are advised to finish the above sample world before proceeding further, as Regional Finale will be an upgradation from the sample world given in previous section and not the advance sample world{% endhint %}

This is a very advance  practice simulation world whcich covers majority of edge and tricky use cases.Particpants can use this world to further enhance their logic after they have succesfully completed a lap on sample world provided in previous section.

{% hint style="warning" %}
This is just a sample world, it's extremly tough and very hard to achieve as it covers majority of edge and tricky use cases for car to move. All teams are recommended to **primarly focus on sample world given above this advance sample world to prepare for regional finale**.  
{% endhint %}

To access the world in simulation, there are two different approaches:

### Option-1

Download the following file and copy paste it content in _**models_config.json**_ file present in  _**~/cognipilot/cranium/AIM_2024_launcher**_ directory. After that run the launcher script by executing following commands:

 ```
$ cd ~/cognipilot/cranium/AIM_2024_launcher
$ python launch_sim.py start
```

{% file src=".gitbook/assets/AIM_2024/models_config_sampleAdvanceWorld.json" %}
Advance Sample world json file
{% endfile %}

### Option-2

Download the following file and copy paste it content in _**Raceway_1.sdf**_ file present in  _**~/cognipilot/cranium/src/dream_world/worlds**_  directory. 

{% file src=".gitbook/assets/AIM_2024/Raceway_1_advance_sample_world.sdf" %}
Advance Sample world sdf file
{% endfile %}

After that you need to follow the steps mentioned on Running of AIM 2024 software stack and Updating Code Base for AIM 2024  gitbook pages

### Output

After following the above steps, the Simulation world should look like this:

![](<.gitbook/assets/AIM_2024/advance world.png>)

