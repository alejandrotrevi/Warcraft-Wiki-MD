# API PlaySound

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Plays the specified sound by SoundKitID.
 willPlay, soundHandle = PlaySound(soundKitID [, channel, forceNoDuplicates, runFinishCallback])

==Arguments==
:;soundKitID:{{apitype|number}} - Sound Kit ID in {{dbc|soundkitentry|SoundKitEntry.db2}}. Sounds used in FrameXML are defined in the [https://github.com/Gethe/wow-ui-source/blob/live/Interface/SharedXML/SoundKitConstants.lua SOUNDKIT] table.
:;channel:{{apitype|string?|default=SFX}} - The sound channel.
<onlyinclude>{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Channel !! Toggle CVar !! Volume CVar<sup>[https://github.com/Gethe/wow-ui-source/blob/10.0.0/Interface/SharedXML/SettingDefinitions/Audio.lua#L432-L449]</sup>
|-
| <font color="#71d5ff"><code>Master</code></font> || {{apitooltip|type=cvar|Sound_EnableAllSound}} || {{apitooltip|type=cvar|Sound_MasterVolume}}
|-
| <code>Music</code> || {{apitooltip|type=cvar|Sound_EnableMusic}} || {{apitooltip|type=cvar|Sound_MusicVolume}}
|-
| <code>SFX</code> (Effects) || {{apitooltip|type=cvar|Sound_EnableSFX}} || {{apitooltip|type=cvar|Sound_SFXVolume}}
|-
| <code>Ambience</code> || style="padding-right: 1em" | {{apitooltip|type=cvar|Sound_EnableAmbience}} || {{apitooltip|type=cvar|Sound_AmbienceVolume}}
|-
| <code>Dialog</code> || {{apitooltip|type=cvar|Sound_EnableDialog}} || {{apitooltip|type=cvar|Sound_DialogVolume}}
|-
| <code>Talking Head</code><sup>[https://github.com/Gethe/wow-ui-source/blob/9.0.5/AddOns/Blizzard_TalkingHeadUI/Blizzard_TalkingHeadUI.lua#L199]</sup> || ||
|}
[[File:API_PlaySoundFile_channels.png|thumb|619px|right|Volume sliders in the interface options]]</onlyinclude>
:;forceNoDuplicates:{{apitype|boolean?|default=true}} - Allows duplicate sounds if false.
:;runFinishCallback:{{apitype|boolean?|default=false}} - Fires {{api|t=e|SOUNDKIT_FINISHED}} when the sound has finished playing, arg1 will be <code>soundHandle</code>.

==Returns==
:;willPlay:{{apitype|boolean}} - true if the sound will be played, nil otherwise (prevented by a muted sound channel, for instance).
:;soundHandle:{{apitype|number}} - identifier for the queued playback.

==Example==
Plays the ready check sound file (''sound/interface/levelup2.ogg'')
<syntaxhighlight lang="lua">
PlaySound(SOUNDKIT.READY_CHECK) -- by SOUNDKIT key
PlaySound(8960)                 -- by SoundKitID
</syntaxhighlight>
 {{api|PlaySoundFile}}(567478) -- by FileDataID

==Details==
* Sound Kit IDs are used to play a set of random sounds. For example the {{dbc|soundkitentry#colFilter%5B1%5D=exact%3A5980|human female NPC greeting}} sound kit refers to 5 different sounds.
<syntaxhighlight lang="lua">
/run PlaySound(5980)

-- will play one of these sounds
/run PlaySoundFile(552133) -- sound/creature/humanfemalestandardnpc/humanfemalestandardnpcgreeting01.ogg
/run PlaySoundFile(552141) -- sound/creature/humanfemalestandardnpc/humanfemalestandardnpcgreeting02.ogg
/run PlaySoundFile(552137) -- sound/creature/humanfemalestandardnpc/humanfemalestandardnpcgreeting03.ogg
/run PlaySoundFile(552142) -- sound/creature/humanfemalestandardnpc/humanfemalestandardnpcgreeting04.ogg
/run PlaySoundFile(552144) -- sound/creature/humanfemalestandardnpc/humanfemalestandardnpcgreeting05.ogg
</syntaxhighlight>

===Finding Sound IDs===
{{:API_PlaySoundFile}}

==Patch changes==
* {{Patch 7.3.0|note=Changed. String-based input is not allowed. SoundKitID should be given while calling ''PlaySound()''. This change is more like a replacement for {{api|PlaySoundKitID}}.}}
* {{Patch 7.0.3|note=Added fourth argument, <code>runFinishCallback</code>.}}
* {{Patch 5.0.4|note=Added <code>willPlay</code> and <code>soundHandle</code> return values.}}

==See also==
* {{api|PlaySoundFile}} - Accepts FileDataIDs and addon file paths.
* {{api|StopSound}}
```