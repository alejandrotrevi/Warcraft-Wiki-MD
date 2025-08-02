# API GiveMasterLoot

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Assigns an item from the current loot window to a group member, when in Master Looter mode.
 GiveMasterLoot(slot, index)

==Arguments==
:;slot:{{apitype|number}} - The index of the item you wish to assign. Should be between 1 and [[API GetNumLootItems|GetNumLootItems]]
:;index:{{apitype|number}} - The index of the player you wish to receive the item. You can retreive candidate names with [[API GetMasterLootCandidate|GetMasterLootCandidate]]

==Example==
Gives all the loot to yourself. Naughty.
 for ci = 1, GetNumRaidMembers() do
  if (GetMasterLootCandidate(ci) == UnitName("player")) then
   for li = 1, GetNumLootItems() do
    GiveMasterLoot(li, ci);
   end
  end
 end

==See also==
* [[API GetNumLootItems|GetNumLootItems()]]
* [[API GetMasterLootCandidate|GetMasterLootCandidate(index)]]
```