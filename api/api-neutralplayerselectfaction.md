# API NeutralPlayerSelectFaction

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Allows a Pandaren to choose a faction.
 NeutralPlayerSelectFaction(factionIndex)

==Arguments==
:;factionIndex:{{apitype|number}} - 1 to choose the Horde, 2 to choose the Alliance.

==Details==
* Available to neutral Pandaren characters after completing the [[Wandering Isle storyline]].
* {{api|t=e|SHOW_FACTION_SELECT_UI}} indicates that a faction choice can be made.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|IsPlayerNeutral}}
```