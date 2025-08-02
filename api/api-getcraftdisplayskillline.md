# API GetCraftDisplaySkillLine

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
This command retrieves displayable information for the current craft.
 name, rank, maxRank = GetCraftDisplaySkillLine()

==Parameters==
===Returns===
:;name:{{apitype|string}} - The name of the active craft, or <code>nil</code> if the current craft has no displayable name.  Also <code>nil</code> if there are no active crafting windows.

:;rank:{{apitype|number}} - The player's current rank for the named craft, if applicable. 

:;maxRank:{{apitype|number}} - The maximum rank for the named craft, if applicable. 

==Details==
The two crafts, Beast Training and Enchanting, have a slightly different UI: the latter has a blue progress bar at the top of the window indicating the player's rank while the former does not.  Accordingly, this function returns <code>nil</code> when the Beast Training window is open, while all return values should be valid when the Enchanting window is open.

==See Also==
[[API_GetCraftSkillLine|GetCraftSkillLine()]] returns the name of the currently active crafting window regardless of whether the name should be displayed.

==Patch changes==
* {{Patch 3.0.2|note=Removed.}}
```