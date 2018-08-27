NOTE: THIS IS DEPRECATED!

I think I found a better way for mod support in dhewm3: by providing an SDK, similar to the original Mod SDK.  
See https://github.com/dhewm/dhewm3-sdk for details.  
It already contains Dentonmod and Classic Doom 3, and more will follow soon!

I'll only keep this stuff here for reference.


---------------------------------------

This repository contains doom3 mods based on the base game (*not* d3xp) ported to dhewm3.
Each mod is in its own branch, the master branch is copied from dhewm3's neo/game/ directory and will be updated if it's updated in dhewm3.
Mods can then easily be updated to those changes by merging the changes from master to the mod branches.

These mods are "linked" (as git submodules) in the https://github.com/DanielGibson/dhewm3-mods project. 
There you'll also find informations on how to compile the mods.

*** This means that you usually don't have to clone this repository ***

If you want to donate a port, just create pull request for master, I'll create a seperate branch from it and add it to the dhewm3-mods project.

The usual (easiest) way to port a mod is to make a diff between the mod's source and the Doom3 SDK and apply the resulting patch to the vanilla game source (from the master branch).
Afterwards usually some manual work must be done to resolve patching conflicts and get the mod to compile. Also, the CMakeLists.txt file must be adjusted (see dentonmod for examples).

Please note that currently I only accept mods that are released under the GPL license - the one used by Open Source Doom3 (i.e. *not* only the Doom3 SDK license) - because merging GPL code and SDK license code is illegal. So please get permission from the Mod authors first.

If you are a mod author and want to release your mod's sourcecode under GPL, but don't want to port it yourself (or don't have time) contact me, maybe I can help you :-)

Once d3xp (Resurrection of Evil) based mods (or their GPL'ed source) turn up, I'll create a similar project for that.


Cheers,

- Daniel
