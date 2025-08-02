# API GetTotemTimeLeft

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns active time remaining (in seconds) before a totem (or ghoul) disappears.
 seconds = GetTotemTimeLeft(slot)

==Arguments==
:;slot:{{apitype|number}} - Which totem to query:
:* 1 - Fire (or Death Knight's ghoul)
:* 2 - Earth
:* 3 - Water
:* 4 - Air

==Returns==
:;seconds:{{apitype|number}} - Time remaining before the totem/ghoul is automatically destroyed

==Details==
* Totem functions are also used for ghouls summoned by a Death Knight (if the ghoul is not made a controllable pet by [[Raise_Dead_(death_knight_ability)|Raise Dead]] rank 2). 

==See also==
* {{api|GetTime}}
* {{api|GetTotemInfo}}
```