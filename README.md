# Colobot: Gold Edition - music files
## THIS REPO IS CURRENTLY FOR TESTING GIT LFS - It's not being used officially yet !!
This repository contains music tracks for Colobot: Gold Edition project (https://github.com/colobot/colobot) that are an optional addition to game's data files (https://github.com/colobot/colobot-data). This repository also includes CMake scripts for converting them from high-quality FLAC to OGG format usable by the game.

The files in this repository are hosted using [Git LFS](https://git-lfs.github.com/), make sure you install it before cloning.

The music files currently include:
* Original music from Colobot game, composed by **Daniel Roux** and prepared by **CoLoRaptor** to be also as stand-alone soundtrack album in the Vorbis meta-tags (by adding titles to every track and changing queue, that would be more suited to album release). This music was taken from original game CD.
 * Track 01: "CoLoBoT Main Theme" - music011.flac
 * Track 02: "Leaving Earth - NASA Exercises" - music002.flac
 * Track 03: "The First Unknown World - Nature of Natives" - music003.flac
 * Track 04: "Crystalium - System Failure" - music004.flac
 * Track 05: "Saari's Heat" - music005.flac
 * Track 06: "Eruption" - music006.flac
 * Track 07: "Centaury - The Lost Hope" - music007.flac
 * Track 08: "Infinite Storm" - music008.flac
 * Track 09: "Terranova - Our New Home" - music009.flac
 * Track 10: "You Win!" - music012.flac
 * Track 11: "You Lose..." - music010.flac
 * Track 12: "Jazz Buzzing EasterEgg" - music013.flac
* New audio tracks, composed by **Emxx52** ([forum](http://colobot.info/forum/memberlist.php?mode=viewprofile&u=68), [GitHub](https://github.com/Emxx52)), also available [on SoundCloud](https://soundcloud.com/emxx-fiftytwo/sets/colobot-gold-edition-soundtrack)
 * "Constructive Destruction" - Constructive.flac
 * "Humanitarian" - Humanitaian.flac *(not available in-game yet)*
 * "Humanitarian v2 - The Box" - Hv2.flac
 * "Infinite Storm v2 - Being Approximately Overcharged" - Infinite.flac *(not available in-game yet)*
 * "Proton Ame" - Proton.flac *(not available in-game yet)*
 * "Prototype" - Prototype.flac
 * "Quite Busy" - Quite.flac
 * "Quite Busy v2 - Echoes of the Sand" - Qv2.flac *(not available in-game yet)*
 * "Under Construction - Terralice Theme" - Terralice.flac *(not available in-game yet)*
 * "Deviated Distortion Imminent" - Distortion.flac *(not available in-game yet)*
 * "Dispersion Circumstance" - Dispersion.flac *(not available in-game yet)*
 * "Sequential Deed Request" - Deed.flac *(not available in-game yet)*
 * "Substantial Processing" *(not available in-game yet)*
* New main menu intro music, composed by **PiXeL** ([forum](http://colobot.info/forum/memberlist.php?mode=viewprofile&u=243))
 * Intro1.ogg
 * Intro2.ogg

# File formats and installation
The files in this repository are available in FLAC format (except for Intro files - we still don't have FLACs for them :/). However, the game can only play OGG files, so FLACs need to be converted first - it's done like this so we can keep high quality music available, but reduce the file size for use in Colobot data files. The conversion can be done by CMake scripts included here, but they require "oggenc" to be installed in your system.
You can change the quality of OGG files by setting MUSIC_QUALITY in CMake (this can be any value in range -1 - 10 including fractions, default is 3)


# Licensing
All music files on this reporitory are licensed under GPLv3 license.
* The rights to redistribute original music files were given to TerranovaTeam along with the source code.
* Emxx52 puts his music on our forum and allows us to distribute it with the game - [forum topic (Polish)](https://colobot.info/forum/showthread.php?tid=177&pid=2858#pid2858)
* The same applies to PiXeL's intro music - [forum post (Polish)](https://colobot.info/forum/showthread.php?tid=177&pid=2525#pid2525)
