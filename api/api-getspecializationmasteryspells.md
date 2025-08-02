# API GetSpecializationMasterySpells

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|future=1|patch=11.2.0|link=https://github.com/Gethe/wow-ui-source/blob/11.2.0/Interface/AddOns/Blizzard_DeprecatedSpecialization/Deprecated_Specialization_Standard.lua#L21-L33}}
Returns the mastery spell ID of the specified specialization.
 masterySpell, masterySpell2 = GetSpecializationMasterySpells(specIndex [, isInspect, isPet])

==Arguments==
:;specIndex:{{apitype|number}} - The index of the specialization to query (1, 2, 3, 4) (Druids have four specializations)
:;isInspect:{{apitype|boolean?}} - Reserved. Must be nil
:;isPet:{{apitype|boolean?}} - Reserved. Must be nil

==Returns==
:;masterySpell:{{apitype|number}} - The Mastery spellID corresponding to one of the current player's specializations
:;masterySpell2:{{apitype|number}} - The Mastery spellID corresponding to one of the current player's specializations

==Values==
Example return values for different classes:

{| class="sortable darktable zebra"
! class !! specIndex 1 !! specIndex 2 !! specIndex 3 !! specIndex 4
|-
| Warrior || 76838|| 76856|| 76857
|-
| Paladin  || 76669|| 76671|| 76672
|-
| Hunter || 76657|| 76659|| 76658
|-
| Rogue || 76803|| 76806|| 76808
|-
| Priest || 77484|| 77485|| 77486
|-
| Death Knight || 77513|| 77514|| 77515
|-
| Shaman || 77222|| 77223|| 77226
|-
| Mage || 76547|| 76595|| 76613
|-
| Warlock || 77215 || 77219|| 77220
|-
| Monk || 117906|| 117907 || 115636
|-
| Druid || 77492|| 77493|| 77494 || 77495
|}

==Details==
For any type of data tracking, use the second parameter, since it is guaranteed to stay the same in different-language clients. This is especially important in Europe, where it is not uncommon for people with e.g. german or french client software to play on english servers. You can keep track of mappings for display by remembering the output pairs in a table, e.g.:

 local mySpecializationIndex = GetSpecialization(); --e.g.  1: Brewmaster
 local myMasterySpellID;
 if (mySpecializationIndex) then 
    myMasterySpellID = GetSpecializationMasterySpells(mySpecializationIndex);
 else
    myMasterySpellID = nil;
 end;

or we can store all the current player's mastery spells:

 local playerMasterySpells = {
     GetSpecializationMasterySpells(1), --e.g. Brewmaster
     GetSpecializationMasterySpells(2), --e.g. Mistweaver 
     GetSpecializationMasterySpells(3), --e.g. Windwalker
 )

==Patch changes==
* {{Patch 5.0.4|note=Added. Replaces [[GetTalentTreeMasterySpells]]}}

==See also==
* {{api|GetSpecializationInfo}}
* {{api|GetSpecializationInfoByID}}
```