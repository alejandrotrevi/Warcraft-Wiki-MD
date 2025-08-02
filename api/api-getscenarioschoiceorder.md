# API GetScenariosChoiceOrder

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns an ordered list of all available scenario IDs.
 allScenarios = GetScenariosChoiceOrder([allScenarios])

==Arguments==
:;allScenarios:{{apitype|table?}} - If provided, this table will be wiped and populated with return values; otherwise, a new table will be created for the return value.

==Returns==
:;allScenarios:{{apitype|table}} - An array containing LFG dungeon IDs of specific scenarios. Not all of these may be level-appropriate.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|GetLFGDungeonInfo}}
* {{api|GetRandomScenarioInfo}}
```