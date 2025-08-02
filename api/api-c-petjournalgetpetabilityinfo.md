# API C PetJournal.GetPetAbilityInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about a battle pet ability.
 name, icon, type = C_PetJournal.GetPetAbilityInfo(abilityID)

==Arguments==
:;abilityID:{{apitype|number}} - battle pet ability ID, as returned by {{api|C_PetJournal.GetPetAbilityList}}, e.g. 362 for [[Howl]].

==Returns==
:;name:{{apitype|string}} - Ability name, e.g. "Howl"
:;icon:{{apitype|string}} - Ability icon texture path, e.g. "INTERFACE\ICONS\ABILITY_SHAMAN_FREEDOMWOLF.BLP"
:;type:{{apitype|battlePetTypeID}}
{{:battlePetTypeID|nocaption=}}

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|C_PetBattles.GetAbilityInfoByID}}
* {{api|C_PetJournal.GetPetAbilityList}}
```