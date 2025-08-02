# API GetTrainerServiceIcon

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the icon texture for a specific trainer service.
 icon = GetTrainerServiceIcon(index)

==Arguments==
:;index:{{apitype|number}} - Index of the trainer service to retrieve information about. Note that indices are affected by the trainer filter. (See [[API_GetTrainerServiceTypeFilter|GetTrainerServiceTypeFilter]] and [[API_SetTrainerServiceTypeFilter|SetTrainerServiceTypeFilter]].)

==Returns==
:;icon:{{apitype|fileID}} - The icon texture for a particular trainer service. nil if id is a header rather than a spell line.

==Example==
Prints skill names and icon textures when interacting with a trainer.
 local i, name, category, icon;
 for i=1,GetNumTrainerServices() do
  name, _, category = GetTrainerServiceInfo(i);
  if (name == nil) then
   break; -- GetNumTrainerServices() does not check if you're talking to a trainer or not.
  end
  if (category ~= "header") then
   icon = GetTrainerServiceIcon(i);
   DEFAULT_CHAT_FRAME:AddMessage(name .. ": " .. icon);
  end
 end
```