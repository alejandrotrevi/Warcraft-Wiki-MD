# API C ClassTalents.GetLastSelectedSavedConfigID

**Contributor:** Numynum

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ClassTalents|system=ClassTalents}}
Returns the value stored using {{api|C_ClassTalents.UpdateLastSelectedSavedConfigID}}.
 configID = C_ClassTalents.GetLastSelectedSavedConfigID(specID)

==Arguments==
:;specID:{{apitype|number}} - [[SpecializationID]] e.g. <code>PlayerUtil.GetCurrentSpecID()</code>

==Returns==
:;configID:{{apitype|number?}}

==Details==
This will return whatever was set with {{api|C_ClassTalents.UpdateLastSelectedSavedConfigID}}. Which means that if a badly written addon (including the default UI) fails to write the correct value, this API won't accurately reflect the current loadout.

If you're currently in a starter build, the configID is -2 (as per <code>Constants.TraitConsts.STARTER_BUILD_TRAIT_CONFIG_ID</code>)

==See Also==
* {{api|C_ClassTalents.UpdateLastSelectedSavedConfigID}} which sets the value retrieved with this API
* {{api|C_Traits.GetConfigInfo}} to retrieve the loadout name
* {{api|C_ClassTalents.GetConfigIDsBySpecID}} to list talent loadouts

{{apinavbox|C_Traits}}
```