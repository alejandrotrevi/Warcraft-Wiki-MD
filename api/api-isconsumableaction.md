# API IsConsumableAction

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if an action is a consumable, i.e. it has a count.
 isConsumable = IsConsumableAction(slotID)

==Arguments==
:;slotID:{{apitype|number}} - [[ActionSlot]]

==Returns==
:;isConsumable:{{apitype|boolean}}
::* True if the action in the specified slot is linked to a consumable, e.g. a potion action.
::* False if the action is not consumable or if the action is empty.

==Details==
* Most consumable actions have a small number displayed in the bottom right corner of their action icon.
* However, in Classic, spells requiring a reagent may return true to '''IsConsumableAction()''' but false to both {{api|IsItemAction}} and {{api|IsStackableAction}}; such spells ''do not'' display a number.<ref>[https://us.forums.blizzard.com/en/wow/t/getactioncount-changed-in-1-13-3/388433], Blizzard forum discussion on [[API_GetActionCount|GetActionCount()]] removal from Classic</ref>
* ''[This statement may be out of date]'' Currently thrown weapons show up with a count of 1. In WoW 2.0 throwing weapons have durability and can be repaired, so this is likely a bug.

==References==
```