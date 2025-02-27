---
description: For GRAND FINALE!
---

# UPDATE: TRACK SIZE

### The dimensions of the track: [**nxp\_raceway\_2**](changing-track.md#track-2)  have been updated.&#x20;

To update the the new dimensions of the track, go to \~**/ros2ws/nxp\_gazebo/models/nxp\_raceway\_2** folder in the setup and replace the code present in **`nxp_raceway.sdf`** with the updated code given below:

```
<?xml version="1.0" ?>
<sdf version="1.5">    
  <model name='nxp_raceway'>
    <pose>0 0 0 0 0 0</pose>
    <link name='nxp_raceway_link'>
      <visual name='nxp_raceway_inside_visual'>
        <cast_shadows>0</cast_shadows>
        <pose>0 0 -.008 0 0 0</pose>
        <geometry>
          <mesh>
            <scale>1.5 1.5 1</scale>
            <uri>model://nxp_raceway_2/meshes/CourseInside.stl</uri>
          </mesh>
        </geometry>
        <material>
          <script>
            <name>Gazebo/White</name>
            <uri>file://media/materials/scripts/gazebo.material</uri>
          </script>
        </material>
      </visual>
      <visual name='nxp_raceway_border_visual'>
        <cast_shadows>0</cast_shadows>
        <pose>-.02 -.03 0 0 0 0</pose>
        <geometry>
          <mesh>
            <scale>1.5 1.5 1</scale>
            <uri>model://nxp_raceway_2/meshes/CourseBorder.stl</uri>
          </mesh>
        </geometry>
        <material>
          <script>
            <name>Gazebo/Black</name>
            <uri>file://media/materials/scripts/gazebo.material</uri>
          </script>
        </material>
      </visual>
    </link>
    <static>1</static>
  </model>
</sdf>
```

{% hint style="success" %}
\[UPDATE NEW]: Line number 24 is edited to remove blurring of black lines on track boundary
{% endhint %}
