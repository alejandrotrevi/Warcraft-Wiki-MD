# API SetLootSpecialization

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets the player's loot specialization.
 SetLootSpecialization(specID)

==Arguments==
:;specID:{{apitype|number}} : [[SpecializationID]] - The specialization to receive loot for, regardless of current specialization; or 0 to receive loot for the current specialization.

==Triggers events==
* {{api|t=e|PLAYER_LOOT_SPEC_UPDATED}} upon changing loot specialization successfully.
* {{api|t=e|CHAT_MSG_SYSTEM}} only if <code>specID > 0</code>.

==Details==
* Attempting to set loot specialization to invalid values or specializations of another class fails silently.

==Patch changes==
* {{Patch 5.3.0|note=Added.}}

==See also==
* {{api|GetLootSpecialization}}
* {{api|GetSpecializationInfo}}
```