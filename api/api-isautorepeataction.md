# API IsAutoRepeatAction

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if an action is currently auto-repeating (e.g. Shoot for wand and Auto Shot for Hunters).
 isRepeating = IsAutoRepeatAction(actionSlot)

==Arguments==
:;actionSlot:{{apitype|number}} - The [[action slot]] to query.

==Returns==
:;isRepeating:{{apitype|boolean}} - true if the action in the slot is currently auto-repeating, false if it is not auto-repeating or the slot is empty.

==See also==
* {{api|IsAutoRepeatSpell}}
```