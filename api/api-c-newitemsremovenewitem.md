# API C NewItems.RemoveNewItem

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Clears the "new item" flag.
 C_NewItems.RemoveNewItem(containerIndex, slotIndex)

==Arguments==
:;containerIndex:{{apitype|number}} : [[bagID]] - container slot id.
:;slotIndex:{{apitype|number}} - slot within the bag to clear the "new item" flag for.

==Patch changes==
* {{Patch 5.4.0|note=Added.}}

==See also==
* {{api|C_NewItems.ClearAll}}
```