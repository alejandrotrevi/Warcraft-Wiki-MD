# API CreateFrame

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Creates a {{api|t=o|Frame}} object.
 frame = CreateFrame(frameType [, name, parent, template, id])

==Arguments==
:;frameType:{{apitype|string}} - Type of the frame; e.g. "Frame" or "Button".
:;name:{{apitype|string?}} - Globally accessible name to assign to the frame, or <code>nil</code> for an anonymous frame.
:;parent:{{apitype|Frame?}} - Parent object to assign to the frame, or <code>nil</code> to be parentless; cannot be a string. Can also be set with {{api|t=w|Region:SetParent}}()
:;template:{{apitype|string?}} - Comma-delimited list of [[virtual XML template]]s to inherit; see also a [https://github.com/Ketho/BlizzardInterfaceResources/blob/mainline/Resources/Templates.lua complete list] of FrameXML templates.
:;id:{{apitype|number?}} - ID to assign to the frame. Can also be set with {{api|t=w|Frame:SetID}}()

==Returns==
:;frame:{{apitype|Frame}} - The created Frame object or one of the other frame type objects.

==Frame types==
Possible frame types are available from the [[XML schema]] ({{framexml_link|AddOns/Blizzard_SharedXML/UI.xsd|name=UI.xsd}})
{| class="darktable"
|
* {{api|t=o|Frame}}
* {{api|t=o|ArchaeologyDigSiteFrame}}
* {{api|t=o|Browser}}
* {{api|t=o|Button}}
* {{api|t=o|CheckButton}}
* {{api|t=o|Checkout}}
* {{api|t=o|CinematicModel}}
* {{api|t=o|ColorSelect}}
* {{api|t=o|Cooldown}}
* {{api|t=o|DressUpModel}}
* {{api|t=o|EditBox}}
* {{api|t=o|FogOfWarFrame}}
* {{api|t=o|GameTooltip}}
* {{api|t=o|MessageFrame}}
|
* {{api|t=o|Model}}
* {{api|t=o|ModelScene}}
* {{api|t=o|MovieFrame}}
* {{api|t=o|OffScreenFrame}}
* {{api|t=o|PlayerModel}}
* {{api|t=o|QuestPOIFrame}}
* {{api|t=o|ScenarioPOIFrame}}
* {{api|t=o|ScrollFrame}}
* {{api|t=o|SimpleHTML}}
* {{api|t=o|Slider}}
* {{api|t=o|StatusBar}}
* {{api|t=o|TabardModel}}
* {{api|t=o|UnitPositionFrame}}
|}

==Details==
* Fires the frame's {{api|t=wh|OnLoad}} script, if it has one from an inherited template.
* Frames cannot be deleted or garbage collected, so it may be preferable to {{api|CreateFramePool|reuse}} them.
* [[Intrinsic frame]]s may also be used.
<!-- ** However, it is possible to destroy frames by parenting them to a user waypoint frame and triggering a loading screen.<ref>{{ref web|url=https://gist.github.com/Meorawr/135d5b266789546e0f63892bb2aed6a9|author=Meo[[File:Inv g fishingbobber 05.png|12px]]rawr (Daniel Yates)|title=MinimalUI.lua - "Can you recommend me a minimal UI?"}}</ref> -->

==Example==
* Shows a texture which is also parented to UIParent so it will be have the same UI scale and hidden when toggled with <code>Alt-Z</code>
[[File:API_CreateFrame_mushroom.png|thumb|right|[https://github.com/Gethe/wow-ui-textures/blob/live/ICONS/INV_Mushroom_11.PNG inv_mushroom_11]]]
<syntaxhighlight lang="lua">
local f = CreateFrame("Frame", nil, UIParent)
f:SetPoint("CENTER")
f:SetSize(64, 64)

f.tex = f:CreateTexture()
f.tex:SetAllPoints(f)
f.tex:SetTexture("interface/icons/inv_mushroom_11")
</syntaxhighlight>

* Creates a button which inherits textures and widget scripts from [https://www.townlong-yak.com/framexml/go/UIPanelButtonTemplate UIPanelButtonTemplate]
[[File:Button_Click_me.png|thumb|right|Click me]]
<syntaxhighlight lang="lua">
local btn = CreateFrame("Button", nil, UIParent, "UIPanelButtonTemplate")
btn:SetPoint("CENTER")
btn:SetSize(100, 40)
btn:SetText("Click me")
btn:SetScript("OnClick", function(self, button, down)
	print("Pressed", button, down and "down" or "up")
end)
btn:RegisterForClicks("AnyDown", "AnyUp")
</syntaxhighlight>

* Displays an [https://wow.tools/mv/?filedataid=125041&type=m2 animated model] for a [[DisplayID]].
<syntaxhighlight lang="lua">
local m = CreateFrame("PlayerModel")
m:SetPoint("CENTER")
m:SetSize(200, 200)
m:SetDisplayInfo(21723) -- murloccostume.m2
</syntaxhighlight>

* Registers for events being fired, like chat messages and when you start/stop moving.
<syntaxhighlight lang="lua">
local function OnEvent(self, event, ...)
	print(event, ...)
end

local f = CreateFrame("Frame")
f:RegisterEvent("CHAT_MSG_CHANNEL")
f:RegisterEvent("PLAYER_STARTED_MOVING")
f:RegisterEvent("PLAYER_STOPPED_MOVING")
f:SetScript("OnEvent", OnEvent)
</syntaxhighlight>

==Patch changes==
* {{Patch 2.0.1|note=The fourth argument, ''inheritFrame'', now accepts comma-separated values.}}
* {{Patch 1.11.0|note=Added fourth argument, ''inheritFrame''.<ref>{{ref web|url=http://forums.worldofwarcraft.com/thread.aspx?fn=wow-interface-customization&t=343889&p=#post382611|archiveurl=http://blue.cardplace.com/cache/wow-interface-customization/343889.htm|author={{Blizz}}[[slouken]]|date=20060523|title=Re: Upcoming 1.11 Changes - Concise List}}</ref>}}
* {{Patch 1.10.0|note=Added.<ref>{{ref web|url=http://forums.worldofwarcraft.com/thread.aspx?fn=wow-interface-customization&t=286547&p=#post286547|archiveurl=http://blue.cardplace.com/cache/wow-interface-customization/286547.htm|author=[[Iriel]]|date=20051228|title=Upcoming 1.10 Changes - Concise List}}</ref>}}

==See also==
* {{api|CreateFramePool()}}

==References==

<!-- luals
---@generic T, Tp
---@param frameType `T` | FrameType
---@param name? string
---@param parent? any
---@param template? `Tp` | Template
---@param id? number
---@return table|T|Tp frame
function CreateFrame(frameType, name, parent, template, id) end
-->
```