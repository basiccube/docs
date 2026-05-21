# Sounds

Sounds can be added by placing audio files in the addon's "sounds" folder, for example: `(addon folder)\sounds\sfx_mysound.ogg`.  
Plenty of file formats should work, but the ones you preferably should be using are either .wav or .ogg files.

When the addon is enabled, you can then use these sound files in your code using the file name specified (ex. `sfx_mysound.wav` would be `sfx_mysound` in code) and with the sound_* functions listed below.

## Sound INI Files

Sounds can also have an .ini file next to them to specify some additional parameters, like volume and whether it's meant to be used as a 3D sound effect. The INI file name needs to be the same name as the name of the audio file (but with .ini as the file extension), like this: `sfx_mysound.ini`.

The following sections and parameters can be in the INI file:  
* _`loopPoints`_ section:  
`start` The starting point of the loop in milliseconds  
`end` The end point of the loop in milliseconds  

* _`sound`_ section:  
`volume` Volume of the sound effect (from 0 to 1)  
`3D` Specifies if this is a sound effect meant to be used in 3D  

Example:
```ini
[sound]
volume=0.175
3D=1
```

## Sound Functions

These are the functions you need to use if you want to play your custom sound files.  
The sound constants in [Constants](spicytopping/constants) work and **only** work with the `sound_play` and `sound_play_3d` functions.  

`sound_play(snd)` Plays a sound in 2D  
`sound_play_3d(snd, x, y)` Plays a sound in 3D at the specified position  
`sound_stop(snd)` Stops the specified sound  
`sound_update_position(snd, x, y)` Updates the position of a sound that is currently playing  
`sound_is_playing(snd)` Returns if a sound is playing  
`sound_is_paused(snd)` Returns if a sound is paused  
`sound_pause(snd, pause)` Sets the sound to be paused or not  
`sound_get_length(snd)` Returns the length of the sound in milliseconds  

The following functions are for more advanced use. Do not use them if you don't understand what any of them do!  
Some functions here are used for very specific purposes in the game.  

(function arguments contained in square brackets are optional)  

`fmod_create(event_name)` Creates an instance of the specified event  
`fmod_release(event_instance)` Deletes an event instance, freeing up memory  
`fmod_destroy(event_instance)` Immediately stops and deletes the event instance  

`fmod_play(event_name)` Plays an event in 2D  
`fmod_play_3d(event_name, x, y)` Plays an event at the specified position  
`fmod_play_unique(event_name, x, y)` Plays an event at the specified position and stops any existing identical events that were played using this function  
`fmod_play_instance(event_instance)` Plays an event instance  
`fmod_play_instance_3d(event_instance, x, y)` Plays an event instance at the specified position  
`fmod_stop(event_instance, [immediate] = false)` Stops an event instance. 'immediate' lets you either forcefully stop the instance or let it fade out (if the event is meant to fade out)  

`fmod_set_position(event_instance, x, y)` Updates the position of the event instance  
`fmod_is_playing(event_instance)` Returns if the event instance is playing  
`fmod_is_paused(event_instance)` Returns if the event instance is paused  
`fmod_pause(event_instance, pause)` Sets the event instance to be paused or not  

`fmod_get_length(event_instance)` Returns the length of the event instance in milliseconds  
`fmod_get_timelinepos(event_instance)` Returns the current position in the event instance's timeline  
`fmod_set_timelinepos(event_instance, position)` Sets the current position in the event instance's timeline  

`fmod_get_event_name(event_instance)` Returns the name of the event instance  
`fmod_is_same(event_instance, event_name)` Returns if the name of the event instance is the same as the specified event name  

`fmod_stop_bus(bus_path, immediate)` Stops all sounds playing in the audio bus. 'immediate' specifies if the events should be forcibly stopped  
`fmod_pause_bus(bus_path, pause)` Sets the audio bus to be paused or not  

> Audio buses:  
`bus:/sfx` Sound effects  
`bus:/music` Music  

`fmod_get_global(parameter)` Gets the value of a global variable  
`fmod_set_global(parameter, value, [ignore_seek] = true)` Sets the value of a global variable  

> Global variables:  
`musicmuffle` Muffled music state  
`pillarfade` Music fade out when near Pillar John  
`masterVolume` Master game volume  
`musicVolume` Music volume  
`sfxVolume` Sound effects volume  
`focus` Game window focus  
`noise` Player is The Noise  
`noisecampaign` Player is in Noise campaign  
`totem` Reduce volume of music, from 0 to 2 (used by totems, treasure collect, gustavo/peppino switch intro)  
`clones` Affects volume of fake peppino boss sounds depending on how many clones there are  

`fmod_get_value(event_instance, parameter)` Gets the value of an event instance's parameter  
`fmod_set_value(event_instance, parameter, value, [ignore_seek] = true)` Sets the value of an event instance's parameter  

> Commonly used music parameters are:  
`state` For different sections of the level  
`stateA`, `stateB`, `stateC` Music variants  

Sound file functions (use the sound_* ones above instead):  
`fmod_create_sound_2d(path, [bus] = "bus:/sfx")` Creates a 2D sound from the specified file path  
`fmod_create_sound_3d(path, [bus] = "bus:/sfx")` Creates a 3D sound from the specified file path  
`fmod_release_sound(sound)` Stops and deletes a sound  

`fmod_play_sound(sound, [paused] = false)` Plays a sound. 'paused' argument is meant for internal use only  
`fmod_play_sound_3d(sound, x, y)` Plays a sound at the specified position  
`fmod_stop_sound(sound)` Stops a sound  

`fmod_set_sound_position(sound, x, y)` Sets the sound's position  
`fmod_is_sound_playing(sound)` Returns if a sound is playing  
`fmod_is_sound_paused(sound)` Returns if a sound is paused  
`fmod_pause_sound(sound, pause)` Sets the sound to be paused or not  
`fmod_get_sound_length(sound)` Returns the length of the sound in milliseconds  