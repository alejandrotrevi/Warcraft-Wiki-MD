# API IsInCinematicScene

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true during in-game cinematics/cutscenes involving NPC actors and scenescripts.
 inCinematicScene = IsInCinematicScene()

==Returns==
:;inCinematicScene:{{apitype|boolean}}

==Example==
<onlyinclude>Prints what type of cinematic is playing on {{api|t=e|CINEMATIC_START}}.
<syntaxhighlight lang="lua">
local function OnEvent(self, event, ...)
	if InCinematic() then
		print("simple cinematic")
	elseif IsInCinematicScene() then
		print("fancy in-game cutscene")
	end
end

local f = CreateFrame("Frame")
f:RegisterEvent("CINEMATIC_START")
f:SetScript("OnEvent", OnEvent)
</syntaxhighlight></onlyinclude>
```