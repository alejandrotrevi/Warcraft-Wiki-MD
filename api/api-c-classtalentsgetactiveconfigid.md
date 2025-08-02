# API C ClassTalents.GetActiveConfigID

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ClassTalents|system=ClassTalents}}
Returns the configID used for your currently selected specialization. Not to be confused with a talent loadout's configID
 activeConfigID = C_ClassTalents.GetActiveConfigID()

==Returns==
:;activeConfigID:{{apitype|number?}}

==Details==
In the context of talent trees, there's a functional divide between loadout configs, and the "active config". Each spec has an "active config", which contains all your active talents, regardless of what loadout you might have selected. This simplifies retrieving information about a player's talent setup, and acts as a safeguard for whenever a player manages to get into a situation where they have no active loadout (e.g. by deleting their loadouts, or by switching to the starter build, and making changes).
Whenever you activate a talent loadout by calling {{api|C_ClassTalents.LoadConfig}}, it will apply any required changes to your "active config", which is why the {{api|t=e|TRAIT_CONFIG_UPDATED}} event payload holds the "active config" ID, rather than the loadout configID.

{{apinavbox|C_Traits}}
```