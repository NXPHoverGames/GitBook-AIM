# Sample Simulation World for Regional Finale

This is a practice simulation world,  which particpants can use to develope there own algorithms for self driving around the track and avoid obstacles.

{% hint style="warning" %}
This is just a sample world. In regional finale, there will be more obstacles and simulation world will be unkown.
{% endhint %}

To access the world in simulation, there are two different approaches:

## Opttion-1

Download the following file and copy paste it content in _**models_config.json**_ file present in  _**~/cognipilot/cranium/AIM_2024_launcher**_ directory. After that run the launcher script by executing following commands:

 ```
$ cd ~/cognipilot/cranium/AIM_2024_launcher
$ python launch_sim.py start
```

{% file src=".gitbook/assets/AIM_2024/models_config_sampleWorld.json" %}
Sample world json file
{% endfile %}

## Opttion-2

Download the following file and copy paste it content in _**Raceway_1.sdf**_ file present in  _**~/cognipilot/cranium/src/dream_world/worlds **_ directory. 

{% file src=".gitbook/assets/AIM_2024/Raceway_1_sample.sdf" %}
Sample world sdf file
{% endfile %}

After that you need to follow the steps mentioned on Running of AIM 2024 software stack and Updating Code Base for AIM 2024  gitbook pages

