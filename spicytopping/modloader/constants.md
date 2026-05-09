# Constants

There are a few constants you can use if you need them for any reason:

```SCREEN_WIDTH``` The width of the screen.  
```SCREEN_HEIGHT``` The height of the screen.  
```MOD_PATH``` This is the directory of the current mod. Not actually a constant, but a variable that each mod loader object has.  

There's also the states enum if you need to know the player and enemy states. Similarly to **MOD_PATH**, it's not an actual enum, but rather a struct.  
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