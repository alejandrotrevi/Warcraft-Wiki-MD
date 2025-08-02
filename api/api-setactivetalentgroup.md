# API SetActiveTalentGroup

**Contributor:** DokoNinjaroboto

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets the active talent group of the player. This is the 5 second cast that occurs when clicking the <code>Activate These Talents</code> button in the talent pane.
 SetActiveTalentGroup(groupIndex);

==Arguments==
:;groupIndex:{{apitype|number}} - Ranging from <code>1</code> to <code>2</code> (primary/secondary talent group). To get the current one use {{api|GetActiveTalentGroup}}()

==Notes==
*Nothing will happen if the '''groupIndex''' is the currently active talent group

==Examples==
The following line will toggle between the player's talent groups
 SetActiveTalentGroup(3 - GetActiveTalentGroup())
```