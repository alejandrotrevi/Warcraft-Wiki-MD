# API IsItemInRange

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.6|tentative=1}}
Returns whether the item is in usable range of the unit.
 inRange = IsItemInRange(item [, unit])

==Arguments==
:;item:{{apitype|number,string}} : {{:ItemInfo}} - If using an item name, requires the item to be in your inventory. Item IDs and links don't have this requirement.
:;unit:{{apitype|string?}} : [[UnitId]] - Defaults to "target"

==Returns==
:;inRange:{{apitype|boolean}} - Whether the item is in range; Returns <code>nil</code> if there is no unit targeted or the item ID is invalid.

==Example==
Prints if you are within 4 yards range of the target by checking the [[Gin-Ji Knife Set]] item range.<ref>https://github.com/DeadlyBossMods/DeadlyBossMods/blob/9.0.21/DBM-Core/DBM-RangeCheck.lua#L57</ref>
 /dump IsItemInRange(90175)

==Patch changes==
* {{Hotfix|date=2023-12-11|doc=|version=10.2.0.52485|note=Partially unrestricted. Querying enemy units while in combat is once again permitted.}}
* {{Hotfix|date=2023-11-16|version=10.2.0.52188|note=Protected. May no longer be called in combat by insecure code.}}
* {{Patch 2.0.1|note=Added.}}

==References==
```