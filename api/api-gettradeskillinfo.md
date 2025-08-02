# API GetTradeSkillInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Retrieves information about a specific trade skill.
 skillName, skillType, numAvailable, isExpanded, altVerb, numSkillUps, indentLevel, showProgressBar, currentRank, maxRank, startingRank = GetTradeSkillInfo(skillIndex)

==Arguments==
 (skillIndex)

:;skillIndex:{{apitype|number}} - The id of the skill you want to query.

==Returns==
 skillName, skillType, numAvailable, isExpanded, altVerb, numSkillUps

:;skillName:{{apitype|string}} - The name of the skill, e.g. "Copper Breastplate" or "Daggers", if the skillIndex references to a heading.
:;skillType:{{apitype|string}} - "header", if the skillIndex references to a heading; "subheader", if the skillINdex references a subheader for things like the cooking specialties;  or a string indicating the difficulty to craft the item ("trivial", "easy", "medium", "optimal", "difficult").
:;numAvailable:{{apitype|number}} - The number of items the player can craft with his available trade goods.
:;isExpanded:{{apitype|boolean}} - Returns if the header of the skillIndex is expanded in the crafting window or not
:;altVerb:{{apitype|string}} - If not nil, a verb other than "Create" which describes the trade skill action (i.e., for Enchanting, this returns "Enchant"). If nil the expected verb is "Create."
:;numSkillUps:{{apitype|number}} - The number of skill ups that the player can receive by crafting this item.
:;indentLevel:{{apitype|number}} - 0 or 1, indicates whether this skill should be indented beneath its header.  Used for specialty subheaders and their recipes.
:;showProgressBar:{{apitype|boolean}} - indicates if a sub-progressbar must be displayed with the specialty current and max ranks. In the normal UI, those values are only shown when the mouse is over the sub-header.
:;currentRank:{{apitype|number}} - is a the current rank for the specialty if showProgressBar is true.
:;maxRank:{{apitype|number}} - is a the maximum rank for the specialty if showProgressBar is true.
:;startingRank:{{apitype|number}} - is the starting rank where the specialty is available. It is used as the starting value of the progress bar.

==Example==
<!-- begin code -->
 local name, type;
 for i=1,GetNumTradeSkills() do
    name, type, _, _, _, _ = GetTradeSkillInfo(i);
    if (name and type ~= "header") then
       DEFAULT_CHAT_FRAME:AddMessage("Found: "..name);
    end
 end
<!-- end code -->
====Result====
:Displays all items the player is able to craft in the chat windows.

==Patch changes==
* {{Patch 5.0.4|note=Added "subheader" skillType and return values indentLevel, showProgressBar, currentRank, maxRank, and startingRank.}}
```