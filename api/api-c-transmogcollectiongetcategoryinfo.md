# API C TransmogCollection.GetCategoryInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns wardrobe category info.
 name, isWeapon, canHaveIllusions, canMainHand, canOffHand, canRanged = C_TransmogCollection.GetCategoryInfo(category)

==Arguments==
:;category:{{apitype|Enum.TransmogCollectionType}}
{{:Enum.TransmogCollectionType|nocaption=1}}

==Returns==
:;name:{{apitype|string}}
:;isWeapon:{{apitype|boolean?|default=false}}
:;canHaveIllusions:{{apitype|boolean?|default=false}}
:;canMainHand:{{apitype|boolean?|default=false}}
:;canOffHand:{{apitype|boolean?|default=false}}
:;canRanged:{{apitype|boolean?|default=false}}

==Details==
* Only returns valid data for the current [[class proficiencies]]. The <code>canEnchant</code>, <code>canMainHand</code> and <code>canOffHand</code> return values differ depending on the class and spec.

==Patch changes==
* {{Patch 11.0.5|note=Added <code>canRanged</code> return value.}}
* {{Patch 7.0.3|note=Added.}}
```