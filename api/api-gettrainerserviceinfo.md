# API GetTrainerServiceInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about a trainer service.
 name, rank, category, expanded = GetTrainerServiceInfo(index)

==Arguments==
:;index:{{apitype|number}} - Index of the trainer service to retrieve information about. Note that indices are affected by the trainer filter. (See [[API_GetTrainerServiceTypeFilter|GetTrainerServiceTypeFilter]] and [[API_SetTrainerServiceTypeFilter|SetTrainerServiceTypeFilter]].)

==Returns==
:;name:{{apitype|string}} - Name of the spell or the header (i.e. "Arcane Explosion" or "Fire").
:;rank:{{apitype|string}} - Rank of the spell, if applicable. Headers return empty strings.
:;category:{{apitype|string}} - "used" (already have the spell), "unavailable" (can not train this skill), "available" (can train this skill) and "header".
:;expanded:{{apitype|number}} - nil if this is a collapsed header (category == "header"), 1 otherwise. (See [[API_CollapseTrainerSkillLine|CollapseTrainerSkillLine]] and [[API_ExpandTrainerSkillLine|ExpandTrainerSkillLine]].)

==Example==
Prints the list of trainable spells when interacting with a trainer.
 local i, name, rank, category;
 for i=1,GetNumTrainerServices() do
  name, rank, category = GetTrainerServiceInfo(i);
  if (name == nil) then
   break; -- GetNumTrainerServices() does not check if you're talking to a trainer or not.
  end
  if (category == "available") then
   DEFAULT_CHAT_FRAME:AddMessage(name .. " (" .. rank .. ")");
  end
 end

==Patch changes==
* {{Patch 4.0.1|note=New return values: name (String), subType (String), category (String), texture (String), requiredLevel (Number), topServiceLine (Number).}}
```