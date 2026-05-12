# Sprites

Sprites can be added by adding .png or .gif files into the addon's "sprites" folder, like this: `(addon folder)\sprites\spr_customsprite.png`.  
PNG files in particular can also be sprite strips, for these to work just add `_strip(sub-image count)` to the end of the file name, for example `spr_customsprite_strip5.png`.

When the addon is enabled, these sprites can be accessed in the code using its name like any other sprite (ex. if the file name is spr_customsprite.png, use spr_customsprite in the code). If you're using a sprite strip, then the `_strip` part of the file name will be removed from the sprite name.

Each sprite can contain an INI file next to it for overriding certain aspects of the sprite, in this case the origin and speed (frames per game frame).  

Example:
```ini
[Sprite]
Speed=0.5
OriginX=50
OriginY=50
```