# API StopSound

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Stops playing the specified sound.
 StopSound(soundHandle [, fadeoutTime])

==Arguments==
:;soundHandle:{{apitype|number}} - Playing sound handle, as returned by {{api|PlaySound}} or {{api|PlaySoundFile}}.
:;fadeoutTime:{{apitype|number?}} - In milliseconds.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}
```