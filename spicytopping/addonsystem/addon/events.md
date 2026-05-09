# Events

Events are pieces of code that are run when a certain action occurs. Each addon can add their own code, and it will be run during said action.  

The code needs to be placed within the addon's "events" folder. For example, if you want to run code when the addon is enabled, then within the addon folder the following file needs to exist: `(addon folder)\events\OnEnable.gml`

These are the events that currently exist:  
`OnEnable` Triggered when the addon is enabled.  
`OnDisable` Triggered when the addon is disabled.  

You can view the events an addon contains in the Addon Editor.