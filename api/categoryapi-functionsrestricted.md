# Category:API functions/restricted

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|notitle=1|nocat=}}
: <span class="noexcerpt" data-nosnippet>👉''See also: [[Object security]]''</span>
Addons and macro scripts are insecure code and are bound by different measures of restrictions when calling API functions. If [[Secure_Execution_and_Tainting|taint]] spreads to the rest of the UI this will render Blizzard code insecure too.
__TOC__

==protected==
APIs which cannot be called by [[secure code|insecure code]]. Fires {{api|t=e|ADDON_ACTION_FORBIDDEN}}.
<syntaxhighlight lang="lua">
/run JumpOrAscendStart()
</syntaxhighlight>
[[File:API_restricted_01.png|link=]]

''<font color="#4ec9b0"><code>*** ForceTaint_Strong ***</code></font> means it was called from a /run script, otherwise this would normally be the addon name.''

==hwevent==
APIs which require a hardware event (like the user clicking a button). Fires {{api|t=e|ADDON_ACTION_BLOCKED}}.
<syntaxhighlight lang="lua">
/run C_Timer.After(0, function() SetCurrentTitle(47) end) -- does not work
</syntaxhighlight>

==nocombat==
APIs which cannot be called in [[API_UnitAffectingCombat|combat]]. Fires {{api|t=e|ADDON_ACTION_BLOCKED}}.
<syntaxhighlight lang="lua">
/run CreateMacro("test", 136243) -- does not work in combat
</syntaxhighlight>

==secureframe==
Widget APIs which cannot be called on [[SecureTemplates|secure frames]] in combat. Fires {{api|t=e|ADDON_ACTION_BLOCKED}}.
<syntaxhighlight lang="lua">
/run ActionButton1:Hide() -- does not work in combat
</syntaxhighlight>
[[File:API_restricted_02.png|link=]]

==restrictedframe==
Widget APIs which cannot be called on [https://us.forums.blizzard.com/en/wow/t/ui-changes-in-rise-of-azshara/202487 restricted frames] such as nameplates. Throws a Lua error.
<syntaxhighlight lang="lua">
/dump NamePlate1:GetBottom() -- Error: [string "return NamePlate1:GetBottom()"]:1: Action[FrameMeasurement] failed because[Can't measure restricted regions]: attempted from: NamePlate1:GetBottom().
</syntaxhighlight>

==noscript==
APIs which cannot be called ''directly'' from a [[MACRO_script|/run]] script or WeakAura. Fires {{api|t=e|ADDON_ACTION_BLOCKED}} or silently fails, depending on the API.
<syntaxhighlight lang="lua">
/run C_AuctionHouse.SearchForFavorites({}) -- does not work and also bricks the AH in the process
</syntaxhighlight>

Putting it inside a function in an addon and then calling it manually works.
<syntaxhighlight lang="lua">
function Example() -- /run Example()
	C_AuctionHouse.SearchForFavorites({})
end
</syntaxhighlight>
<syntaxhighlight lang="lua">
-- or as a button
local btn = CreateFrame("Button", nil, UIParent, "UIPanelButtonTemplate")
btn:SetPoint("CENTER")
btn:SetSize(120, 40)
btn:SetText("Example")
btn:SetScript("OnClick", function(self, button)
	C_AuctionHouse.SearchForFavorites({})
end)
</syntaxhighlight>

[[Category:API functions]]
```