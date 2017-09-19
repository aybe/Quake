Original readme: (https://github.com/aybe/Quake/blob/master/readme.txt)

## This fork features
- Visual Studio 2017 project
- proper joystick support for XBox 360/One controller, with deadzone and non-linear response for better aiming
- added previous/next weapon commands

## This fork changes
- assembly optimization disabled
- OpenGL version is disabled

## Notes

### To start clean, i.e. Quake that compiles in VS2017, runs, and without any changes

Start from this commit: [Uninitialized variables](https://github.com/aybe/Quake/commit/4437c317832a6ae350675ab6ffec260de956e471)

## Binaries

https://github.com/aybe/Quake/releases (with aforementioned features)

## Joystick

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
