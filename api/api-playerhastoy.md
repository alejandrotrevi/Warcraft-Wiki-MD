# API PlayerHasToy

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Determines if player has a specific toy in their toybox
 hasToy = PlayerHasToy(itemId)

==Arguments==
:;itemId:{{apitype|number}} - itemId of a toy.

==Returns==
:;hasToy:{{apitype|boolean}} - True if player has itemId in their toybox, false if not.

==Example==
 if PlayerHasToy(92738) then print('Remember to wear your Safari Hat!'); end
```