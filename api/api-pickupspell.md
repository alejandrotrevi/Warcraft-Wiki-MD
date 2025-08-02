# API PickupSpell

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|nocombat|note=Restricted since patch 2.0}} {{deprecatedapi|patch=11.0.0}}
Places a spell onto the cursor.
 PickupSpell(spellID)

==Arguments==
:;spellID:{{apitype|number}} - spell ID of the spell to pick up.

==Details==
* This function will put a spell on mouse cursor.

==Patch changes==
* {{Patch 4.0.1|note=This function now takes a single <code>spellID</code> argument. The previous <code>(slot, "book")</code> version is available as {{api|PickupSpellBookItem}}.}}

==See Also==
* {{api|PickupAction}}, {{api|PickupPetAction}}, {{api|PickupBagFromSlot}}, {{api|PickupContainerItem}}, {{api|PickupInventoryItem}}, {{api|PickupItem}}, {{api|PickupMacro}}, {{api|PickupMerchantItem}}, {{api|PickupPlayerMoney}}, {{api|PickupStablePet}}, {{api|PickupTradeMoney}}
* {{api|ClearCursor}}
```