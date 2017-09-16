Original readme: (https://github.com/aybe/Quake/blob/master/readme.txt)

**The main goal/ideas of this fork are:**
- building under Visual Studio 2017
- minimal code changes, maximum re-use of existing infrastructure/code
- proper joystick support for XBox 360/One controller through XInput, with deadzone and non-linear response for better aiming
- added previous/next weapon commands
- TODO enable resolutions higher than 1280x1024 to accomdate today's screens
- TODO fullscreen shader for things like CRT emulation

All these things are [*conditional*](https://github.com/aybe/Quake/blob/master/WinQuake/Config.h).

**The changes compared to the original release:**
- assembly optimization disabled (still runs smoothly since today's PCs are much faster)
- OpenGL version is disabled

**Binaries**

https://github.com/aybe/Quake/releases

**Joystick**

Here's an example of AUTOEXEC.CFG with a default layout for the XBox 360/One Controller:

```
joystick 1
joyadvanced 1

joyforwardsensitivity 1.0
joysidesensitivity 1.0
joypitchsensitivity -1.0
joyyawsensitivity 1.0

joyforwardthreshold 0.4
joysidethreshold 0.4
joyyawthreshold 0.25
joypitchthreshold 0.25

+mlook
joyadvancedupdate

bind "AUX5" "+jump" // left shoulder
bind "AUX8" "pause" // start
bind "AUX11" "+speed" // left trigger
bind "AUX12" "+attack" // right trigger
bind "AUX32" "impulse 12" // d-pad left, previous weapon
bind "AUX30" "impulse 10" // d-pad right, next weapon
```
