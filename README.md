Find the original readme [here](https://github.com/aybe/Quake/blob/master/readme.txt).

## Features
- proper joystick support for XBox 360/One controller, with deadzone and non-linear response for better accuracy
- addition of  `previous` and `next` weapon commands

## Installation instructions
(tested under Windows 10 with the CD-ROM version of Quake that ships with DOS, Windows and OpenGL executables)
- download the archive of the latest release: https://github.com/aybe/Quake/releases
- unzip it to a directory of your choice, e.g. `C:\Quake`
- from the Quake CD-ROM, copy the `ID1` directory in the `Data` directory next to the executable
- you are now ready to run `WinQuake.exe`

### Installation notes

#### Display issues

If you didn't include `ID1\config.cfg` from the CD-ROM, the game will start but minimize itself a couple of times before finally starting. This is because on first start the game detects available display resolutions, this step however, behaves weirdly under a modern version of Windows.

#### Xbox controller

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

## Notes for developers
- the Visual Studio 2017 project builds for `Debug` and `Release` for `x86` only, this is because SciTech MGL was only shipped as a 32-bit library. It is now open-source and can be found [here](http://www.edm2.com/index.php/SciTech_MGL) or [here](https://github.com/kendallb/scitech-mgl) (not sure it's worth the effort, though).
- assembly optimizations, OpenGL version and QuakeWorld client have not been enabled
- for a barebone source without aforementioned features, checkout this commit instead: [Uninitialized variables](https://github.com/aybe/Quake/commit/4437c317832a6ae350675ab6ffec260de956e471)
