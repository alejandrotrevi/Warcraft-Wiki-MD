# API IsCurrentAction

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the specified action is currently being used.
 isCurrent = IsCurrentAction(actionSlot)

==Arguments==
:;actionSlot:{{apitype|number}} - [[action slot]] ID to query.

==Returns==
:;isCurrent:{{apitype|boolean}} - 1 if the action in the slot is currently executing, nil otherwise.
```