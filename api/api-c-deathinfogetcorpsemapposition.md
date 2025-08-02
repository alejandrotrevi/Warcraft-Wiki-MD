# API C DeathInfo.GetCorpseMapPosition

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_DeathInfo|system=DeathInfo}}
Returns the location of the player's corpse on the map.
 position = C_DeathInfo.GetCorpseMapPosition(uiMapID)

==Arguments==
:;uiMapID:{{apitype|number}} : [[UiMapID]]

==Returns==
:;position:{{apitype|Vector2DMixin?}} - Returns nil when there is no corpse.

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```