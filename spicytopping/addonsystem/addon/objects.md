# Objects

Objects can be added by creating folders within the addon's "objects" folder. When the addon is enabled, the addon system searches for sub-folders within it and then adds them as objects that can then be used within your code.  
The folder names you specify is what it will use for the name of the objects, for example if you create the folder `(addon name)\objects\obj_example` then you use the name `obj_example` in the code when referring to it.

Each object sub-folder can contain it's own set of GML files which will be the code it'll run for the object events.

## Supported events
See the GameMaker manual for information on each object event listed here.  

The following events are supported:  
```create.gml``` Create  
```destroy.gml``` Destroy  
```cleanup.gml``` Cleanup  
```step.gml``` Step  
```beginstep.gml``` Begin Step  
```endstep.gml``` End Step  
```draw.gml``` Draw  
```drawbegin.gml``` Draw Begin  
```drawend.gml``` Draw End  
```drawgui.gml``` Draw GUI  
```drawguibegin.gml``` Draw GUI Begin  
```drawguiend.gml``` Draw GUI End  
```predraw.gml``` Pre-Draw  
```postdraw.gml``` Post-Draw  
```roomstart.gml``` Room Start  
```roomend.gml``` Room End  
```outsideroom.gml``` Outside Room  
```intersectboundary.gml``` Intersect Boundary  
```animationend.gml``` Animation End  
```alarm(0-11).gml``` Alarms  
```userevent(0-15).gml``` User Events  

## Constants

Constants that you can use in addon objects:  
```MOD_PATH``` This is the directory of the current addon. Not actually a constant, but a variable that each addon object has.  

You can find the rest of the constants [here](/spicytopping/constants).

## "with" statement
In the code, you cannot use **with** statements with addon objects in the same way as regular objects.  
There are two different methods you can use:

The simplest method is to use the **mith** function, it is meant to be a close enough replacement for the **with** statement.
For example, if you want to run code in all obj_example addon objects, you can do the following:
```gml
mith(obj_example, function()
{
	// code for obj_example here
})
```

Alternatively, the other method is to use the **with** statement and check all addon objects and see if its object name (which is in the addonObject struct) is the same as whatever the name of the object you're checking for.  

So, if you want to run code in the obj_example addon object using the **with** statement, you can do the following:
```gml
with (obj_addonObject)
{
	if (addonObject.name == obj_example.name)
	{
		// code for obj_example here
	}
}
```

```gml
with (obj_addonObject)
{
	if (addonObject.name != obj_example.name)
		continue;
		
	// code for obj_example here
}
```
