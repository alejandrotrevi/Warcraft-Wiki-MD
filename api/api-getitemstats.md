# API GetItemStats

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.5|removed=11.0.2}}
Returns a table of stats for an item.
 stats = GetItemStats(itemLink, [statTable])

==Arguments==
:itemLink
::String - An [[item link]] for which to get stats.
:statTable
::Table - An optional, empty table that will be filled with stats and returned.  If this parameter is omitted, a new table is returned.

==Returns==
:stats
::Table - A table of item stats.  If statTable was supplied, it will also be returned.

==Example==

The key for each entry in the dictionary is the name of a constant in Interface\FrameXML\GlobalStrings.lua, and the value of that constant is the localized name for the stat.  For example, an item that has 10 Stamina and no other stats would return <code>{ "ITEM_MOD_STAMINA_SHORT" = 10 }</code>.

 stats = GetItemStats(GetInventoryItemLink("player", 16))
 DEFAULT_CHAT_FRAME:AddMessage("Your main hand item has " .. 
     tostring(stats["ITEM_MOD_STAMINA_SHORT"] or 0) .. " " .. ITEM_MOD_STAMINA_SHORT .. ".")

would return something like

 Your main hand item has 10 Stamina.

The stat table contains the stats for the "base" version of an item, without any enchantments or gems.  There is no way to get the stats for the gemmed and enchanted version of an item.

==Details==
If statTable is supplied, it should be empty.  GetItemStats will add the stats of the item to this table without clearing it first.  Stats left over from a previous call to GetItemStats will be overwritten if present on the new item.  For example, if the table already contains 10 Strength and 20 Stamina and GetItemStats is called on an item with 30 Intellect and 30 Stamina, the new table will contain 10 Strength, 30 Intellect, and 30 Stamina, ''not'' 50 Stamina.

 local stats = {}
 GetItemStats("item:41002", stats)
 table.wipe(stats)
 GetItemStats("item:41003", stats)
```