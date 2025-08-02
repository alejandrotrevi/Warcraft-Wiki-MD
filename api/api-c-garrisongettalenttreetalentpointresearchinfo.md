# API C Garrison.GetTalentTreeTalentPointResearchInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Garrison|system=GarrisonInfo}}
Needs summary.
 goldCost, currencyCosts, durationSecs = C_Garrison.GetTalentTreeTalentPointResearchInfo(garrTalentID, researchRank, garrTalentTreeID, talentPointIndex, isRespec)

==Arguments==
:;garrTalentID:{{apitype|number}}
:;researchRank:{{apitype|number}}
:;garrTalentTreeID:{{apitype|number}}
:;talentPointIndex:{{apitype|number}}
:;isRespec:{{apitype|boolean}}

==Returns==
:;goldCost:{{apitype|number}}
:;currencyCosts:{{apitype|GarrisonTalentCurrencyCostInfo[]}}
{{:Struct GarrisonTalentCurrencyCostInfo|nocaption=1}}
:;durationSecs:{{apitype|number}}

==Patch changes==
* {{Patch 9.2.0|note=Added <code>garrTalentID, researchRank</code> arguments.}}
* {{Patch 9.0.1|note=Added <code>currencyCosts</code> return.}}
* {{Patch 8.3.0|note=Added.}}
```