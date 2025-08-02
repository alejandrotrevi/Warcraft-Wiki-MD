# API GetSavedInstanceEncounterInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info about a specific encounter from a saved instance lockout.
 bossName, fileDataID, isKilled, unknown4 = GetSavedInstanceEncounterInfo(instanceIndex, encounterIndex)

==Arguments==
:;instanceIndex:{{apitype|number}} - Index from 1 to {{api|GetNumSavedInstances}}()
:;encounterIndex:{{apitype|number}} - Index from 1 to the number of encounters in the instance. For multi-part raids, this includes bosses that are not in that raid section, so the first boss in the second wing of a Raid Finder raid could actually have an encounterIndex of '4'.

==Returns==
:;bossName:{{apitype|string}} - The localized name of the encounter in question
:;fileDataID:{{apitype|number}} - The {{api|Texture_SetTexture|ID number}} for a texture associated with the encounter, usually an achievement icon. If Blizzard hasn't designated one for the encounter, expect this return to be nil.
:;isKilled:{{apitype|boolean}} - True if you have killed/looted the boss since the last reset period
:;unknown4:{{apitype|boolean}} - Unused by Blizzard, has an unknown purpose, and seems to always be false

==Example==
 /dump GetSavedInstanceEncounterInfo(1,1)
 => "Vigilant Kaathar", nil, true, false

==Patch changes==
* {{Patch 4.0.1|note=Added.}}

==See also==
* {{api|GetNumSavedInstances}} - Counts number of instances this function applies to
* {{api|GetLFGDungeonEncounterInfo}} - A moderately similar function to this one, except it works off of dungeon IDs instead of saved instance indexes
* {{api|GetSavedInstanceInfo}} - A more generic function; it allows you to pull up information on the dungeon itself instead of the individual encounters
```