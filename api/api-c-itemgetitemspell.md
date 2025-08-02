# API C Item.GetItemSpell

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Item|system=Item}}
Returns the spell effect for an item.
 spellName, spellID = C_Item.GetItemSpell(itemInfo)

==Arguments==
:;itemInfo:{{apitype|ItemInfo}} : {{:ItemInfo}}

==Returns==
:;spellName:{{apitype|string}} - The name of the spell.
:;spellID:{{apitype|number}} - The spell's unique identifier.

==Details==
* Useful for determining whether an item is usable.

==Patch changes==
* {{Patch 10.2.6|note=Added.}}
```