# API GetDetailedItemLevelInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.6|tentative=1}}
Returns detailed item level info.
 effectiveILvl, isPreview, baseILvl = GetDetailedItemLevelInfo(itemID or itemString or itemName or itemLink)

==Arguments==
One of the following four ways to specify which item to query:
:;itemId:{{apitype|number}} - Numeric ID of the item. e.g. 30234 for [[Nordrassil Wrath-Kilt]]
:;itemName:{{apitype|string}} - Name of an item owned by the  player at some point during this play session, e.g. "Nordrassil Wrath-Kilt".
:;itemString:{{apitype|string}} - A fragment of the [[itemString]] for the item, e.g. "item:30234:0:0:0:0:0:0:0" or "item:30234".
:;itemLink:{{apitype|string}} - The full [[itemLink]].

==Returns==
:;effectiveILvl:{{apitype|number}} - same as in tooltip.
:;isPreview:{{apitype|boolean}} - True means it would have a + in the tooltip, a minimal level for item used in loot preview in encounter journal
:;baseILvl:{{apitype|number}} - base item level

==Details==
effectiveLevel:
* matches all the upgrades (WF/TF) applied to item
* does not show scaling down in timewalking instances - i.e. matches number in parenthesis in tooltip
* does not show correct item level for artifact off-hand items - it always stays as 750 instead of matching main hand

==Patch changes==
* {{Patch 7.1.0|note=Added.}}
```