# API RunMacroText

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|protected|note=Use the "macro" action type of [[SecureActionButtonTemplate]].}}
Executes a string as if it was a macro.
 RunMacroText(macro)

==Arguments==
:;macro:{{apitype|string}} - the string is interpreted as a macro and then executed

==Example==
This creates an invisible button in the middle of the screen, that prints Hello World! every time it is clicked with the left button.
 -- Create the macro to use
 local myMacro = [=[
 /run print("Hello")
 /run print("World!")
 ]=]
 
 -- Create the secure frame to activate the macro
 local frame = CreateFrame("Button", nil, UIParent, "SecureActionButtonTemplate");
 frame:SetPoint("CENTER")
 frame:SetSize(100, 100);
 frame:SetAttribute("type", "macro") 
 frame:SetAttribute("macrotext", myMacro);
 frame:RegisterForClicks("LeftButtonUp");

==Details==
* Macros are executed via the client repeatedly firing the {{api|t=e|EXECUTE_CHAT_LINE}} event.
* The maximum macro length via this method is 1023 characters

==Patch changes==
* {{Patch 2.0.1|note=Protected.}}
```