# API C Garrison.GetOwnedBuildingInfoAbbrev

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns basic information on garrison buildings.
 id, name, textureKit, icon, rank, isBuilding, timeStart, buildTime, canActivate, canUpgrade, isPrebuilt = C_Garrison.GetOwnedBuildingInfoAbbrev(plotID)

==Arguments==
:;plotID:{{apitype|number}}

==Returns==
:;1. id:{{apitype|number}}
:;2. name:{{apitype|string}}
:;3. textureKit:{{apitype|string}}
:;4. icon:{{apitype|number}} : [[FileID]]
:;5. rank:{{apitype|number}} - Rank of the building in this plot, between 1 and 3
:;6. isBuilding:{{apitype|boolean}} - Returns true when the building in this plot is still in progress.
:;7. timeStart:{{apitype|number}} - Timestamp when the building was placed.
:;8. buildTime:{{apitype|number}} - Total duration (in seconds) until the building is completed and can be activated.
:;9. canActivate:{{apitype|boolean}} - Returns true when the build has been completed but the building has not yet been activated.
:;10. canUpgrade:{{apitype|boolean}} - Returns true when the building has available upgrades. false when already on max level or or plans not known.
:;11. isPrebuilt:{{apitype|boolean}}

==Patch changes==
* {{Patch 6.0.2|note=Added.}}

==See also==
* {{api|C_Garrison.GetOwnedBuildingInfo}}()

==External Links==
{{Elinks-api|t=a|nodoc=|wowprog=https://wowprogramming.com/docs/api/C_Garrison.GetOwnedBuildingInfoAbbrev.html}}
```