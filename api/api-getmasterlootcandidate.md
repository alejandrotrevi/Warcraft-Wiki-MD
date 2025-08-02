# API GetMasterLootCandidate

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the name of an eligible player for receiving master loot by index.
 candidate = GetMasterLootCandidate(slot, index)

==Arguments==
:;slot:{{apitype|number}} - The loot slot number of the item you want to get information about
:;index:{{apitype|number}} - The number of the player whose name you wish to return. Typically between 1 and 40.

==Returns==
:;candidate:{{apitype|string}} - The name of the player.

==Details==
* Only valid if the player is the master looter.

==See also==
:* [[API GetNumRaidMembers|GetNumRaidMembers()]]
:* [[API GiveMasterLoot|GiveMasterLoot(slot, index)]]
```