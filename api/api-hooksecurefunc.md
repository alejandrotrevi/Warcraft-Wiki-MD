# API hooksecurefunc

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Securely posthooks the specified function. The hook will be called with the same arguments after the original call is performed.
 hooksecurefunc([tbl,] functionName, hookfunc)

==Arguments==
:;tbl:{{apitype|table?}} - Table to hook the <code>functionName</code> key in; if omitted, defaults to the global table (<code>_G</code>).
:;functionName:{{apitype|string}} - name of the function being hooked.
:;hookfunc:{{apitype|function}} - your hook function.

==Example==
The following calls hook {{api|CastSpellByName}} and {{api|GameTooltip:SetUnitBuff|t=w}} without compromising their secure status. When those functions are called, the hook prints their argument list into the default chat frame.
 hooksecurefunc("CastSpellByName", print); -- Hooks the global CastSpellByName
 hooksecurefunc(GameTooltip, "SetUnitBuff", print); -- Hooks GameTooltip.SetUnitBuff

==Details==
* This is the only safe way to hook functions that execute protected functionality.
* <code>hookfunc</code> is invoked after the original function, and receives the same parameters; return values from hookfunc are discarded. 
* After this function is used on a function, setfenv() throws an error when attempted on that function
* You cannot "unhook" a function that is hooked with this function except by a UI reload. Calling hooksecurefunc() multiple times only ''adds'' more hooks to be called.
* Also note that using hooksecurefunc() may not always produce the expected result. Keep in mind that it actually replaces the original function with a new one (the function reference changes). For example, if you try to hook the global function "MacroFrame_OnHide" (after the macro frame has been displayed), your function will not be called when the macro frame is closed. It's simply because in Blizzard_MacroUI.xml the OnHide function call is registered like this:
 <OnHide function="MacroFrame_OnHide"/>
: The function ID called when the frame is hidden is the former one, before you hooked "MacroFrame_OnHide". The workaround is to hook a function called by "MacroFrame_OnHide":
 hooksecurefunc(MacroPopupFrame, "Hide", MyFunction)
* If you want to securely hook a frame's script handler, use {{api|Frame:HookScript|t=w}}:
 MacroPopupFrame:HookScript("OnHide", MyFunction)

==Restrictions==
* {{Tww-inline}} This function cannot be used to install hooks on functions with specific names. Attempting to do so will raise a "Cannot hook function" error.
{| class="darktable zebra"
|+ Unhookable function names
|-
| {{api|t=a|getfenv}} || {{api|t=a|rawset}} || {{api|t=a|select}}
|-
| {{api|t=a|getmetatable}} || {{api|t=a|pairs}} || {{api|t=a|setfenv}}
|-
| {{api|t=a|hooksecurefunc}} || {{api|t=a|pcall}} || {{api|t=a|setmetatable}}
|-
| {{api|t=a|ipairs}} || {{api|t=a|pcallwithenv}} || {{api|t=a|type}}
|-
| {{api|t=a|issecurevalue}} || {{api|t=a|scrub}} || {{api|t=a|unpack}}
|-
| {{api|t=a|issecurevariable}} || {{api|t=a|securecall}} || {{api|t=a|wipe}}
|-
| {{api|t=a|next}} || {{api|t=a|securecallfunction}} || {{api|t=a|xpcall}}
|-
| {{api|t=a|rawget}} || {{api|t=a|secureexecuterange}} || 
|}

==Patch changes==
* {{Patch 11.0.0|note=Can no longer install hooks on functions with specific names.}}
* {{Patch 2.0.1|note=Added.}}

{{API Trail Secure}}
<!-- luals
---@param tbl table
---@param name string
---@param hook function
---@overload fun(name: string, hook: function)
function hooksecurefunc(tbl, name, hook) end
-->
```