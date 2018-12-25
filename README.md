# DirectDraw Force Refresh Rate
This repo is a small collection of windows registry files for common monitor refresh rates that, when merged, force DirectDraw's refresh rate.

## Why?
Some games have wonky display implementations. For example: in Metal Gear Rising, if you try to play the game at 1080p with full-screen it (for reasons unknown) tries to run in 24hz. If your monitor doesn't support 24hz, your screen will probably lose signal and the game will probably crash.
Using these registry files, we can force DirectDraw to use our own specified refresh rate (ie. to match the monitor), fixing the problem.

## Usage
1. Identify the appropriate .reg file for your computer. For example, if your monitor supports 60hz and your operating system is 64-bit, you would use `dd_force_060hz_64bit.reg`.
2. Merge the previously identified .reg file by double-clicking it and accepting the warnings. No restart required.
3. Play your game as normal.
4. When you're finished playing, merge `dd_force_clear.reg` by double-clicking it and accepting the warnings. This will remove entries created by step 1 - you probably don't want to keep them in case it interferes with other games.