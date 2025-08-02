# API C Heirloom.GetHeirloomInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Returns information about a heirloom by itemID
 name, itemEquipLoc, isPvP, itemTexture, upgradeLevel, source, searchFiltered, effectiveLevel, minLevel, maxLevel = C_Heirloom.GetHeirloomInfo(itemID)

==Arguments==
:;itemID:{{apitype|number}} - a heirloom itemID

==Returns==
:;name:{{apitype|string}} - false if not a heirloom item
:;itemEquipLoc:{{apitype|string}}
:;isPvP:{{apitype|boolean}}
:;itemTexture:{{apitype|string}}
:;upgradeLevel:{{apitype|number}}
:;source:{{apitype|number}} - heirloom source index
:;searchFiltered:{{apitype|boolean}}
:;effectiveLevel:{{apitype|number}}
:;minLevel:{{apitype|number}}
:;maxLevel:{{apitype|number}}
```