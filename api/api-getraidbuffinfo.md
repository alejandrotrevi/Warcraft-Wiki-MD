# API GetRaidBuffInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about [[Buff#List of notable buffs obtained from other players|raid buffs]] for the player.
 buffmask, buffcount = GetRaidBuffInfo()

==Returns==
:;buffmask:{{apitype|number}} - Bit mask of currently active raid buffs.
:;buffcount:{{apitype|number}} - The maximum number of raid buffs your current raid can provide.

==Details==
* Every bit in the buffmask represents one of the 8 raid buffs. It is set to 1 if the buff is currently active and set to 0 otherwise. The order is the following, beginning with the first bit: Stats, Stamina, Attack Power, Attack Speed, Spell Power, Spell Haste, Critical Strike, Mastery.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|GetRaidBuffTrayAuraInfo}}
```