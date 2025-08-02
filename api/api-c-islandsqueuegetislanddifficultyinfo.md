# API C IslandsQueue.GetIslandDifficultyInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the island expedition modes.
 islandDifficultyInfo = C_IslandsQueue.GetIslandDifficultyInfo()

==Returns==
:;islandDifficultyInfo:structure - IslandsQueueDifficultyInfo[]

{| class="sortable darktable zebra"
! Field !! Type !! Description
|-
| difficultyId || {{apitype|number}} || ID specific to islands
|-
| previewRewardQuestId || {{apitype|number}} || 
|}

==Details==
{| class="sortable darktable zebra"
|-
! Index !! difficultyId !! previewRewardQuestId 
|-
| 1 (Normal) || 1726 || 51838
|-
| 2 (Heroic) || 1736 || 53339
|-
| 3 (Mythic) || 1737 || 53340
|-
| 4 (PvP) || 1762 || 53341
|}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```