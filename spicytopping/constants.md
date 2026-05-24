# Constants

Here's some constants that can be used wherever you can execute code in the mod (most likely via the addon system).  
Constants will be added over time.  

```SCREEN_WIDTH``` The width of the screen.  
```SCREEN_HEIGHT``` The height of the screen.  

Sounds:  
```
sfx_bumpwall
sfx_collect
sfx_cardcollect
sfx_cowkick
sfx_explosion
sfx_groundpound
sfx_jump

sfx_player_dive
sfx_player_jump
sfx_player_machbump
sfx_player_step
sfx_player_stepinshit
```

There's also the states enum (internally it's a struct) if you need to know the player and enemy states.  
State list:  
```
normal
jump

crouch
crouchjump
ladder

backbreaker
parry

mach1
mach2
mach3

machslide
crouchslide
climbwall

tumble
machroll

bump
hurt

gottreasure
keyget
victory

door
comingoutdoor

taxi
policetaxi

timesup
gameover
ejected

chainsaw
tackle
enemytackle

arenaintro
actor
animation

portal
graffiti
bossintro
thrown
stunned
transition
transitioncutscene

handstandjump
punch
slap
faceplant
chainsawbump

grab
finishingblow
superslam
tacklecharge

shotgun
shotgunshoot

lungeattack
lungegrab
pummel
blockstance
supergrab
playersuperattack
shoulderbash

titlescreen
bombdelete

Sjump
Sjumpprep
Sjumpland

freefall
freefallprep
freefallland
facestomp

slipbanan
slipnslide
golf
tube
balloon

rideweenie
ridecow
motorcycle

trashjump
trashroll

stringfling
stringjump
stringfall

trickjump
jetpackjump
spiderweb

skateboard
grind
hook

grabbed
hit
gotoplayer
debugstate

ratmount
ratmounthurt
ratmountjump
ratmountcrouch
ratmountladder
ratmountattack
ratmountspit
ratmountclimbwall
ratmountgroundpound
ratmountbounce
ratmountballoon
ratmountgrind
ratmounttumble
ratmountpunch
ratmounttrickjump
ratmountskid

knightpep
knightpepattack
knightpepbump
knightpepslopes

bombpep
bombpepup
bombpepside
bombgrab

fireass
firemouth
hotmouth

ghost
ghostpossess

mort
mortjump
mortattack
morthook

barrel
barreljump
barrelslide
barrelclimbwall

rocket
rocketslide

antigrav

cheeseball
cheeseballclimbwall

cheesepep
cheesepepjump
cheesepepfling
cheesepepstickside
cheesepepstickup
cheesepepstick
cheesepeplaunch

boxxedpep
boxxedpepjump
boxxedpepspin

animatronic

ice
snowball
snowballceiling
snowbigball

spring
springjump

machcancelstart
machcancel
noisecrusher
bombkick

pogo
wallcling
hookshot

jetpack
jetpackstart

revolver
dynamite
boots
slidekick

helicopter
helicopterfall
helicopterspin

mortnormal

marionormal
marioanim
mariodead

ball

custom1
custom2
custom3
custom4
custom5
custom6
custom7
custom8
custom9
custom10
custom11
custom12
custom13
custom14
custom15
custom16
custom17
custom18
custom19
custom20

idle
walk
stun
turn
secret
ratgrabbed
rage
bounce
charge
chase
land
grabbing
uppunch
shoulder
pizzaheadjump
```