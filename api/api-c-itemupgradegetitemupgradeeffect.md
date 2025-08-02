# API C ItemUpgrade.GetItemUpgradeEffect

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ItemUpgrade|system=ItemUpgrade}}
Returns the effect of upgrading an item on one of its effects.
 outBaseEffect, outUpgradedEffect = C_ItemUpgrade.GetItemUpgradeEffect(effectIndex [, numUpgradeLevels])

==Arguments==
:;effectIndex:{{apitype|number}} - Index of the effect to query, ascending from 1 to {{api|C_ItemUpgrade.GetNumItemUpgradeEffects}}()
:;numUpgradeLevels:{{apitype|number?}}

==Returns==
:;outBaseEffect:{{apitype|string}} - effect text before the item upgrade (e.g. "When your attacks hit you have a chance to gain 3,386 critical strike for 30 sec.")
:;outUpgradedEffect:{{apitype|string}} - effect text after the item upgrade (e.g. "When your attacks hit you have a chance to gain 3,649 critical strike for 30 sec.")

==Details==
* The function returns information about the item currently being considered for an upgrade (e.g. using {{api|SetItemUpgradeFromCursorItem}}).
* Item effects are non-stat bonuses on the item, like custom Equip: bonuses (procs) and Use: abilities.
* The strings returned by this function are plain text; FrameXML attempts to highlight the differences in numbers using string operations (see ItemUpgradeFrame_GetUpgradedEffectString)

==Patch changes==
* {{Patch 9.1.0|note=Added.}}

==See also==
* {{api|GetItemUpgradeStats}}
```