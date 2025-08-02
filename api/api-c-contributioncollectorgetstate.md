# API C ContributionCollector.GetState

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ContributionCollector|system=ContributionCollector}}
Returns the current state of a building, its completion percentage, and time until next state change.
 contributionState, contributionPercentageComplete, timeOfNextStateChange, startTime = C_ContributionCollector.GetState(contributionID)

==Arguments==
:;contributionID:{{apitype|number}} : [[ContributionID]]

==Returns==
:;contributionState:{{apitype|Enum.ContributionState?|default=None}}
{{:Enum.ContributionState|nocaption=1}}
:;contributionPercentageComplete:{{apitype|number}}
:;timeOfNextStateChange:{{apitype|number?}}
:;startTime:{{apitype|number}}

==Patch changes==
* {{Patch 8.0.1|note=Added <code>startTime</code> return.}}
* {{Patch 7.2.0|note=Added.}}
```