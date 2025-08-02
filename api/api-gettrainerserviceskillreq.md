# API GetTrainerServiceSkillReq

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the name of the required skill and the amount needed in that skill.
 skillName, skillLevel, hasReq = GetTrainerServiceSkillReq(index)

==Arguments==
:;index:{{apitype|number}} - the number of the [[API GetTrainerSelectionIndex|selection]] in the trainer window

==Returns==
:;skillName:{{apitype|string?}} - The name of the skill.
:;skillLevel:{{apitype|number}} - The required level needed for the skill.
:;hasReq:{{apitype|boolean}} - Seems to be true for skills that you cannot learn, nil for skills you have learned already.

==Example==
  local selection = [[API GetTrainerSelectionIndex|GetTrainerSelectionIndex()]]
  local skillName, skillAmt = [[API GetTrainerServiceSkillReq|GetTrainerServiceSkillReq(selection)]]
  DEFAULT_CHAT_FRAME:AddMessage('Skill Name: ' .. skillName)
  DEFAULT_CHAT_FRAME:AddMessage('Skill Amount Required: ' .. skillLevel)

If you had an engineering trainer open, with a skill you knew already the output would be:

  Skill Name: Engineering
  Skill Amount Required: 375
```