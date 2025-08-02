# API C Map.GetMapLevels

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Map|system=MapUI}}
Returns the suggested player and battle pet levels for a map.
 playerMinLevel, playerMaxLevel, petMinLevel, petMaxLevel = C_Map.GetMapLevels(uiMapID)

==Arguments==
:;uiMapID:{{apitype|number}} : [[UiMapID]]

==Returns==
:;playerMinLevel:{{apitype|number}}
:;playerMaxLevel:{{apitype|number}}
:;petMinLevel:{{apitype|number?|default=0}}
:;petMaxLevel:{{apitype|number?|default=0}}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```