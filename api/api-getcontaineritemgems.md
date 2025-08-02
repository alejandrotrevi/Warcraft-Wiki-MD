# API GetContainerItemGems

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns item IDs of gems inserted into the item in a specified container slot.
 gem1, gem2, ... = GetContainerItemGems(bag, slot);

==Arguments==
; bag : Number ([[BagID]]) - Index of the bag to query.
; slot : Number - Index of the slot within the bag to query, ascending from 1.

==Returns==
; gem1, gem2, ... : Number - Item IDs of the gems within the item in the specified container slot.

==Patch changes==
* {{Patch 7.0.3|note=Removed.}}
```