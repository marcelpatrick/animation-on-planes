# animation-on-planes

- download pluggin: Animated Texture with GIF Importer
  - Copy the pluggins folder and copy inside your UE project folder

- Import your GIF files into your UE project.
  - They will be automatically converted to BaseTexture format
  
- Create a material
  - Set blend mode to masked
  - Make it so that its base color and emissive comes from a texture:
  -   Add a texture sample Param2d to be the input parameter of these material attributes - link it to base color and emissive color

- Create a material instance out of the material
  - Assign the texture with the GIF to this instance's Param2d: in Parameter Groups > Global texture parameter values > Texture

- Put a plain into the world
  - Assign the material instance to the plain
  
