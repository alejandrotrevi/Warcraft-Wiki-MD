# API IsModifierKeyDown

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if a modifier key is currently pressed down.
<syntaxhighlight lang="lua">
isDown = IsModifierKeyDown() <- IsControlKeyDown() <- IsLeftControlKeyDown()
                                                   <- IsRightControlKeyDown()
                             <- IsShiftKeyDown()   <- IsLeftShiftKeyDown()
                                                   <- IsRightShiftKeyDown()
                             <- IsAltKeyDown()     <- IsLeftAltKeyDown()
                                                   <- IsRightAltKeyDown()
</syntaxhighlight>

==Returns==
:;isDown:{{apitype|boolean}} - True if the specified modifier key is pressed down.

==Details==
{| {{apitable}}
{{apirow | Related Events | {{api|t=e|MODIFIER_STATE_CHANGED}} }}
{{apirow | Related API | {{api|IsModifiedClick}}, {{api|GetBindingByKey}} }}
|}

==Example==
Prints if the left-ctrl and left-shift modifiers are pressed down.
<syntaxhighlight lang="lua">
local function OnEvent(self, event, ...)
	if IsLeftControlKeyDown() and IsLeftShiftKeyDown() then
		print("hello")
	end
end

local f = CreateFrame("Frame")
f:RegisterEvent("MODIFIER_STATE_CHANGED")
f:SetScript("OnEvent", OnEvent)
</syntaxhighlight>
```