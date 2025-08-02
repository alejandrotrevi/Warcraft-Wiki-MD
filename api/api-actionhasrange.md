# API ActionHasRange

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the action has has a range requirement.
 hasRange = ActionHasRange(slotID)

==Arguments==
:;slotID:{{apitype|number}} - The [[actionSlot|slot ID]] to test.

==Returns==
:;hasRange:{{apitype|boolean}} - True if the specified slot contains an action which has a numeric range requirement.

==Details==
This function returns true if the action in the specified slot ID has a numeric range requirement as shown in the action's tooltip, e.g. [[Fire Blast]] has a numeric range of 20 yards.  For actions like [[Attack]] which have no numeric range requirement in their tooltip (even though they only work within a certain range), this function will return false.
```