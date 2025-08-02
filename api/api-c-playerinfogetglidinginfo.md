# API C PlayerInfo.GetGlidingInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_PlayerInfo|system=PlayerInfo}}
Returns the [[Dragonriding]] gliding speed.
 isGliding, canGlide, forwardSpeed = C_PlayerInfo.GetGlidingInfo()

==Returns==
:;isGliding:{{apitype|boolean}} - True when the player is currently gliding.
:;canGlide:{{apitype|boolean}} - True when the player is in a Dragonriding zone and on an applicable mount.
:;forwardSpeed:{{apitype|number}} - The gliding speed, this is 65 for max dive speed and can go up to 100 when using abilities.

==Example==
Shows the gliding and movement speed on the center of the screen.
<syntaxhighlight lang="lua">
local f = CreateFrame("Frame", nil, UIParent, "BackdropTemplate")
f:SetPoint("CENTER", 0, 50)
f:SetSize(132, 50)
f:SetBackdrop({
	bgFile = "Interface/Tooltips/UI-Tooltip-Background",
	edgeFile = "Interface/Tooltips/UI-Tooltip-Border",
	edgeSize = 16,
	insets = { left = 4, right = 4, top = 4, bottom = 4 },
})
f:SetBackdropColor(0, 0, 0, .5)
f.glide = f:CreateFontString(nil, nil, "GameTooltipText")
f.glide:SetPoint("TOPLEFT", 10, -12)
f.movespeed = f:CreateFontString(nil, nil, "GameTooltipText")
f.movespeed:SetPoint("TOPLEFT", f.glide, "BOTTOMLEFT")

C_Timer.NewTicker(.1, function()
	local isGliding, canGlide, forwardSpeed = C_PlayerInfo.GetGlidingInfo()
	local base = isGliding and forwardSpeed or GetUnitSpeed("player")
	local movespeed = Round(base / BASE_MOVEMENT_SPEED * 100)
	f.glide:SetText(format("Gliding speed: |cff71d5ff%d%%|r", forwardSpeed))
	f.movespeed:SetText(format("Move speed: |cffffff00%d%%|r", movespeed))
end)
</syntaxhighlight>

{| class="darktable"
| [[File:API_C_PlayerInfo.GetGlidingInfo1.mp4|814px]]
|}

==See also==
* {{api|GetUnitSpeed}}
```