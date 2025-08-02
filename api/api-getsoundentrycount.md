# API GetSoundEntryCount

**Contributor:** Meorawr

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of sound entries a sound kit contains.
 entryCount = GetSoundEntryCount(soundKit)

==Arguments==
:;soundKit:{{apitype|number}} - A sound kit ID.

==Returns==
:;entryCount:{{apitype|number?}} - The number of sound entries this sound kit contains.

==Details==
* A sound entry typically refers to a distinct sound file that will be sampled when the sound kit is played.

==Patch changes==
* {{Patch 10.1.0|note=Added.}}
```