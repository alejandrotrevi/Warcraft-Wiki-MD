# API C Scenario.GetCriteriaInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 criteriaString, criteriaType, completed, quantity, totalQuantity, flags, assetID, quantityString, criteriaID, duration, elapsed, criteriaFailed, isWeightedProgress
    = C_Scenario.GetCriteriaInfo(criteriaIndex)
    = C_Scenario.GetCriteriaInfoByStep(stepID, criteriaIndex)

==Arguments==
===<font color="#4ec9b0">GetCriteriaInfo</font>===
:;criteriaIndex:{{apitype|number}} - up to <code>numCriteria</code>, the 3rd return value of {{api|C_Scenario.GetStepInfo}}()

===<font color="#4ec9b0">GetCriteriaInfoByStep</font>===
:;stepID:{{apitype|number}}
:;criteriaIndex:{{apitype|number}}

==Returns==
:;1. criteriaString:{{apitype|string}}
:;2. criteriaType:{{apitype|number}}
:;3. completed:{{apitype|boolean}}
:;4. quantity:{{apitype|number}}
:;5. totalQuantity:{{apitype|number}}
:;6. flags:{{apitype|number}}
:;7. assetID:{{apitype|number}}
:;8. quantityString:{{apitype|string}}
:;9. criteriaID:{{apitype|number}} - see {{dbc|criteria|Criteria.db2}} / {{dbc|criteriatree|CriteriaTree.db2}}
:;10. duration:{{apitype|number}}
:;11. elapsed:{{apitype|number}}
:;12. criteriaFailed:{{apitype|boolean}}
:;13. isWeightedProgress:{{apitype|boolean}}

==Patch changes==
* {{Patch 6.0.2|note=Added '''C_Scenario.GetCriteriaInfoByStep()'''}}
* {{Patch 5.0.4|note=Added '''C_Scenario.GetCriteriaInfo()'''}}
```