# API C Covenants.GetCovenantData

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Covenants|system=Covenant}}
Needs summary.
 data = C_Covenants.GetCovenantData(covenantID)

==Arguments==
:;covenantID:{{apitype|Enum.CovenantType}}
{{:Enum.CovenantType|nocaption=1}}

==Returns==
:;data:{{apitype|CovenantData?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|ID}} || {{apitype|number}} || 
|-
| {{apiname|textureKit}} || {{apitype|textureKit}} || 
|-
| {{apiname|celebrationSoundKit}} || {{apitype|number}} || 
|-
| {{apiname|animaChannelSelectSoundKit}} || {{apitype|number}} || 
|-
| {{apiname|animaChannelActiveSoundKit}} || {{apitype|number}} || 
|-
| {{apiname|animaGemsFullSoundKit}} || {{apitype|number}} || 
|-
| {{apiname|animaNewGemSoundKit}} || {{apitype|number}} || 
|-
| {{apiname|animaReinforceSelectSoundKit}} || {{apitype|number}} || 
|-
| {{apiname|upgradeTabSelectSoundKitID}} || {{apitype|number}} || 
|-
| {{apiname|reservoirFullSoundKitID}} || {{apitype|number}} || 
|-
| {{apiname|beginResearchSoundKitID}} || {{apitype|number}} || 
|-
| {{apiname|renownFanfareSoundKitID}} || {{apitype|number}} || 
|-
| {{apiname|factionID}} || {{apitype|number}} || 
|-
| {{apiname|name}} || {{apitype|string}} || 
|-
| {{apiname|soulbindIDs}} || {{apitype|number[]}} || 
|}

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```