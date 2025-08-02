# API GetCraftSkillLine

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
This command tells the caller which, if any, crafting window is currently open.  

 currentCraftingWindow = GetCraftSkillLine(n)

==Arguments==
:;n:{{apitype|number}} - Not sure how this is used, but any number greater than zero seems to behave identically.  Passing zero always results in a <code>nil</code> return value.

==Returns==
:;currentCraftingWindow:{{apitype|string}} - The name of the currently opened crafting window, or <code>nil</code> if no crafting window is open.  This will be one of "Enchanting" or "Beast Training".

==Details==
This function is not quite the same as [[API_GetCraftDisplaySkillLine|GetCraftDisplaySkillLine()]].  The latter returns <code>nil</code> in case the Beast Training window is open, while the current function returns "Beast Training".

==Patch changes==
* {{Patch 3.0.2|note=Removed.}}
```