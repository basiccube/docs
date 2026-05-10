# Sprites

Sprites can be added by adding .png or .gif files into the addon's "sprites" folder, like this: `(addon folder)\sprites\spr_customsprite.png`.
PNG sprite strips are not supported yet.

When the addon is enabled, these sprites can be accessed in the code using its name like any other sprite (ex. if the file name is spr_customsprite.png, use spr_customsprite in the code).

Each sprite can contain an INI file next to it for overriding certain aspects of the sprite, in this case the origin and speed (frames per game frame).  

Example:
```ini
[Sprite]
Speed=0.5
OriginX=50
OriginY=50
```