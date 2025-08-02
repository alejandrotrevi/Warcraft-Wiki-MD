# API ArchaeologyMapUpdateAll

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Updates and returns the amount of [[digsite]]s in a zone.
 numSites = ArchaeologyMapUpdateAll(uiMapID)

==Arguments==
:;uiMapID:{{apitype|number}} : [[UiMapID]]

==Returns==
:;numSites:{{apitype|number}} - How many [[digsite]]s the player can [[survey]] in a zone. The player must actually be in a zone that can be surveyed.

==Patch changes==
* {{Patch 5.4.0|note=Added.}}
```