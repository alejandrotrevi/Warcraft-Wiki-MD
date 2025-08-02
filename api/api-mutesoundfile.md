# API MuteSoundFile

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Mutes a sound file.
 MuteSoundFile(sound)

==Arguments==
:;sound:{{apitype|number,string}} - [[FileID]] of a game sound or file path to an addon sound.

==Example==
<onlyinclude>Plays the [https://wow.tools/files/#search=Spells/LevelUp.ogg Sound/Spells/LevelUp.ogg] sound
 /run PlaySoundFile(569593)
Mutes it, the sound won't play
 /run MuteSoundFile(569593); PlaySoundFile(569593) 
Unmutes it and plays it
 /run UnmuteSoundFile(569593); PlaySoundFile(569593)</onlyinclude>

==Details==
* Muted sound settings only persist through relogging and /reload. They have to be muted again after restarting the game client.
* This works on all internal game sounds, addon sounds and sounds played manually by {{api|PlaySoundFile}}()
* There is no API to replace sound files.

==Finding Sound IDs==
{{:API_PlaySoundFile}}

==Addon example==
Mutes the [https://wow.tools/files/#search=sound/spells/fizzle,type:ogg fizzle] sounds.
<syntaxhighlight lang="lua">
local sounds = {
	569772, -- sound/spells/fizzle/fizzleholya.ogg
	569773, -- sound/spells/fizzle/fizzlefirea.ogg
	569774, -- sound/spells/fizzle/fizzlenaturea.ogg
	569775, -- sound/spells/fizzle/fizzlefrosta.ogg
	569776, -- sound/spells/fizzle/fizzleshadowa.ogg
}

for _, fdid in pairs(sounds) do
	MuteSoundFile(fdid)
end
</syntaxhighlight>

==Patch changes==
* {{Patch 8.2.0|note=Added. (Build 30948 Jun 27 2019)}}
```