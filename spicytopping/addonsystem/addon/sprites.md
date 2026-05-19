# Sprites

Sprites can be added by adding .png or .gif files into the addon's "sprites" folder, like this: `(addon folder)\sprites\spr_customsprite.png`.
The files can alternatively be put within sub-folders, so this something like this would work as well: `(addon folder)\sprites\coolsprites\spr_customsprite.png`.  

PNG files in particular can also be sprite strips, for these to work just add `_strip(sub-image count)` to the end of the file name, for example `spr_customsprite_strip5.png`.

> It is highly recommended that you use PNGs for sprites and avoid using GIFs entirely, as GIFs both eat up a lot more memory and take way longer to load compared to PNG files.

When the addon is enabled, these sprites can be accessed in the code using its name like any other sprite (ex. if the file name is spr_customsprite.png, use spr_customsprite in the code). If you're using a sprite strip, then the `_strip` part of the file name will be removed from the sprite name.

## Sprite INI Files

Each sprite can contain an INI file next to it for overriding certain aspects of the sprite, such as the origin and speed.  
The INI file name needs to be the same name as the sprite file name (just with .ini as the file extension). If you're using a sprite strip, it can be either the name of the file with `_strip` at the end or you can omit it entirely, like this: `spr_customsprite.ini` or `spr_customsprite_strip5.ini`.

The following keys can be in the `Sprite` section of the INI file:  
`Speed` The speed of the sprite (frames per game frame)  
`OriginX` The sprite's X origin  
`OriginY` The sprite's Y origin  
`CenterOrigin` Sets the sprite to use a origin point in the center if the origin X and Y aren't already specified

Examples:
```ini
[Sprite]
Speed=0.5
OriginX=50
OriginY=50
```

```ini
[Sprite]
CenterOrigin=1
```