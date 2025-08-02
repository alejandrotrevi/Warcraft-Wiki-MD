# API C ClassTalents.CommitConfig

**Contributor:** Numynum

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ClassTalents|system=ClassTalents}}
Applies any pending changes to the specified loadout configID
 success = C_ClassTalents.CommitConfig([savedConfigID])

==Arguments==
:;savedConfigID:{{apitype|number?}} This should be a loadout configID, from {{api|C_ClassTalents.GetLastSelectedSavedConfigID}} or {{api|C_ClassTalents.GetConfigIDsBySpecID}}. Not the ActiveConfigID from {{api|C_ClassTalents.GetActiveConfigID}}.

==Returns==
:;success:{{apitype|boolean}}

==See also==
{{api|C_Traits.CommitConfig}} should be used when committing changes to generic talents (e.g. dragonriding) and professions.

{{apinavbox|C_Traits}}
```