# Overview

Driven Assimilators and Rogue Servitors with the Shattered Ring origin do not have their biological (Cyborg Species/Bio-Trophies) species' habitability preference set to ringworld.  Because other biological empires with the same origin are forced into that habitability preference, this is an unfair advantage for these already-powerful machine empire types.  This mod fixes that by tacking on an extra event after intial empire Pops are generated to adjust habitability for these empire types if they have Origin: Shattered Ring.

# Changes

This mod adds a single extra event which is triggered after each empire's capital planet is initialized.  The new event only executes its effects for Driven Assimilators and Rogue Servitors with the origin Shattered Ring.  The event finds all non-main, non-robotic species on the empire's capital planet and changes their ideal habitability to Ringworld (`pc_ringworld_habitable`).

## Compatibility

Should be compatible with almost anything.  If other mods add new origins which also start on a ringworld, this mod will **not** affect them.

## Known Issues

Because of how species modification at game start works, you will have an "extra" species with no Pops in your species tab with the original planetary preference from empire design (it will be named "Obsolete").  The game will hide it after a day or two of gameplay.

## Changelog

* 1.0.0 Initial version