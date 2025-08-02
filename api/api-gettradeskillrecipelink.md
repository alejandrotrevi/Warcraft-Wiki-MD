# API GetTradeSkillRecipeLink

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the [[EnchantLink]] for a trade skill.
 link = GetTradeSkillRecipeLink(index)

==Arguments==
:;index:{{apitype|number}} - The row of the tradeskill listbox containing the item. The indices include the category headers. The tradeskill window doesn't have to be open, but the tradeskill and indices reflect the last state of the tradeskill window. The indices change if you expand or collapse headings (i.e. they exactly reflect the line number of the item as it is currently displayed in the tradeskill window).

==Returns==
:;link:{{apitype|string}} - An [[EnchantLink]] (color coded with href) which can be included in chat messages to show the reagents and the items the trade skill creates.

==Example==
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
```