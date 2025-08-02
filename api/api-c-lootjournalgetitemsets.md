# API C LootJournal.GetItemSets

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_LootJournal|system=LootJournal}}
Needs summary.
 itemSets = C_LootJournal.GetItemSets([classID, specID])

==Arguments==
:;classID:{{apitype|number?}}
:;specID:{{apitype|number?}}

==Returns==
:;itemSets:{{apitype|LootJournalItemSetInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| setID || {{apitype|number}} || 
|-
| itemLevel || {{apitype|number}} || 
|-
| name || {{apitype|string}} || 
|}

==Patch changes==
* {{Patch 9.2.0|note=Added.}}
```