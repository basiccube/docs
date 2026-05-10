# Sprites

Sprites can be added by adding .png or .gif files into the addon's "sprites" folder, like this: `(addon folder)\sprites\spr_customsprite.png`.
PNG sprite strips are not supported yet.

When the addon is enabled, these sprites can be accessed in the code using its name (ex. if the file name is spr_customsprite.png, use spr_customsprite in the code), but **cannot be used using the regular draw_sprite functions!**. To use your custom sprites, you need to use the appropriate draw_image functions, for instance if you want to use the draw_sprite_ext function with your sprite, then use draw_image_ext instead.

Each sprite can contain an INI file next to it for overriding certain aspects of the sprite, in this case the origin and speed (frames per game frame).  

Example:
```ini
[Sprite]
Speed=0.5
OriginX=50
OriginY=50
```