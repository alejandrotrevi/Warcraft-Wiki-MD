# API GetLootSlotLink

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the item link for a loot slot.
 itemLink = GetLootSlotLink(index)

==Arguments==
:;index:{{apitype|number}} - The index of the item in the list to retrieve info from (1 to GetNumLootItems())

==Returns==
:;itemLink:{{apitype|string}} - The [[itemLink]] for the specified item, or nil if <code>index</code> is invalid.

==Example==
The example below will display the item links into your chat window.

 local linkstext = ""
 for index = 1, GetNumLootItems() do
   if LootSlotHasItem(index) then
     local itemLink = GetLootSlotLink(index)
     linkstext = linkstext .. itemLink
   end
 end
 print(linkstext)
```