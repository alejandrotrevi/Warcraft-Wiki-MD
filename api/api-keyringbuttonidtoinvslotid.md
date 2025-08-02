# API KeyRingButtonIDToInvSlotID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Map a keyring button to an inventory slot button for use in inventory functions.
 invSlot = KeyRingButtonIDToInvSlotID(buttonID)

==Arguments==
:;buttonID:{{apitype|number}} - key ring button ID.

==Returns==
:;invSlot:{{apitype|number}} - an [[API TYPE InventorySlotID|inventory slot ID]].

==Patch changes==
====<font color="#4ec9b0">Retail</font>====
* {{Patch 4.2.0|note=Removed.}}
* {{Patch 1.11.0|note=Added.}}

====<font color="#4ec9b0">Classic</font>====
* {{Patch 1.13.3|note=Added.}}
```