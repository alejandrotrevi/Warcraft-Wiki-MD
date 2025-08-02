# API C Garrison.GetFollowers

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a list of garrison tech followers.
 info = C_Garrison.GetFollowers([followerType])

==Arguments==
:;followerType:{{apitype|Enum.GarrisonFollowerType?}}
{{:Enum.GarrisonFollowerType|nocaption=1}}

==Returns==
:;info:{{apitype|GarrFollowerInfo[]}}
{{:Struct_GarrFollowerInfo|nocaption=1}}

==Details==
* This does not return a complete list of all possible followers, it will be whatever is displayed for the character in the Garrison UI.

==Example==
Dumps the first follower.
<syntaxhighlight lang="lua">
local followers = C_Garrison.GetFollowers()
DevTools_Dump(followers[1])
</syntaxhighlight>
<syntaxhighlight lang="lua">
{
	classAtlas = "GarrMission_ClassIcon-Priest-Discipline",
	className = "Discipline Priest",
	classSpec = 124,
	displayIDs = {
		[1] = {
			followerPageScale = 1,
			id = 67797
			showWeapon = true,
		}
	},
	displayHeight = 0.5,
	displayScale = 1,
	followerID = "0x0000000004CBDB61",
	followerTypeID = 4,
	garrFollowerID = 856
	height = 1,
	iLevel = 900,
	isAutoTroop = false,
	isCollected = true,
	isFavorite = false,
	isMaxLevel = true,
	isSoulbind = false,
	isTroop = false,
	level = 45,
	levelXP = 200000,
	name = "Calia Menethil",
	portraitIconID = 1401872,
	quality = 4,
	scale = 0.69999998807907,
	slotSoundKitID = 62813,
	xp = 60600,
}
</syntaxhighlight>

==Patch changes==
* {{Patch 7.0.3|note=Supports Legion Troops/Champions.}}
* {{Patch 6.2.0|note=Supports the Shipyard.}}
* {{Patch 6.0.2|note=Added.}}
```