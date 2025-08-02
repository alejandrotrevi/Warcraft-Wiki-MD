# API EJ GetTierInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Get some information about the encounter journal tier for index.
 name, link = EJ_GetTierInfo(index)

==Arguments==
:;index:{{apitype|number}} - The index of the tier. Ranging from 1 to {{api|EJ_GetNumTiers}}(). See below for details.

==Returns==
:;name:{{apitype|string}} - The (localized) tier name.
:;link:{{apitype|string}} - The (localized) tier link.

==Details==
Tiers:
* 1 = Classic
* 2 = Burning Crusade
* 3 = Wrath of the Lich King
* 4 = Cataclysm
* 5 = Mists of Pandaria
* 6 = Warlords of Draenor
* 7 = Legion
*8 = Battle for Azeroth

==See also==
* {{api|EJ_GetCurrentTier}}
```