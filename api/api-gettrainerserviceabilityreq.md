# API GetTrainerServiceAbilityReq

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the name of a requirement for training a skill and if the player meets the requirement.
 ability, hasReq = GetTrainerServiceAbilityReq(trainerIndex, reqIndex)

==Arguments==
:;trainerIndex:{{apitype|number}} - Index of the trainer service to retrieve information about. Note that indices are affected by the trainer filter. (See {{api|GetTrainerServiceTypeFilter}} and {{api|SetTrainerServiceTypeFilter}}.)
:;reqIndex:{{apitype|number}} - Index of the requirement to retrieve information about.

==Returns==
:;ability:{{apitype|string}} - The name of the required ability. Not readily available on function call, see [[SpellMixin#ContinueOnSpellLoad|SpellMixin:ContinueOnSpellLoad]].
:;hasReq:{{apitype|boolean}} - Flag for if the player meets the requirement.
```