# Character Events

Character events are basically just [events](spicytopping/addonsystem/addon/events), but specifically for the player and are only executed when the player is a custom character. Some events should return either `true` or `false`, which is useful if you want to override a certain action.

The code files for these are placed within a character's "events" folder, so it should be like this: `(addon folder)\characters\(character folder)\events\(event name).gml`

## Available Events

`OnPlayerHurt` Player gets hurt  
`UpdatePlayerSounds` Player sounds update  

`jump` Player jumps. Return `true` to override the code  

Crouch:  
`crouch/start` Player crouches. Return `true` to override the code  
`crouch/precrouch` Before the crouch state code  
`crouch/postcrouch` After the crouch state code  
`crouch/jump` Player crouch jumps. Return `true` to override the code  
`crouch/prejump` Before the crouch jump state code  
`crouch/postjump` After the crouch jump state code  

Crouchslide:  
`crouchslide/start` Player does crouchslide. Return `true` to override the code  
`crouchslide/precrouchslide` Before the crouchslide state code  
`crouchslide/postcrouchslide` After the crouchslide state code  

Mach Run:  
`machrun/premach1` Before the mach1 state code  
`machrun/postmach1` After the mach1 state code  
`machrun/premach2` Before the mach2 state code  
`machrun/postmach2` After the mach2 state code  
`machrun/premach3` Before the mach3 state code  
`machrun/postmach3` After the mach3 state code  
`machrun/dive` Player does dive. Return `true` to override the original code  

Wall Climb:  
`climbwall/preclimbwall` Before the climbwall state code  
`climbwall/postclimbwall` After the climbwall state code  
`climbwall/walljump` Player jumps off a wall during a wall climb. Return `true` to run the original code afterwards  
`climbwall/hitceiling` Player hits the ceiling during a wall climb. Return `true` to run the original code afterwards  
`climbwall/out` Players reaches top of wall and enters mach state. Return `true` to run the original code afterwards  

Freefall:  
`freefall/land` Player lands after a body slam. Return `true` to override the code  
`freefall/landslope` Player lands on a slope after a body slam. Return `true` to override the code  
`freefall/prefreefall` Before the freefall state code  
`freefall/postfreefall` After the freefall state code  
`freefall/preland` Before the freefall land state code  
`freefall/postland` After the freefall land state code  
`freefall/divecancel` Player does dive groundpound. Return `true` to override the code  

Super Jump prep:  
`superjump/prepstart` Player enters super jump prep. Return `true` to override the code  
`superjump/preprep` Before super jump prep code  
`superjump/postprep` After super jump prep code  
`superjump/preprelease` Player releases key to do super jump. Return `true` to override the code  

Super Jump old prep:  
`superjump/preoldprep` Before old super jump prep code  
`superjump/postoldprep` After old super jump prep code  
`superjump/oldpreprelease` After animation ends for old super jump prep. Return `true` to override the code  

Super Jump:  
`superjump/presjump` Before super jump code  
`superjump/postsjump` After super jump code  

Super Jump cancel:  
`superjump/cancelstart` Player does super jump cancel. Return `true` to override the code  
`superjump/precancel` Before super jump cancel code  
`superjump/postcancel` After super jump cancel code  

Attacks (return `true` to override original code):  
`attacks/grab` Player activates grab attack  
`attacks/shoulderbash` Player activates shoulder bash attack  
`attacks/faceplant` Player activates faceplant attack  
`attacks/slap` Player activates slap attack  
`attacks/kungfu` Player activates kung fu attack  
`attacks/pummel` Player activates pummel attack  
`attacks/breakdance` Player activates breakdance attack  
`attacks/pistol` Player activates pistol attack  
`attacks/chainsaw` Player activates chainsaw attack  
`attacks/uppercut` Player activates uppercut  

`attacks/noisespin` Player activates spin attack  
`attacks/noisehookshot` Player activates hookshot attack  
`attacks/noisebomb` Player activates bomb attack  

Grab attack:  
`attacks/pregrab` Before grab code  
`attacks/postgrab` After grab code  

Uppercut:  
`attacks/preuppercut` Before uppercut code  
`attacks/postuppercut` After uppercut code  

Breakdance:  
`attacks/prebreakdance` Before breakdance code  
`attacks/postbreakdance` After breakdance code  

Faceplant:
`attacks/prefaceplant` Before faceplant code  
`attacks/postfaceplant` After faceplant code  