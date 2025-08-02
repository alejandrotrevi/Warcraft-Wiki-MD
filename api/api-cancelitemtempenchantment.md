# API CancelItemTempEnchantment

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|protected|note=Use the "cancelaura" action type of [[SecureActionButtonTemplate]] with the "target-slot" attribute set to [[InventorySlotId|weapon slot ID]].}}
Removes temporary weapon enchants (e.g. Rogue poisons and sharpening stones).
 CancelItemTempEnchantment(weaponHand)

==Arguments==
:;weaponHand:{{apitype|number}} - '''1''' for Main Hand, '''2''' for Off Hand.

==Patch changes==
* {{Patch 4.0.1|note=Protected.}}
```