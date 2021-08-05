# Overview

Driven Assimilators and Rogue Servitors with the Shattered Ring origin do not have their biological (Cyborg Species/Bio-Trophies) species's habitability preference set to ringworld.  Because other biological empires with the same origin are forced into that habitability preference, this is an unfair advantage for these already-powerful machine empire types.  This mod fixes that by tacking on an extra event after intial empire Pops are generated to adjust habitability for these empire types if they have Origin: Shattered Ring.

This mod now also offers a graphical for for all Shattered Ring origins, and applies a similar habitability change to Driven Assimilators with a Resource Consolidation origin.

# Changes

This mod adds a three extra events which are triggered after each empire's capital planet is initialized.

The first event only executes its effects for Driven Assimilators and Rogue Servitors with the origin Shattered Ring.  The event finds all non-main, non-robotic species on the empire's capital "planet" and changes their ideal habitability to Ringworld (`pc_ringworld_habitable`).

The second event executes for every empire with the Shattered Ring origin.  The event switches the appearance of the starting ringworld to match the shipset selected by the empire, but has no gameplay impact.

The third event only executes its effects for Driven Assimilators (and Rogue Servitors - just in case) with the origin Resource Consolidation (aka Machine World).  The event finds all non-main, non-robotic species on the empire's capital planet and changes their ideal habitability to Machine World (`pc_machine`).

## Compatibility

Should be compatible with almost anything.  If other mods add new origins which also start on a ringworld or machine world, this mod will **not** affect them.

### When to Install

This mod can be safely added or removed from your save game after the game has started.  The code in this mod executes entirely during game setup - if the game was started with the mod, its effects have already been applied, otherwise no code executed.

## Known Issues

Because of how species modification at game start works, you will have an "extra" species with no Pops in your species tab with the original planetary preference from empire design (it will be named "Obsolete").  The game will hide it after a day or two of gameplay.

## Changelog

* 1.0.0 Initial version
* 1.0.1 Add info to README (no script changes)
* 1.0.2 Remove extra images files to keep distribution lightweight (no script changes)
* 1.0.3 Maintenance release: add logo to Steam description (no script changes)
* 1.1.0 Starting ringworld will match your species's shipset (graphical culture), Machine World preference for Resource Consolidation
    * Event sets the initial ringworld to use the same graphical culture (base game has slight variation)
    * Particularly notable for the Machine shipset, which has a custom ringworld
    * Special thanks to Nanderty for pursuing this graphical detail and FrozenParagon for help with megastructures
    * Driven Assimilators (or Rogue Servitors, if you modded for that) with Origin: Resource Consolidation start with biological pops having machine world habitability preference

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/ringworld_origin_rebalance)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.