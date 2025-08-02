# API BankButtonIDToInvSlotID

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Maps a BankButtonID to InventorySlotID.
 invSlot = BankButtonIDToInvSlotID(buttonID [, isBag])

==Arguments==
:;buttonID:{{apitype|number}} - bank item/bag ID.
:;isBag:{{apitype|number?}} - if buttonID is a bag, nil otherwise.  Same result as [[API ContainerIDToInventoryID|ContainerIDToInventoryID]], except this one only works for bank bags and is more awkward to use.

==Returns==
:;invSlot:{{apitype|number}} - An [[API TYPE InventorySlotID|inventory slot ID]] that can be used in other [[World of Warcraft API#Inventory Functions|inventory functions]]
```