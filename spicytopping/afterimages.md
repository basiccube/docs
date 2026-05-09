# Custom Afterimage Color Sets

Since the July 2nd, 2025 build, custom afterimage color sets can be added into the mod.  
These are loaded from the "afterimages" folder in Spicy Topping's AppData directory, that being `%appdata%\PizzaTower_SE\afterimages`.  
If the folder doesn't exist then just create it yourself.  

Any afterimages added in this folder appear as selectable values in the mod configuration menu for the `Afterimage Color Set` setting.

You specify a set of light color values, then dark color values (there have to be the same amount of dark colors as there are light colors!), and then a name for the color set.
All colors have to be a hex color value.  
Once you're done, save the file as a .json file in the folder mentioned earlier.

Example:
```json
{
	"light" : ["#202020", "#404040", "#808080"],
	"dark" : ["#101010", "#202020", "#404040"],
	"name" : "Example Color Set"
}
```