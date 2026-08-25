# RS90 OPENDINGUX
## Concepts
RS90 port is based on original [libretro](https://github.com/libretro) / **[frodo-libretro](https://github.com/libretro/frodo-libretro)** port, and has all the problems it has at this point, so what you expect from it is applied to this port.
This fork also compiles and works on other systems, but you just get what original provides

General recommendations  are:
* Use single-disk games, I might fix this in future but this is out of RS90 port scope
* Expect crackling, RS90 is no racer, but in 90% it is just fine
* Don't forget there is a on-screen keyboard, so you are not left in wilds :)
* For some yet unknown reason original port can not change disks, use an option in retroarch to restart it whole
* All controls are mapped at joystick in port 1, but half the games expect joystick in port 2, so you do everything needed in preparations using defaults, and then switch to port 2 in options when you play, but this renders all the controls besides joystick 2 useless

## Controls
There is two modes, original and shifted. R button acts as a (caps-)lock style shift button, so you click it, not hold it.  Mode is indicated in bottom left corner with **R ON**/**R OFF** text.

Original:
* *A* - Joystick fire
* *DPad* - joystick control
* *B* - Open on-screen keyboard (use *DPad* and *A* to navigate)
* *Start* - prints classic «LOAD"*",8,1» and «RUN», useful to start D64's
* *Select* - Return
* *L* - Run/Stop
* *R* - Shift toggle

Shifted:
* *A* - F1
* *B* - F3
* *Start* - F5
* *DPad* - Cursor keys

## Building
You need `rs90-toolchain` with `mipsel-rs90-linux-musl-gcc` and `mipsel-rs90-linux-musl-g++`
There is a way to define path to it, using `RS90_TOOLCHAIN=<path>` make argument, default is `~/rs90/rs90-toolchain`
So your build command could be something like `make platform=rs90 RS90_TOOLCHAIN=<your path>`
