# API C Scenario.GetBonusStepInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the information about the current scenario bonus objective.
 name, description, numCriteria, failed = C_Scenario.GetBonusStepInfo()

==Returns==
:;name:{{apitype|string}} - name of the bonus step, e.g. "Bonus: Go for the Gold!", or nil if there is no active bonus objective.
:;description:{{apitype|string}} - objective description, e.g. "Get a score of at least 30,000", or nil if there is no active bonus objective
:;numCriteria:{{apitype|number}} - number of criteria this bonus objective has.
:;failed:{{apitype|boolean}} - true if this bonus objective has been failed, false otherwise.

==Patch changes==
* {{Patch 5.3.0|note=Added.}}

==See also==
* {{api|C_Scenario.GetBonusCriteriaInfo}}
```