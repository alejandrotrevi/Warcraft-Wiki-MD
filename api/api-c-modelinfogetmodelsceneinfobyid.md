# API C ModelInfo.GetModelSceneInfoByID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ModelInfo|system=ModelInfo}}
Needs summary.
 modelSceneType, modelCameraIDs, modelActorsIDs, flags = C_ModelInfo.GetModelSceneInfoByID(modelSceneID)

==Arguments==
:;modelSceneID:{{apitype|number}}

==Returns==
:;modelSceneType:{{apitype|Enum.ModelSceneType}}
{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! Value !! Field !! Description
|-
| 0 || MountJournal || 
|-
| 1 || PetJournalCard || 
|-
| 2 || ShopCard || 
|-
| 3 || EncounterJournal || 
|-
| 4 || PetJournalLoadout || 
|-
| 5 || ArtifactTier2 || 
|-
| 6 || ArtifactTier2ForgingScene || 
|-
| 7 || ArtifactTier2SlamEffect || 
|-
| 8 || CommentatorVictoryFanfare || 
|-
| 9 || ArtifactRelicTalentEffect || 
|-
| 10 || PvPWarModeOrb || 
|-
| 11 || PvPWarModeFire || 
|-
| 12 || PartyPose || 
|-
| 13 || AzeriteItemLevelUpToast || 
|-
| 14 || AzeritePowers || 
|-
| 15 || AzeriteRewardGlow || 
|-
| 16 || HeartOfAzeroth || 
|-
| 17 || WorldMapThreat || 
|-
| 18 || Soulbinds || 
|-
| 19 || JailersTowerAnimaGlow || 
|}
:;modelCameraIDs:{{apitype|number[]}}
:;modelActorsIDs:{{apitype|number[]}}
:;flags:{{apitype|number}}

==Patch changes==
* {{Patch 10.0.5|note=Added <code>flags</code> return.}}
* {{Patch 9.0.1|note=Added <code>PvPWarModeOrb, PvPWarModeFire, Soulbinds, JailersTowerAnimaGlow</code> fields.}}
* {{Patch 8.3.0|note=Added <code>WorldMapThreat</code> field.}}
* {{Patch 8.2.0|note=Added <code>HeartOfAzeroth</code> field.}}
* {{Patch 8.0.1|note=Added <code>PvpWarModeOrb, PvpWarModeFire, PartyPose, AzeriteItemLevelUpToast, AzeritePowers, AzeriteRewardGlow</code> fields.}}
* {{Patch 7.3.0|note=Added <code>ArtifactRelicTalentEffect</code> field.}}
* {{Patch 7.2.5|note=Added <code>CommentatorVictoryFanfare</code> field.}}
* {{Patch 7.2.0|note=Added.}}
```