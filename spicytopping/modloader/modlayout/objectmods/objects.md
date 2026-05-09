# "objects" folder

This folder is scanned by the mod loader where it will then detect sub-folders within it and add them as objects. The folder names is what it will use for the object names.
Each object sub-folder contains it's own set of GML files which are the object events.

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

## "with" statement
In the code, you cannot use **with** statements with mod loader objects in the same way as regular objects.  
There are two different methods you can use:

The best and recommended method is to use the new **mith** function, this is meant to be a close enough replacement for the **with** statement, **mith** being "mod loader" and "with" combined into one word.  
For example, if you want to run code in all obj_example mod loader objects, you can do the following:
```gml
mith(obj_example, function()
{
	// code for obj_example here
})
```

Alternatively, the other method is to use the **with** statement and check all mod loader objects and see if its object name (which is in the objectInfo struct) is the same as whatever the name of the object you're checking for.  

So, if you want to run code in the obj_example mod loader object using the **with** statement, you can do the following:
```gml
with (obj_modloaderObject)
{
	if (objectInfo.name == obj_example.name)
	{
		// code for obj_example here
	}
}
```

```gml
with (obj_modloaderObject)
{
	if (objectInfo.name != obj_example.name)
		continue;
		
	// code for obj_example here
}
```

> If your code contains the **__OBJECT** struct in place of the **objectInfo** struct, it should still work for compatibility purposes but keep in mind that it is recommended that you use the **objectInfo** struct instead.