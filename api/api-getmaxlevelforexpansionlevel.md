# API GetMaxLevelForExpansionLevel

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Expansion}}
Maps an expansion level to a maximum character level for that expansion.
 maxLevel = GetMaxLevelForExpansionLevel(expansionLevel)

==Arguments==
:;expansionLevel:{{apitype|number}}

==Returns==
:;maxLevel:{{apitype|number}}

==Values==
{| class="sortable darktable zebra col1-center col3-center"
! Value !! Enum !! MaxLevel
|-
| 0 || LE_EXPANSION_CLASSIC || 30
|-
| 1 || LE_EXPANSION_BURNING_CRUSADE || 30
|-
| 2 || LE_EXPANSION_WRATH_OF_THE_LICH_KING || 30
|-
| 3 || LE_EXPANSION_CATACLYSM || 35
|-
| 4 || LE_EXPANSION_MISTS_OF_PANDARIA || 35
|-
| 5 || LE_EXPANSION_WARLORDS_OF_DRAENOR || 40
|-
| 6 || LE_EXPANSION_LEGION || 45
|-
| 7 || LE_EXPANSION_BATTLE_FOR_AZEROTH || 50
|-
| 8 || LE_EXPANSION_SHADOWLANDS || 60
|}

==Patch changes==
* {{Patch 9.0.1|note=Removed <code>useModernLevelMapping</code>}}
* {{Patch 8.2.5|note=Added <code>useModernLevelMapping</code>}}
* {{Patch 7.3.2|note=Added.}}
```