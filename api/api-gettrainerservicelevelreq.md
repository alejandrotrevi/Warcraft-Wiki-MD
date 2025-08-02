# API GetTrainerServiceLevelReq

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the required level to learn a skill from the trainer.
 reqLevel = GetTrainerServiceLevelReq(id)

==Arguments==
:;id:{{apitype|number}} - Index of the trainer service to retrieve information about. Note that indices are affected by the trainer filter. (See [[API_GetTrainerServiceTypeFilter|GetTrainerServiceTypeFilter]] and [[API_SetTrainerServiceTypeFilter|SetTrainerServiceTypeFilter]].)

==Returns==
:;reqLevel:{{apitype|number}} - The required level (for pet or player) to learn the skill.
```