# API GetActionText

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the label text for an action.
 text = GetActionText(actionSlot)

==Arguments==
:;actionSlot:{{apitype|number}} - The queried [[ActionSlot]].

==Returns==
:;text:{{apitype|string}}
::* The action's text, if present.  Macro actions use their names for their action text.
::* nil, if the slot has no action text, or is empty.  Most standard WoW action icons don't have action text.
```