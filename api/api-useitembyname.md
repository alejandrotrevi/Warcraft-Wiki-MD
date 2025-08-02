# API UseItemByName

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.6|tentative=1}}
Uses the specified item.
 UseItemByName(name[, target])

==Arguments==
:;name:{{apitype|string}} - name of the item to use.
:;target:{{apitype|string?}} : [[UnitId]] - The unit to use the item on, defaults to "target" for items that can be used on others.

==Patch changes==
* {{Patch 2.0.1|note=Protected.}}

==See also==
* {{api|UseContainerItem}}
* {{api|UseInventoryItem}}
```