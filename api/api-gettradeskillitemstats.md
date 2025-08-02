# API GetTradeSkillItemStats

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Gets the link string for a trade skill item.
 itemStats = GetTradeSkillItemStats(skillId)

==Parameters==
===Arguments===
:(index)

:;index:{{apitype|number}} - The row of the tradeskill listbox containing the item. The indices include the category headers. The tradeskill window doesn't have to be open, but the tradeskill and indices reflect the last state of the tradeskill window. The indices change if you expand or collapse headings (i.e. they exactly reflect the line number of the item as it is currently displayed in the tradeskill window).

Example:
Trade Blacksmithing: (window is open, all catagories shown)

{|
|-----
| Index || Name             
|-----
| 1 || - Daggers           
|-----
| 2 || Deadly Bronze Poniard
|-----
| 3 || Pearl-handled Dagger 
|-----
| 4 || Big Bronze Knife
|-----
| 5 || - One-Handed AxesCategory head
|}

Trade Blacksmithing: (window is open, only trade items are shown)

{|
|-----
| Index || Name                     
|-----
| 1 || - Trade Items               
|-----
| 2 || Elemental Sharpening Stone
|-----
| 3 || Thorium Shield Spike      
|}

===Returns===
:itemStats

:;itemStats:table of string

==Example==
 itemStats = {GetTradeSkillItemStats(2)} -- Get item stats for Deadly Bronze Poniard (see above)

===Result===
 itemStats = { "Uncommon", "Binds when equipped", "One-Hand", "|cffff2020Dagger|r", "16 - 30 Damage", "Speed 18", "+4 Strength", "Level 25", "Requires Level 20" }

===Note===
The curly braces around the functions call are critical, if you forget those your result will be:

 itemStats = "Uncommon"
```