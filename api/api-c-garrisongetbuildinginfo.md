# API C Garrison.GetBuildingInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns garrison building info.
 id, name, textureKit, icon, description, rank, currencyID, currencyQty, goldQty, buildTime, needsPlan, isPrebuilt, possSpecs, upgrades, canUpgrade, isMaxLevel, hasFollowerSlot = C_Garrison.GetBuildingInfo(buildingID)

==Arguments==
:;buildingID:{{apitype|number}} : {{dbc|GarrBuilding}}

==Returns==
:;1. id:{{apitype|number}}
:;2. name:{{apitype|string}}
:;3. textureKit:{{apitype|string}}
:;4. icon:{{apitype|fileID}}
:;5. description:{{apitype|string}}
:;6. rank:{{apitype|number}}
:;7. currencyID:{{apitype|number}}
:;8. currencyQty:{{apitype|number}}
:;9. goldQty:{{apitype|number}}
:;10. buildTime:{{apitype|string}}
:;11. needsPlan:{{apitype|boolean}}
:;12. isPrebuilt:{{apitype|boolean}}
:;13. possSpecs:{{apitype|table}}
:;14. upgrades:{{apitype|number[]}}
:;15. canUpgrade:{{apitype|boolean}}
:;16. isMaxLevel:{{apitype|boolean}}
:;17. hasFollowerSlot:{{apitype|boolean}}

==Example==
 /dump C_Garrison.GetBuildingInfo(145)
<syntaxhighlight lang="lua">
[1] = 145,
[2] = "Trading Post",
[3] = "GarrBuilding_TradingPost_3_A",
[4] = 975746,
[5] = "The Trading Post is the garrison's center of commerce with the natives of Draenor.",
[6] = 3,
[7] = 0,
[8] = 0,
[9] = 1000,
[10] = "1 hr",
[11] = true,
[12] = false,
[13] = {
},
[14] = {
  [1] = 111,
  [2] = 144,
  [3] = 145
},
[15] = true,
[16] = true,
[17] = false
</syntaxhighlight>

==Patch changes==
* {{Patch 6.0.2|note=Added.}}

==See also==
* {{api|C_Garrison.GetBuildings}}
```