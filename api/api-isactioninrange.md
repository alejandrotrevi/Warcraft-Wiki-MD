# API IsActionInRange

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the specified action is in range.
 inRange = IsActionInRange(actionSlot [, unit])

==Arguments==
:;actionSlot:{{apitype|number}} - The [[actionSlot|action slot]] to test.
:;unit:{{apitype|string?}} : [[UnitId]]

==Returns==
:;inRange:{{apitype|boolean}} - nil if the slot has no action, or if the action cannot be used on the current target, or if range does not apply; false if the action is out of range, and true otherwise.

==Patch changes==
* {{Patch 6.0.2|note=Return values are now true/false instead of 1/0}}


==See also==
* {{api|IsSpellInRange}}
* {{api|IsItemInRange}}
* {{api|CheckInteractDistance}}
* {{api|ActionHasRange}}
```