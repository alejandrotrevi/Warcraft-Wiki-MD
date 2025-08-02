# API C LootJournal.GetItemSetItems

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_LootJournal|system=LootJournal}}
Needs summary.
 items = C_LootJournal.GetItemSetItems(setID)

==Arguments==
:;setID:{{apitype|number}}

==Returns==
:;items:{{apitype|LootJournalItemInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| itemID || {{apitype|number}} || 
|-
| icon || {{apitype|number}} || 
|-
| invType || {{apitype|number}} || 
|}

==Patch changes==
* {{Patch 9.2.0|note=Readded.}}
* {{Patch 9.0.1|note=Removed.}}
* {{Patch 7.0.3|note=Added.}}
```