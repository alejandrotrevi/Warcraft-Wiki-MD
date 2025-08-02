# API GetExpansionForLevel

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Expansion}}
Needs summary.
 expansionLevel = GetExpansionForLevel(playerLevel)

==Arguments==
:;playerLevel:{{apitype|number}}

==Returns==
:;expansionLevel:{{apitype|number}}

==Values==
{| class="sortable darktable zebra"
! Levels !! Expansion
|-
| align="center" | 1-30 || 0 (LE_EXPANSION_CLASSIC)
|-
| align="center" | 31-35 || 3 (LE_EXPANSION_CATACLYSM)
|-
| align="center" | 36-40 || 5 (LE_EXPANSION_WARLORDS_OF_DRAENOR)
|-
| align="center" | 41-45 || 6 (LE_EXPANSION_LEGION)
|-
| align="center" | 46-50 || 7 (LE_EXPANSION_BATTLE_FOR_AZEROTH)
|-
| align="center" | 51-60 || 8 (LE_EXPANSION_SHADOWLANDS)
|-
| align="center" | 61-70 || 9 (LE_EXPANSION_DRAGONFLIGHT)
|-
| align="center" | 71-80 || 10 (LE_EXPANSION_WAR_WITHIN)
|}

==Patch changes==
* {{Patch 9.0.1|note=Removed <code>useLegacy</code> argument.}}
* {{Patch 8.2.5|note=Added.}}
```