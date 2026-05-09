# mod.json

This file specifies metadata that is required for the mod to function. Without it, the mod loader will not recognize the mod.

It's a very straightforward JSON file, that can contain the following values:

```name``` The name of the mod that appears in the mod manager menu.  
```desc``` A description for the mod, shown when the mod is selected in the mod manager menu.  
```author``` The authors of the mod, shown when the mod is selected in the mod manager menu.  
```version``` The mod's version number.  
```type``` Mod type. Only value currently that does anything is ```"character"```.  

> **If the mod is meant to be a character reskin mod (which is set via the ```"character"``` mod type), then the following values are required:**  
```characterData``` A struct, containing values specifically for character reskin mods.  
Can contain these values:
> * ```characterName``` Character name that appears in the character picker.  
> * ```baseCharacter``` The character that the character reskin will be based off of.  
	Allowed values are:  
	```"P"``` (Peppino)  
	```"N"``` (The Noise)  
	```"V"``` (Vigilante)  
> * ```characterID``` ID for the character reskin. Make sure that the character ID you're using doesn't overlap with any other character reskin mods.  

Some examples:

```json
{
	"name" : "Example Mod",
	"desc" : "An example mod for the mod loader implementation in Spicy Topping.",
	"author" : "basiccube",
	"version" : "1.0",
}
```

```json
{
	"name" : "Example Character Mod",
	"desc" : "An example character for the character system.",
	"author" : "basiccube",
	"version" : "1.0",
	"type" : "character",
	
	"characterData" :
	{
		"characterName" : "Example Character",
		"baseCharacter" : "P",
		"characterID" : "EC",
	},
}
```