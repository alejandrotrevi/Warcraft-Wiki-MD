# API GetRuneCount

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Returns the Death Knight's number of runes for a slot.
 count = GetRuneCount(runeIndex)

==Arguments==
:;runeIndex:{{apitype|number}} - Ranging from 1 to 6 which correspond to the available rune slots from left to right.

==Returns==
:;count:{{apitype|number}} - 1 if the rune is available and not on cooldown or 0 if the rune is on cooldown.

==Details==
To find out how many runes the player has available to spend:

 total = 0
 for i=1,6 do
     total = total + GetRuneCount(i)
 end
 print(total)

==Patch changes==
* {{Patch 3.0.2|note=Added.}}

==See also==
*{{api|GetRuneCooldown}}
```