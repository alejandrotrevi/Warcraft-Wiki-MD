# API GetWeaponEnchantInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for temporary weapon enchantments (e.g. sharpening stones).
 hasMainHandEnchant, mainHandExpiration, mainHandCharges, mainHandEnchantID, hasOffHandEnchant, offHandExpiration, offHandCharges, offHandEnchantID, hasRangedEnchant, rangedExpiration, rangedCharges, rangedEnchantID = GetWeaponEnchantInfo()

==Returns==
:;hasMainHandEnchant:{{apitype|boolean}} - ''true'' if the weapon in the main hand slot has a temporary enchant, ''false'' otherwise
:;mainHandExpiration:{{apitype|number}} - time remaining for the main hand enchant, as thousandths of seconds
:;mainHandCharges:{{apitype|number}} - the number of charges remaining on the main hand enchant
:;mainHandEnchantID:{{apitype|number}} - ID of the main hand enchant (new in 6.0)
:;hasOffHandEnchant:{{apitype|boolean}} - ''true'' if the weapon in the secondary (off) hand slot has a temporary enchant, ''false'' otherwise
:;offHandExpiration:{{apitype|number}} - time remaining for the off hand enchant, as thousandths of seconds
:;offHandCharges:{{apitype|number}} - the number of charges remaining on the off hand enchant
:;offHandEnchantID:{{apitype|number}} - ID of the off hand enchant (new in 6.0)
:;hasRangedEnchant:{{apitype|boolean}} - ''true'' if the weapon in the ranged hand slot has a temporary enchant, ''false'' otherwise (only on cataclysm/4.x)
:;rangedExpiration:{{apitype|number}} - time remaining for the ranged enchant, as thousandths of seconds (only on cataclysm/4.x)
:;rangedCharges:{{apitype|number}} - the number of charges remaining on the ranged enchant (only on cataclysm/4.x)
:;rangedEnchantID:{{apitype|number}} - ID of the ranged enchant (only on cataclysm/4.x)

==Related Events==
* {{api|t=e|UNIT_INVENTORY_CHANGED}} fires when (among other things) the player's temporary enchants, and thus the return values from this function, change.
```