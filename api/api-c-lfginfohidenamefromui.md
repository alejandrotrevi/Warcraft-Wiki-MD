# API C LFGInfo.HideNameFromUI

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if a dungeon name has to be hidden in the UI.
 shouldHide = C_LFGInfo.HideNameFromUI(dungeonID)

==Arguments==
:;[[LfgDungeonID|dungeonID]]:{{apitype|number}}

==Returns==
:;shouldHide:{{apitype|boolean}}

==Details==
* List of IDs where shouldHide is true.
{| class="sortable darktable zebra"
|-
! ID !! Name !! [[DifficultyID]]
|-
| 1030 || 7.0 Artifacts - Sub Rog - Acquisition - Demonic Portal World || 12: Normal Scenario
|-
| 1090 || Boost 2.0 R&D || 12: Normal Scenario
|-
| 1307 || Tideskorn Harbor Acquisition Scenarios - JMC || 12: Normal Scenario
|-
| 1309 || Shield's Rest Acquisition Scenarios - JMC || 12: Normal Scenario
|-
| 1371 || Priest Order Formation - JMC || 12: Normal Scenario
|-
| 1381 || [DNT] Blade in Twilight || 12: Normal Scenario
|-
| 1382 || [DNT] Sword of Kings || 12: Normal Scenario
|-
| 1436 || 7.2 Broken Shore Intro - Legion Command Ship (KMS) || 12: Normal Scenario
|}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```