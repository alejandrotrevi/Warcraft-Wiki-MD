# API GetTradeTargetItemInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns item info for the other player in the trade window.
 name, texture, quantity, quality, isUsable, enchant = GetTradeTargetItemInfo(index)

==Arguments==
:;index:{{apitype|number}} - the slot (1-7) to retrieve info from

==Returns==
:;name:{{apitype|string}} - Name of the item
:;texture:{{apitype|string}} - Name of the item's texture
:;quantity:{{apitype|number}} - Returns how many is in the stack
:;quality:{{apitype|number}} - The item's quality (0-6)
:;isUsable:{{apitype|number}} - True if the player can use this item
:;enchant:{{apitype|string}} - enchant being applied (no trade slot)
```