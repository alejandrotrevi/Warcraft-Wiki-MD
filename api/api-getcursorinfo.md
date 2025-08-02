# API GetCursorInfo

**Contributor:** AlternativeTheory

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns what the mouse cursor is holding.
 infoType, ... = GetCursorInfo()

==Returns==
The first return value is a string indicating the nature of an object on the cursor; additional return values provide detail. The following return value combinations have been observed:

*"item", itemID, itemLink
*:itemId : {{apitype|number}} - Item ID of the item on the cursor.
*:itemLink : {{apitype|string}} - [[ItemLink]] of the item on the cursor.

*"spell", spellIndex, bookType, spellID, baseSpellID
*:spellIndex: {{apitype|number}} - The index of the spell in the spell book.
*:bookType : {{apitype|string}} - Always BOOKTYPE_SPELL (or else the type would have been "petaction").
*:spellID : {{apitype|number}} - Spell ID of the spell on the cursor
*:baseSpellID : {{apitype|number}} - [[API_FindBaseSpellByID|Base Spell ID]] if an [[API_FindSpellOverrideByID|Override spell]] is on the cursor

*"petaction", spellID, spellIndex, retVal3
*:spellID: {{apitype|number}} - Spell ID of the pet action on the cursor, or unknown 0-4 number if the spell is a shared pet control spell (Follow, Stay, Assist, Defensive, etc...)..
*:spellIndex: {{apitype|number}} - The index of the spell in the pet spell book, or nil if the spell is a shared pet control spell (Follow, Stay, Assist, Defensive, etc...).
*:retVal3: Needs summary.

*"macro", index
*:index : {{apitype|number}} - The index of the macro on the cursor.

*"money", amount
*:amount : {{apitype|number}} - The amount of money in copper.

*"mount", mountID, mountIndex
*:mountID: {{apitype|number}} - The ID of the mount.
*:mountIndex: {{apitype|number}} - The index of the mount in the journal.

*"merchant", index
*:index : {{apitype|number}} - The index of the merchant item.

*"battlepet", petGUID
*:petGUID : {{apitype|string}} - GUID of a battle pet in your collection.

==Details==
{| {{apitable}} border: 0px;"
{{apirow | Related Events | {{api|t=e|CURSOR_UPDATE}}<br>{{api|t=e|CURSOR_CHANGED}} }}
{{apirow | Related API | {{api|GetCursorPosition}} }}
|}

==Example==
The following snippet, if you're holding an item, prints out the amount of that item in your bags.
 local infoType, itemID, itemLink = GetCursorInfo()
 if infoType == "item" then
  print("You have " .. GetItemCount(itemLink) .. "x" .. itemLink .. " in your bags.")
 else
  print("You're not holding an item on your cursor.")
 end
```