# API GetTradeSkillItemLink

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Gets the link string for a trade skill item.
 link = GetTradeSkillItemLink(skillId)

==Arguments==
:;skillId:{{apitype|number}} - The Id specifying which trade skill's link to get.  Trade Skill window must be open for this to work.  Indexes start at 1 which is the general category of the tradeskill, if you have selected a sub-group of trade skills then 1 will be the name of that sub-group.

Example:
Trade Blacksmithing: (window is open, all catagories shown)

{|
|-----
| Index || Name             
|-----
| 1 || Daggers           
|-----
| 2 || Heatseeker        
|-----
| 3 || One-handed Swords 
|-----
| 4 || Frostguard        
|}

Trade Blacksmithing: (window is open, only trade items are shown)

{|
|-----
| Index || Name                     
|-----
| 1 || Trade Items               
|-----
| 2 || Elemental Sharpening Stone
|-----
| 3 || Thorium Shield Spike      
|}

==Returns==
:;link:{{apitype|string}} - An item link string (color coded with href) which can be included in chat messages to represent the item which the trade skill creates.
```