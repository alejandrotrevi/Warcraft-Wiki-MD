# API C ItemUpgrade.GetNumItemUpgradeEffects

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ItemUpgrade|system=ItemUpgrade}}
Returns the number of item effects affected by upgrading the current item.
 numItemUpgradeEffects = C_ItemUpgrade.GetNumItemUpgradeEffects()

==Returns==
:;numItemUpgradeEffects:{{apitype|number}} - number of item effects that will be altere by upgrading the item.

==Details==
* The function returns information about the item currently being considered for an upgrade (e.g. using {{api|SetItemUpgradeFromCursorItem}}).
* Item effects are non-stat bonuses on the item, like custom Equip: bonuses (procs) and Use: abilities.

==Patch changes==
* {{Patch 9.1.0|note=Added.}}
```