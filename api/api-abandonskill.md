# API AbandonSkill

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
The player abandons a skill.
 AbandonSkill(skillLineID)

==Arguments==
:;skillLineID:{{apitype|number}} - The Skill Line ID (can be found with [[API GetProfessionInfo]]())

==Example==
<syntaxhighlight lang="lua">
local prof1, prof2, archaeology, fishing, cooking, firstAid = GetProfessions();
local skillLineID = select(7, GetProfessionInfo(prof1));
AbandonSkill(skillLineID);
</syntaxhighlight>

==Result==
The player abandons a skill.

'''CAUTION''': There is no confirmation dialog for this action.  Use with care.
```