# API C TransmogCollection.GetAppearanceSourceDrops

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_TransmogCollection|system=TransmogrifyCollection}}
Needs summary.
 encounterInfo = C_TransmogCollection.GetAppearanceSourceDrops(itemModifiedAppearanceID)

==Arguments==
:;itemModifiedAppearanceID:{{apitype|number}}

==Returns==
:;encounterInfo:{{apitype|TransmogAppearanceJournalEncounterInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| instance || {{apitype|string}} || 
|-
| instanceType || {{apitype|number}} || 
|-
| tiers || {{apitype|string[]}} || 
|-
| encounter || {{apitype|string}} || 
|-
| difficulties || {{apitype|string[]}} || 
|}

==Patch changes==
* {{Patch 7.0.3|note=Added.}}
```