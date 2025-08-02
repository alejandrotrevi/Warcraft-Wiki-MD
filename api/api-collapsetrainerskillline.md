# API CollapseTrainerSkillLine

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Collapses a header in the trainer window, hiding all spells below it.
 CollapseTrainerSkillLine(index)

==Arguments==
:;index:{{apitype|number}} - The index of a line in the trainer window (if the supplied index is not a header, an error is produced).
::Index 0 ("All") will collapse all headers.
::Note that indices are affected by the trainer filter, see {{api|GetTrainerServiceTypeFilter}}() and {{api|SetTrainerServiceTypeFilter}}()

==Example==
Collapses all trainer headers. This can also be done by using index 0 instead.
 for i = 1, GetNumTrainerServices() do
 	local category = select(3, GetTrainerServiceInfo(i))
 	if category == "header" then
 		CollapseTrainerSkillLine(i)
 	end
 end

==Patch changes==
* {{Patch 4.0.1|note=Removed.}}

==See also==
* {{api|GetTrainerServiceInfo}}()
```