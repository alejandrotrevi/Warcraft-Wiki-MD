# API PlaySoundFile

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Plays the specified sound by [[FileDataID]] or addon file path.
 willPlay, soundHandle = PlaySoundFile(sound [, channel])

==Arguments==
:;sound:{{apitype|number,string}} - Either a [[FileDataID]], or the path to a sound file from an addon.
::* The file must exist prior to logging in or reloading. Both .ogg and .mp3 formats are accepted. 
:;channel:{{apitype|string?|default=SFX}} - The sound channel.
{{:API_PlaySound}}

==Returns==
:;willPlay:{{apitype|boolean}} - true if the sound will be played, nil otherwise (prevented by a muted sound channel, for instance).
:;soundHandle:{{apitype|number}} - identifier for the queued playback.

==Example==
Plays a sound file included with your addon and ignores any sound setting except the master volume slider:
* Both slash <code>/</code> or escaped backslashes <code>\\</code> can be used as file separators.
 PlaySoundFile("Interface\\AddOns\\MyAddOn\\mysound.ogg", "Master")

Plays the level up sound:
 -- <s>by file path</s> (dropped in 8.2.0)
 PlaySoundFile("Sound/Spells/LevelUp.ogg")

 -- by FileDataID [https://wow.tools/files/#search=569593 569593] (added support in 8.2.0)
 PlaySoundFile(569593)

 -- by SoundKitID {{dbc|soundkitentry#search=888|888}} (SoundKitName {{dbc|soundkitname#search=levelup|LEVELUP}})
 {{api|PlaySound}}(888)

==Finding Sound IDs==
<onlyinclude>File Data IDs
* By file name/path, e.g. [https://wow.tools/files/#search=Spells/LevelUp,type:ogg Spells/LevelUp,type:ogg] in wow.tools
* By SoundKitID, e.g. [https://wow.tools/files/#search=skit:888 skit:888] in wow.tools
* By sound kit name with https://wow.tools/files/sounds.php
* With the Sound ID Finder addon: https://www.curseforge.com/wow/addons/sound-id-finder
Sound Kit Names/IDs
* From the sounds tab for an NPC, for example https://www.wowhead.com/npc=154304/waveblade-shaman#sounds
* By sound kit name with https://www.wowhead.com/sounds and {{dbc|soundkitname|SoundKitName.db2}}
* IDs used by the FrameXML are defined in the [https://github.com/Gethe/wow-ui-source/blob/live/Interface/SharedXML/SoundKitConstants.lua SOUNDKIT] table
* The full list of IDs can be found in {{dbc|soundkitentry|SoundKitEntry.db2}}</onlyinclude>

==Patch changes==
* {{Patch 8.2.0|note=Updated to accept FileDataIDs due to the removal of file paths.<sup>[https://github.com/Stanzilla/WoWUIBugs/issues/7]}}</sup>

==See also==
* {{api|PlaySound}} - Plays a sound by SoundKitID
* {{api|StopSound}}
* {{api|MuteSoundFile}} - Mutes a sound
* {{api|UnmuteSoundFile}}
```