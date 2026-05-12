# Characters

Custom characters can be added by creating a "characters" folder in your addon, creating another folder within there (the name for this one can be anything, it doesn't matter), and then having a character.json file in there, which specifies some required information for your character.

The folder structure should look like this for your custom character:
```
(addon folder)/
	characters/
		(character folder name)/
			character.json
			sprites/
				(add sprites in this folder)
```

The character.json file itself should have the following keys:

```name``` The name of your character.  
```id``` Your character's ID. Preferably use a short series of letters for it and ensure that it doesn't overlap with any other custom characters.   
```baseID``` The character that your custom one will be based off of.  
> The following characters are allowed to be used for the `baseID` key:  
	```"P"``` (Peppino)  
	```"N"``` (The Noise)  
	```"V"``` (Vigilante)  

Example:
```json
{
	"name" : "Example Character",
	"id" : "EX",
	"baseID" : "P"
}
```

Sprites are placed in the character's "sprites" folder, see the [Sprites](spicytopping/addonsystem/addon/sprites) page for more info.