# API GetPetExperience

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the pet's current and total XP required for the next level.
 currXP, nextXP = GetPetExperience()

==Returns==
:;currXP:{{apitype|number}} - The current XP total
:;nextXP:{{apitype|number}} - The XP total required for the next level

==Example==
Pet experience is displayed in the default chat frame.
<syntaxhighlight lang="lua">
local currXP, nextXP = GetPetExperience()
print("Pet experience: " .. currXP .. " / " .. nextXP)
</syntaxhighlight>
```