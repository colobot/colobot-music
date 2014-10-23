# Colobot: Gold Edition - music files
This reporitory contains music tracks for Colobot: Gold Edition project (https://github.com/colobot/colobot) and is an optional addition to game's data files (https://github.com/colobot/colobot-data).
It currently includes:
* Original music from Colobot game, composed by **Daniel Roux**
 * musicXXX.flac files, they were taken from original game CD
* New audio tracks, composed by **Emxx52** ([forum](http://colobot.info/forum/memberlist.php?mode=viewprofile&u=68), [GitHub](https://github.com/Emxx52))
 * "Constructive Destruction" - Constructive.flac
 * "Humanitarian" - Humanitaian.flac
 * "Humanitarian v2 - The Box" - Hv2.flac
 * "Prototype" - Prototype.flac
 * "Quite Busy" - Quite.flac
 * "Infinite Storm v2 - Being Approximately Overcharged" - Infinite.flac
* New main menu intro music, composed by **PiXeL** ([forum](http://colobot.info/forum/memberlist.php?mode=viewprofile&u=243))
 * Intro1.ogg
 * Intro2.ogg

# File formats and installation
This repository contains files in FLAC format. However, the game can only play OGG files, so they need to be converted first - it's done like this so we can keep high quality music available, but reduce the file size for use in Colobot data files. This is done by CMake scripts included with this repository, but they require "oggenc" to be installed in your system.

# Licensing
All music files on this reporitory are licensed under GPLv3 license.
* The rights to redistribute original music files were given to TerranovaTeam along with the source code.
* Emxx52 puts his music on our forum and allows us to distribute it with the game - [forum topic (Polish)](http://colobot.info/forum/viewtopic.php?p=3242#p3242)
* The same applies to PiXeL's intro music - [forum post (Polish)](http://colobot.info/forum/viewtopic.php?f=17&t=354&p=3505#p3505)
