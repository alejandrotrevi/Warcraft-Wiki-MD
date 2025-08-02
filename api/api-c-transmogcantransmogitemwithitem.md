# API C Transmog.CanTransmogItemWithItem

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether an item can be transmogrified to look like another item.
 canBeTransmogrified, failReason = C_Transmog.CanTransmogItemWithItem(targetItem, sourceItem)

==Arguments==
:;targetItem:String/Number : item name, item link, or item ID of the item that will change its appearance
:;sourceItem:String/Number: item name, item link, or item ID of the item the appearance of which will be copied.

==Returns==
:;canBeTransmogrified:{{apitype|boolean}} - true if targetItem can be transmogrified to look like sourceItem, false otherwise.
:;failReason:String/nil - If the items cannot be transmogrified, a token indicating the cause:
:* "MISMATCH" - Items are of different types, or one of the items is a vanity item (e.g. [[Chef's Hat]]).
:* "NO_ITEM" - The character doesn't own both of the items involved.
:* "NO_STATS" - One of the items has no stats (e.g. [[Item suffix|an item with a random suffix]] identified by ID rather than link).
:* "LEGENDARY" - One of the items is legendary.
:* "INVALID_TYPE" - Item type cannot be used for transmogrification (e.g. non-equitable items, fishing poles)

==Patch changes==
* {{Patch 7.0.3|note=Moved from {{api|CanTransmogrifyItemWithItem}} to {{api|C_Transmog.CanTransmogItemWithItem}}.}}
```