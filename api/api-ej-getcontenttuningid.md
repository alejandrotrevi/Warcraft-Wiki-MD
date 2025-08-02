# API EJ GetContentTuningID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the currently selected content tuning ID for BFA instances per {{api|EJ_SelectInstance}}.
 tuningID = EJ_GetContentTuningID()

==Returns==
:;tuningID:{{apitype|number}} : {{dbc|contenttuning|ContentTuning.ID}}

==Details==
* Used in the FrameXML for {{api|GameTooltip_SetHyperlink|GameTooltip:SetHyperlink}} when hovering over inline spell hyperlinks in the overview tab. [https://www.townlong-yak.com/framexml/8.1.5/Blizzard_EncounterJournal/Blizzard_EncounterJournal.lua#1001]

==Values==
{| class="sortable darktable zebra"
|-
! ID !! [[DifficultyID|Difficulty]] !! Type
|-
| 500 || 1 || Dungeon - Normal
|-
| 501 || 2 || Dungeon - Heroic
|-
| 502 || 23 || Dungeon - Mythic
|-
! colspan="3" | Uldir
|-
| 503 || 14 || Raid - Normal
|-
| 504 || 15 || Raid - Heroic
|-
| 505 || 16 || Raid - Mythic
|-
| 506 || 17 || Raid - Raid Finder
|-
! colspan="3" | Battle of Dazar'alor
|-
| 686 || 14 || Raid - Normal
|-
| 687 || 15 || Raid - Heroic
|-
| 688 || 16 || Raid - Mythic
|-
| 689 || 17 || Raid - Raid Finder
|-
! colspan="3" | Crucible of Storms
|-
| 698 || 14 || Raid - Normal
|-
| 697 || 15 || Raid - Heroic
|-
| 696 || 16 || Raid - Mythic
|-
| 695 || 17 ||  Raid - Raid Finder
|}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}

==See also==
* {{api|EJ_GetDifficulty}}
```