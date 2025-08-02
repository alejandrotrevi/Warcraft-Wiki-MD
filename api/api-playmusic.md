# API PlayMusic

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Plays the specified sound file on loop to the "Music" sound channel.
 willPlay = PlayMusic(sound)

==Arguments==
:;sound:{{apitype|number,string}} - [[FileDataID]] of a game sound or file path to an addon sound.

==Returns==
:;willPlay:{{apitype|boolean}} - Seems to always return true even for invalid file paths or FileDataIDs.

==Example==
Plays [https://music.apple.com/us/album/stormstout-brew/561372303?i=561372387 Stormstout Brew] from the [[Mists_of_Pandaria_Soundtrack#Track_list|Mists of Pandaria Soundtrack]]
 -- by file path (dropped in 8.2.0)
 PlayMusic("sound/music/pandaria/mus_50_toast_b_03.mp3")

 -- by FileDataID [https://wow.tools/files/#search=MUS_50_Toast_B 642878] (added support in 8.2.0)
 PlayMusic(642878)

==Details==
* If any of the built-in music is playing when you call this function (e.g. Stormwind background music), it will fade out.
* The playback loops until it is stopped with {{api|StopMusic}}(), when the user interface is reloaded, or upon logout. Playing a different sound file will also cause the current song to stop playing. It cannot be paused.
* OggVorbis (.ogg) files are supported since World of Warcraft uses the [https://www.fmod.com/ FMOD] sound engine.
* You can find a full list here: https://wow.tools/files/#search=sound/music

==Patch changes==
* {{Patch 8.2.0|note=Dropped support for internal file paths and accepts [[FileDataID]]s.}}
* {{Patch 7.1.0|note=Should once again work correctly. A bug was introduced in [[Patch 7.0.3]] that caused it to be non-functional.}}
* {{Patch 6.0.3|note=Should now work correctly and be able to play MP3s once more.}}
```