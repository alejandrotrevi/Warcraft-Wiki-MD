# API GetLootSpecialization

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the player's current loot specialization.
 specID = GetLootSpecialization()

==Returns==
:;specID:{{apitype|number}} : [[SpecializationID]] - The current loot specialization, or 0 if loot specialization is not set (and the player receives loot based on their current specialization).

==Patch changes==
* {{Patch 5.3.0|note=Added.}}

==See also==
* {{api|SetLootSpecialization}}
* {{api|GetSpecializationInfoByID}}
* {{api|t=e|PLAYER_LOOT_SPEC_UPDATED}}
```