# API C PvP.GetBattlefieldVehicleInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_PvP|system=PvpInfo}}
Returns battleground vehicle info.
 info = C_PvP.GetBattlefieldVehicleInfo(vehicleIndex, uiMapID)

==Arguments==
:;vehicleIndex:{{apitype|number}}
:;uiMapID:{{apitype|number}} : [[UiMapID]]

==Returns==
:;info:{{apitype|BattlefieldVehicleInfo}}
{{:Struct BattlefieldVehicleInfo|nocaption=1}}

==Patch changes==
* {{Patch 9.0.1|note=Moved to <code>C_PvP.GetBattlefieldVehicleInfo()</code>}}
* {{Patch 3.1.0|note=Added as <code>GetBattlefieldVehicleInfo()</code>}}
```