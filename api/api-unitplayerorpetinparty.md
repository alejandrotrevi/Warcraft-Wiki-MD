# API UnitPlayerOrPetInParty

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} 
Returns true if a different unit or pet is a member of the party.
 inMyParty = UnitPlayerOrPetInParty(unit)

==Arguments==
:;unit:{{apitype|string}} : The unit to check for party membership.

==Returns==
:;inMyParty:{{apitype|boolean}} - 1 if the unit is another player or another player's pet in your party, nil otherwise.

==Details==
* This function returns nil if the unit is the player, or the player's pet.
```