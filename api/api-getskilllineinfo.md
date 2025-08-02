# API GetSkillLineInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information on a skill line/header.
 skillName, header, isExpanded, skillRank, numTempPoints, skillModifier,
   skillMaxRank, isAbandonable, stepCost, rankCost, minLevel, skillCostType,
   skillDescription = GetSkillLineInfo(index)

==Arguments==
:;index:{{apitype|number}} - The index of a line in the skills window, can be a header or skill line. Indices can change depending on collapsed/expanded headers.

==Returns==
:;1. skillName:{{apitype|string}} - Name of the skill line.
:;2. header:{{apitype|number}} - Returns 1 if the line is a header, nil otherwise.
:;3. isExpanded:{{apitype|number}} - Returns 1 if the line is a header and expanded, nil otherwise.
:;4. skillRank:{{apitype|number}} - The current rank for the skill, 0 if not applicable.
:;5. numTempPoints:{{apitype|number}} - Temporary points for the current skill.
:;6. skillModifier:{{apitype|number}} - Skill modifier value for the current skill.
:;7. skillMaxRank:{{apitype|number}} - The maximum rank for the current skill. If this is 1 the skill is a proficiency.
:;8. isAbandonable:{{apitype|number}} - Returns 1 if this skill can be unlearned, nil otherwise.
:;9. stepCost:{{apitype|number}} - Returns 1 if skill can be learned, nil otherwise.
:;10. rankCost:{{apitype|number}} - Returns 1 if skill can be trained, nil otherwise.
:;11. minLevel:{{apitype|number}} - Minimum level required to learn this skill.
:;12. skillCostType:{{apitype|number}}
:;13. skillDescription:{{apitype|string}} - Localized skill description text

==Example==
Prints the player's skill lines.
 /run for i = 1, GetNumSkillLines() do print(i, GetSkillLineInfo(i)) end

==Patch changes==
* {{Patch 4.0.1|note=Removed.}}
```