# API C ItemUpgrade.GetItemLevelIncrement

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ItemUpgrade|system=ItemUpgrade}}
Returns the proposed item level increment for the item being considered for upgrading.
 itemLevelIncrement = C_ItemUpgrade.GetItemLevelIncrement([numUpgradeLevels])

==Arguments==
:;numUpgradeLevels:{{apitype|number?|default=1}}

==Returns==
:;itemLevelIncrement:{{apitype|number}} - the number of item levels by which upgrading the current item will increase its item level, 0 if the item cannot be upgraded further or if there is no item being considered for upgrade.

==Patch changes==
* {{Patch 9.1.0|note=Added.}}

==See also==
* {{api|GetItemUpdateLevel}}()
```