# API GetLootInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a table with all of the loot info for the current loot window.
 info = GetLootInfo()

==Returns==
:;info:{{apitype|table[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| isQuestItem || {{apitype|boolean?}} ||
|-
| item || {{apitype|string}} || Item Name, e.g. "Linen Cloth" or "65 Copper"
|-
| locked || {{apitype|boolean}} || Whether you are eligible to loot this item or not. Locked items are by default shown tinted red.
|-
| quality || {{apitype|number}} || Item [[Enum_Item.ItemQuality|Quality]]
|-
| quantity || {{apitype|number}} || The quantity of the item in a stack. The quantity for coin is always 0.
|-
| roll || {{apitype|boolean}} ||
|-
| texture || {{apitype|number}} || Texture [[FileID]]
|}

==Patch changes==
* {{Patch 6.0.2|note=Added.}}

==See also==
* {{api|GetLootSlotInfo}}
* {{api|t=e|LOOT_READY}} - When this event fires, the function will have new data available.
```