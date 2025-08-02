# API C PetJournal.GetPetSummonInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_PetJournal|system=PetJournalInfo}}
Needs summary.
 isSummonable, error, errorText = C_PetJournal.GetPetSummonInfo(battlePetGUID)

==Arguments==
:;battlePetGUID:{{apitype|WOWGUID}}

==Returns==
:;isSummonable:{{apitype|boolean}}
:;error:{{apitype|Enum.PetJournalError}}
{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! Value !! Field !! Description
|-
| 0 || {{apiname|None}} || 
|-
| 1 || {{apiname|PetIsDead}} || 
|-
| 2 || {{apiname|JournalIsLocked}} || 
|-
| 3 || {{apiname|InvalidFaction}} || 
|-
| 4 || {{apiname|NoFavoritesToSummon}} || 
|-
| 5 || {{apiname|NoValidRandomSummon}} || 
|}
:;errorText:{{apitype|string}}

==Patch changes==
* {{Patch 11.0.0|note=Removed <code>InvalidCovenant</code> field.}}
* {{Patch 9.0.1|note=Added <code>InvalidCovenant</code> field.}}
* {{Patch 8.2.0|note=Added.}}
```