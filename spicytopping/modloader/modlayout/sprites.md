# "sprites" folder

This folder is where the mod loader will search for sprites.  
Only PNG and GIF files are supported. If the sprite is a PNG file, then the PNG needs to be a sprite strip for it to work properly.

When a mod is enabled, these sprites can then be accessed within the code using its name (ex. if the file name is spr_customsprite.gif, use spr_customsprite in the code).
For character reskins, the sprites are meant to be named after the sprite variables (use mod_dumpcharspritenames to figure out the names to use).  

Each sprite can contain an INI file next to it for overriding certain aspects of the sprite, in this case the width, origin and speed (frames per game frame).  
You cannot override the width on GIF sprites.

Example:
```ini
[Sprite]
Width=100
Speed=0.5
XOrigin=50
YOrigin=50
```