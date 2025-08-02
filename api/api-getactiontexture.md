# API GetActionTexture

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the icon texture for an action.
 texture = GetActionTexture(actionSlot)

==Arguments==
:;actionSlot:{{apitype|number}} - The queried [[ActionSlot]].

==Returns==
:;texture:{{apitype|fileID?}} - Returns nil if the slot is empty.
```