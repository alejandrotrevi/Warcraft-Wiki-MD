# API C EncounterJournal.GetEncounterJournalLink

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_EncounterJournal|system=EncounterJournal}}
Needs summary.
 link = C_EncounterJournal.GetEncounterJournalLink(linkType, ID, displayText, difficultyID)

==Arguments==
:;linkType:{{apitype|Enum.JournalLinkTypes}}
{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! Value !! Field !! Description
|-
| 0 || Instance || 
|-
| 1 || Encounter || 
|-
| 2 || Section || 
|-
| 3 || Tier || 
|}
:;ID:{{apitype|number}}
:;displayText:{{apitype|string}}
:;difficultyID:{{apitype|number}}

==Returns==
:;link:{{apitype|string}}
```