# API EJ GetSectionPath

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} 
Returns the parent Section ID if available.
 sectionID, parentSectionID, grandParentSectionID = EJ_GetSectionPath(sectionID)

==Arguments==
:;sectionID:{{apitype|number}}

==Returns==
:;sectionID:{{apitype|number}} : {{dbc|journalencountersection|JournalEncounterSection.ID}}
:;parentSectionID:{{apitype|number?}}
:;grandParentSectionID:{{apitype|number?}}

==Patch changes==
* {{Patch 4.2.0|note=Added.}}
```