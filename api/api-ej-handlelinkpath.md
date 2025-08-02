# API EJ HandleLinkPath

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the supplementary instance and encounter ID for an encounter or section ID.
 instanceID, encounterID, sectionID, tierIndex = EJ_HandleLinkPath(journalType, id)

==Arguments==
:;journalType:{{apitype|number}}
:;id:{{apitype|number}} - depending on journal type; 0=instanceID, 1=encounterID, 2=sectionID

==Returns==
:;instanceID:{{apitype|number}} : {{dbc|journalinstance|JournalInstance.ID}}
:;encounterID:{{apitype|number?}} : [[JournalEncounterID]]
:;sectionID:{{apitype|number?}} : {{dbc|journalencountersection|JournalEncounterSection.ID}}
:;tierIndex:{{apitype|number?}}

==Example==
Section "Bwonsamdi's Boon" (19444) is from the "King Rastakhan" (2335) encounter in the "Battle of Dazar'alor" (1176) instance
 /dump EJ_HandleLinkPath(2, 19444)

 > 1176, 2335, 19444

==Details==
* Used in the FrameXML to open a [[Hyperlinks#journal|journalLink]] to the Encounter Journal.<sup>[https://www.townlong-yak.com/framexml/go/EncounterJournal_OpenJournalLink]</sup>

==Patch changes==
* {{Patch 4.2.0|note=Added.}}
```