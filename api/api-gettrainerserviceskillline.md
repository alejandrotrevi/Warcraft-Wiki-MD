# API GetTrainerServiceSkillLine

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Gets the name of the skill at the specified line from the current trainer.
 skillLine = GetTrainerServiceSkillLine(index)

==Arguments==
:;index:{{apitype|number}} - Index of the trainer service to get the name of. Note that indices are affected by the trainer filter. (See [[API_GetTrainerServiceTypeFilter|GetTrainerServiceTypeFilter]] and [[API_SetTrainerServiceTypeFilter|SetTrainerServiceTypeFilter]].)

==Returns==
:;skillLine:{{apitype|string}} - The name of the skill on the specified line.
```