# Addon Metadata (addon.json)

addon.json is how Spicy Topping recognizes the addon. It specifies various metadata that is both required for the addon to function and also useful for a player using your addon.

The file itself is a regular JSON file, that can contain the following keys:

```name``` The name of the addon that will appear in the addons menu.  
```desc``` A description for the addon, shown in the addons menu.  
```author``` The authors of the addon, shown in the addons menu.  
```version``` The mod's version number.  

An example:

```json
{
	"name" : "Example Addon",
	"desc" : "An example addon for Spicy Topping.",
	"author" : "basiccube",
	"version" : "1.0"
}
```

## Addon Icon

You can optionally add an icon for the addon that will be shown in the "Manage Addons" menu.  
Next to the addon.json file, add a 256x256 image with the name `icon.png`.