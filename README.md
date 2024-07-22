# animation-on-planes

- download pluggin: Animated Texture with GIF Importer - https://github.com/neil3d/UAnimatedTexture5 
  - Copy the pluggins folder and copy inside your UE project root folder in the same location as the Contents folder

- Import your GIF files into your UE project.
  - They will be automatically converted to FileMediaSource format
 
- Create a MediaPlayer file
  - Select the option for UE to automatically create a Media Texture file out of it
  - Open the MediaPlayer file
  - In PlayBack options > Decoder > select Electra Player
  - and select the imported FileMediaSource with your GIF
  
- Create a material
  - Set blend mode to masked or Opaque
  - Make it so that its base color and emissive comes from a texture:
    - Add a texture sample Param2d to be the input parameter of these material attributes - link it to base color and emissive color
  - Add material params such as brightness, saturation etc to controll its quality
![image](https://github.com/user-attachments/assets/70a67eba-6c0d-4bf1-b1fd-676e05aeaf92)


- Create a material instance out of the material
  - Assign the media texture with the GIF to this instance's Param: in Parameter Groups > Global texture parameter values > Texture
  - Adjust material params if needed
 
- Open the media player
  - Select loop option
  - click on play for the gif animation to start playing on the material instance

- Put a plain into the world
  - Assign the material instance to the plain
  
