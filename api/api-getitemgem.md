# API GetItemGem

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.6|tentative=1}}
Returns the gem for a socketed equipment item.
 itemName, itemLink = GetItemGem(item, index) 

==Arguments==
:;item:{{apitype|string}} - The name of the equipment item (the item must be equipped or in your inventory for this to work) or the [[ItemLink]]
:;index:{{apitype|number}} - The index of the desired gem: 1, 2, or 3

==Returns==
:;itemName:{{apitype|string}} - The name of the gem at the specified index.
:;itemLink:{{apitype|string}} : [[ItemLink]]

==Details==
* Using the name may be ambiguous if you have more than one of the named item.

==Example==
Prints the 2nd gem socketed in this item.
<syntaxhighlight lang="lua">
local link = "|cff0070dd|Hitem:87451:::41438:::::53:257:::1:6658:2:9:35:28:1035:::|h[Helm of Elemental Binding]|h|r"
print(GetItemGem(link, 2)) -- "Perfect Brilliant Bloodstone", "|cff1eff00|Hitem:41438::::::::53:257:::::::|h[Perfect Brilliant Bloodstone]|h|r"
</syntaxhighlight>

==Patch changes==
* {{Patch 2.1.0|note=Added.}}
```