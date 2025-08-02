# API C ClassTalents.GetConfigIDsBySpecID

**Contributor:** Numynum

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ClassTalents|system=ClassTalents}}
Returns a list of talent loadouts for a given spec
 configIDs = C_ClassTalents.GetConfigIDsBySpecID([specID])

==Arguments==
:;specID:{{apitype|number?}} - [[SpecializationID]] e.g. <code>PlayerUtil.GetCurrentSpecID()</code>, defaults to current spec

==Returns==
:;configIDs:{{apitype|number[]}} - list of loadout configIDs

==Details==
The list of loadouts is not available until {{api|t=e|TRAIT_CONFIG_LIST_UPDATED}} is fired. And {{api|t=e|TRAIT_CONFIG_LIST_UPDATED}} will fire on any changes to this list.

==See Also==
* {{api|C_ClassTalents.GetLastSelectedSavedConfigID}} to get the currently selected loadout configID
* {{api|C_ClassTalents.LoadConfig}} and {{api|C_ClassTalents.UpdateLastSelectedSavedConfigID}} to change loadouts
* {{api|C_Traits.GetConfigInfo}} to retrieve the loadout name and other information

{{apinavbox|C_Traits}}
```