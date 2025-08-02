# API C ContributionCollector.GetBuffs

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the buffs provided by a building (e.g. in a [[Warfront]]).
 spellID, ... = C_ContributionCollector.GetBuffs(contributionID)

==Arguments==
:;[[ContributionID|contributionID]]:{{apitype|number}}

==Returns==
(variable returns: spellID1, spellID2, ...)
:;spellID:{{apitype|number}} - the spellID of the first buff provided. This buff is always provided when the building is active.

==Patch changes==
* {{Patch 7.2.0|note=Added.}}
```